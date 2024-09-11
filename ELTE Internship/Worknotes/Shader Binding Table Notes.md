# Shader Binding Table

A logical unit, consisting of **shader function handles** and **embedded parameters** for **ray tracing** functions.
Shaders in the table are executed depending on whether or not a geometry was hit by a ray, and which geometry was hit.
When a geometry is intersected, a set of parameters specified on both the host and device side of the application combine to determine which shader is going to be executed.

## Rasterization vs. Ray tracing 

|                 | Rasterization                                                                                     | Ray tracing                                        |
| --------------- | ------------------------------------------------------------------------------------------------- | -------------------------------------------------- |
|                 |                                                                                                   |                                                    |
| **Determinism** | Objects are batched by the shader they use, we knopw which set of shader must be called for them. | We don't know which objects a ray will hit.        |
| **Memory**      | N/A                                                                                               | Needs the whole scene in the memory (or its proxy) |
![](https://www.willusher.io/img/rtx-execution-model.svg)

RTX API uses this SBT to associate objects with shaders.

## Shaders
### Ray Generation
Entry point to the ray tracer to generate the initial set of rays.
Multiple of these can be written into the table, but only once can be called for a launch.

### Intersection
Used for computing ray intersections with custom primitives.
**Optional shader**

### Any Hit
Gets called for each potential intersection found along the ray.
Can be used to filter potential intersections, for example with transparent objects.
**Optional shader**

### Closest Hit
Called for the closest hit along the ray.
Can compute and return intersection information through the **ray payload** or **trace additional rays**.

### Miss
Called when no hit is found.

## Hit Group
Consists of the [[Shader Binding Table Notes#Closest Hit|Closest Hit]], [[Shader Binding Table Notes#Any Hit|Any Hit]], [[Shader Binding Table Notes#Intersection|Intersection]] shaders.
Describes how to process rays and intersections.

## Shader Record
A pair consisting of one or more **shader functions** and **embedded parameters** to these functions.