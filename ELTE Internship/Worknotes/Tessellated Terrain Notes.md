# OpenGL Tesselation Engine

1. [[#Tessellation Control Shader]] (programmable)
2. [[#Tessellation Primitive Generator]] (fixed stage - configurable)
3. [[#Tessellation Evaluation Shader]] (programmable)

Only accepts "patches" as primitives for rendering

## Tessellation Control Shader
- executed once per vertex of the input patch
- outer-, inner tesselation levels

## Tessellation Primitive Generator
- generates the new primitives
- three types of primitives that can be tessellated:
	- isolines
	- triangles
	- quads
- the type of the primitive is defined in the TES 


## Tessellation Evaluation Shader 
- after the TEG, the newly generated primitives and the original input patch are combined <mark style="background: #FFF3A3A6;">into the output patch</mark> 
- is executed for each vertex in the tessellated output patch
- vertices are given a parameter-space coordinate 
# Dynamic Level of Detail (LOD)
## Camera Distance Approach
- For each edge, it's distance from the camera is calculated (average of the distance of the 2 vertices of the edge)
- Interpolation of distance between max and min tessellation levels
- This is done for all 4 edges of the quad, and the calculated tessellation level is applied to the corresponding outer-level 
- The inner tessellation levels are an average of the outer levels
## Sphere Approach
- Tessellation based on triangle size
- Sphere around each edge => projected into screen space => Diameter of the sphere calculated => comparison of its width to the target triangle width => if the width is greater than the target, tessellate!
- Sphere is needed for edge cases like the edge being too close to the camera

# Terrain Rendering 
## Uniform patch terrain
- in general very wasteful
- for larger/more complex terrains, performance decreases a lot

## Non-uniform Patch Terrain
- patches closer to the camera are smaller
- patches farther from the camera are larger for smaller vertex count
- problems introduced:
	- cracks => happens when the edges are not the same size => results in a "T-junction"
- The solution: 
	- scale factors for edges (TGC)
	- "fractional_even_spacing" parameter in the evaluation shader
# Implementation (notes)
## With Uniform patches
- Only one patch's vertex data is needed for rendering all the vertices of all the patches
- No cracks
## With Non-uniform patches 
- Quadtrees for generating the patches
- "The basic process for constructing the quadtree is as follows:
	- Start with the root node. This is a single patch covering the entire terrain.
	- Compare the position of the camera in the world to the origin of the node. If the camera is close enough to require additional levels of detail, subdivide the node into four smaller children.
	- Repeat for each child node until a maximum subdivision level is reached, or the camera is far enough away that it doesn’t require any more subdivision for an acceptable level of detail."