# Concurrent binary tree (CBT)
Halfedge mesh representation:
- h - ID
- TWIN - ID of the halfedge pointing to the same edge
- PREV
- NEXT
- VERT - from which vertex
- EDGE
- FACE
## Bisection Based Triangulation 
- Simple 
- Preserves topology of input mesh - good for animated assets
### Initialisation
**Bisector for Each Halfedge**
"Note that we refer to a bisector using the notation $b^d_j$, where 𝑑 ≥ 0 denotes its subdivision level and 𝑗 ≥ 0 its index."
**Root Bisector Vertices**
Taking the average of all vertices defining the plane on which the root bisector vertex exists.
**Neighboring Bisectors**
We can retrieve these using the NEXT, PREV and TWIN operators. 
Notation:
$Next(h_7) = h_8 → b^0_8$ and similarly with PREV and TWIN, where if $b^d_n$, then d equals the subdivision level, and n is a series of the halfedge + bisector ID


### Progressive Subdivision Operators (2)
1. Guarantees conforming topologies when a applied locally.
2. Allows for "incremental updates" on an existing triangulation -> this provides an alternative to computing entire triangulations in either bottom-up or top-down fashion

**Bisector Refinement** -> for increasing the resolution of our mesh
*Notation:*
$b^d_j \rightarrow b^{d+1}_{2j}$ (first child)
and
$\_ \rightarrow b^{d+1}_{2j+1}$ (second child)

**Bisector Vetrices via Subdivision Matrix**
![[Pasted image 20240709215414.png]]

**Algorithm 5 Pointer Refinement - Notes**
![[Pasted image 20240709220220.png]]
**Bisector Decimation** -> for decreasing the resolution of our mesh

**Neighbour Refinement Rule**
- isolation at a boundary
- in pairs of same subdivision level
**Bisector Decimation Rule**
- four bisectors of same subdivision depth forming a cycle via their NEXT and PREV operators
- two border bisectors of same subdivision depth having their TWIN point to the null bisector
Both operations require their neighbours to be updated as well.
## GPU Implementation as a CBT
### CBT
A full binary tree where:
- the leaf nodes store binary values and form a bitfield
- the remaining nodes form a sum-reduction tree over these binary values, aka. tells us the number of ones in its child nodes
Stored as a binary heap ($2^{D+1}$).

**Initialization**
CBT of depth: D>=0 
Memory pool of capacity, an array of constant-sized memory blocks: $2^D$
- must be sized in advance, cannot be resized
- bits are associated with memory blocks
- bits: 0 = free, 1 = allocated

**Binary Search Algorithm**
$O(D)$ complexity for retrieving the i-th bit set to one.
See pseudo-code for further details.

**Block iteration and updates**
Parallelization of block iteration happens through scheduling a thread for each memory block.
Steps after request for a new memory block:
1. atomic incrementation of an allocation counter
2. the original value tells us which 0-valued bit in the CBT's bitfield should be set to 1
3. set it to one and write data to the associated memory block
See pseudo-code for further details.

### GPU Triangulation Pipeline
![[Pasted image 20240710083257.png]]
D >= Log(H) (upperbound), where H is the number of half edges in our input mesh.
Data for the bisectors in the memory pool:
- 3 integers that act as pointers for NEXT, PREV, TWIN of each bisector
- 1 integer for the bisector index
For concurrent split and/or merge the following is also required:
- 1 integer for encoding the split/merge command as a bit code, which is concurrently modified via atomic bitwise-OR
- 4 integers for storing unused memory pool locations for writing
The former guarantees that the evaluation for each bisector only happens once.
The latter is needed because we only allow one refinement/decimation during each incremental update, aka. in the worst case a bisector splits into 4 other bisectors at max (when it's part of a compatibility chain of two foreign bisectors under refinement).
- 1 integer as an atomic counter
- $2^D$ buffer of 2 integers per element for caching the results of Algo 7 and 8 (searching for i-th bit of value 1 and 0)

**Initialization**
- H root bisector initialization
	- bisector.index = $log_2(H) + h$  where $h \in [0,H-1]$ denotes the mesh's halfedge
	- bisector.next  = NEXT(h)
	- bisector.prev  = PREV(h)
	- bisector.twin  = TWIN(h)
- sum-reduction tree computing

**Incremental Update Pipeline**
9 steps:
1. **ResetCounter** - on one thread
2. **CachePointers** - result of Algorithm 7 on 1. and Algorithm 8 on 2. integer of the pointer buffer
3. **ResetCommands** - set the command of each bisector to zero
4. **GenerateCommands** - decision is made by decompressing the vertices of the bisector via Algorithm 2 and making sure it's screen space area matches a user-defined value. Options:
	- Refinement - Algorithm 3
	- Decimation - Algorithm 4
	- Nothing 
5. **ReserveBlocks** - "When both are required(split and merge) (this happens when a bisector decides to merge and belongs to the compatibility chain of another bisector that requests a split), we ignore the merge command and only apply splits."
6. **FillNewBlocks** - Computing and saving the index of each newly created bisector to the memory blocks it has allocated. 
	- At the end of this step all bisectors have a valid index, and a partial number of valid neighbours
7. **UpdateNeighbours** 
8. **UpdateBitfield** - CBT bitfield update. Non-null command bisectors are freed and associated with the null bit. Depending on command, we set up to 4 bits to one to save the allocations triggered by the bisector.
9. **SumReduction** - Update of the sum-reduction tree -> new round is possible

## Performance Measurements

**Absolute Timings**
"Note that update performances
are similar between Figure 7 and Figure 8 despite the CBT being twice as big for the latter scene.
This is due to the way we implement our GenerateCommands kernel, which requires evaluating the
world-space position of each bisector’s vertices; this evaluation is more expensive for Figure 1 and
Figure 7 because we rely on double precision"

**Performances Against the Original CBT Implementation**

## Important algorithms:
1. Root Bisector Vertices 
	- ![[Pasted image 20240710163227.png]]
2. Bisector Vertices 
	- ![[Pasted image 20240710163243.png]]
3. Adaptive Refinement
	- ![[Pasted image 20240710163309.png]]
4. Conservative Decimation
	- ![[Pasted image 20240710163325.png]]
5. Pointer Refinement
	- ![[Pasted image 20240710163401.png]]
6. Pointer Decimation
	- ![[Pasted image 20240710163429.png]]
7. Find the i-th bit set to one
	- ![[Pasted image 20240710163456.png]]
8. Find the i-th bit set to zero
	- ![[Pasted image 20240710163515.png]]
9. Memory pool update using CBT
	- ![[Pasted image 20240710163535.png]]
+
Rules:
- ![[Pasted image 20240710163605.png]]