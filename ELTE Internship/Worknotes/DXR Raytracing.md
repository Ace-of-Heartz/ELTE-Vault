# Acceleration Structures

**Motivation:** With raytracing, the number of intersection tests are key determining factor in the efficiency and speed of our application.
Using *Acceleration Structures*, we can reduce the number of ray-triangle intersection tests during our rendering process.
These structures are divided into a two-level tree, consisting of [[DXR Raytracing#Top Level Acceleration Structure (TLAS)|Top Level Acceleration Structures]] and [[DXR Raytracing#Bottom Level Acceleration Structure (BLAS)|Bottom Level Acceleration Structures]].
## Bottom Level Acceleration Structure (BLAS)
**Consists of:** a multiple vertex buffers, each with its own transformation matrix.
**Notes:** If an object is instantiated several times in the same BLAS, it's geometry will be *duplicated* 
## Top Level Acceleration Structure (TLAS)
**Consists of:** object instances for each BLAS, each with its own transformation matrix

