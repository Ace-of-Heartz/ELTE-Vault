# Program layout in memory
## Tools
- Cache (data cache vs. instruction cache)
- Stack (frame)
- Heap

# Common Issues
## Stalling
**Problem:**
- two consecutive instructions depend on each other => one's execution halts the other's
- idle bubble
**Solution:**
- Compiler shuffles around our code to minimize or avoid the effect of this
- CPUs try to reorder execution on the fly

## Branch Prediction
**Problem:**
- guess which branch is taken and fetch date from there 
- => if the guess is wrong, the pipeline gets stalled, it needs to get flushed and the correct branch's instructions must be fetched 
**Solution:**
- using "backward branch"
- => make then "then" part the most treaded

# Graphics Pipeline
Different computer units => unified compute units (CUDA cores on NVidia)
- No branch prediction
- No Cache
- => but (=) more space
SIMD Processing:
- same code on many different items (multiple ALUs sharing the same code)
**Implicit vectorization**
**Latency hiding**
	- many small contexts = maximal latency hiding
	- few, large contexts = low latency hiding
GPU **main command buffer** almost like a communication channel between CPU and GPU
Synchronization:
- **Client Sync (fence)**: block the CPU program until the GPU either receives or finishes the commands sent up until the synchronization command
- **Server Sync (barrier)**: block the GPU from executing commands until the commands issued before the barrier are finished

# Compute shaders:
Completely user controlled execution frequency, unrelated to the graphics pipeline
- **Work item:**
	- single thread, smallest unit of command execution
- **Work group:**
	- 1,2 or 3 dimensional grid of work items
	- smallest autonomous unit of execution
	- no fixed order of work item execution
- **Compute space:**
	- 1,2 or dimensional grid of work items
	- no fixed order of work group execution
## Syncs:
- **memoryBarrierAtomicCounter**: 
	- block execution until all previous atomic writes are visible
- **memoryBarrier{Image|Buffer|Shared}**:
	- wait until previously issued image/buffer/shared variable writer propagate
- **memoryBarrier:**
	- all of above
- **groupMemoryBarrier:**
	- almost the same as memoryBarrier, but restricted to work group only