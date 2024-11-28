# N-Body simulation with Extras
- **Points**: 90%

## Notes
"Numerical integration is usually performed over small timesteps using a method such as [leapfrog integration](https://en.wikipedia.org/wiki/Leapfrog_integration "Leapfrog integration"). However all numerical integration leads to errors. Smaller steps give lower errors but run more slowly. Leapfrog integration is roughly 2nd order on the timestep, other integrators such as [Runge–Kutta methods](https://en.wikipedia.org/wiki/Runge%E2%80%93Kutta_methods "Runge–Kutta methods") can have 4th order accuracy or much higher.

One of the simplest refinements is that each particle carries with it its own timestep variable, so that particles with widely different dynamical times don't all have to be evolved forward at the rate of that with the shortest time."

## Sources
- [N-Body Simulation](https://en.wikipedia.org/wiki/N-body_simulation)
- [NVIDIA - N-Body Simulation](https://developer.nvidia.com/gpugems/gpugems3/part-v-physics-simulation/chapter-31-fast-n-body-simulation-cuda) 
- [Barnes-Hut](http://arborjs.org/docs/barnes-hut)
- [Barnes-Hut Paper](https://iss.oden.utexas.edu/Publications/Papers/burtscher11.pdf)
- [GitHub - GPU N-Body](https://github.com/bneukom/gpu-nbody)