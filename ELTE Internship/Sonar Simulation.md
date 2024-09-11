# Sonar Simulation
## Description:
Szakmai gyakorlat vagy szakdolgozat téma alapszakos hallgatók számára
**Előfeltétel :** *Számítógépes grafika gyakorlat, C++ ismerete*
**Előnyt jelent :** *Haladó számítógépes grafika, GPGPU*
**Témakiírás :** Sugárkövetés implementálása **DXR raytracing shader-ek** segítségével és ezek alkalmazása szonár hanghullám terjedésének, visszaverődésének
és törésének szimulációjára. Szimuláció eredményének többféle hatékony vizualizációjának implementálása. **C++** és **DirectX12** vagy **Vulkan** megegyezés szerint.

Internship or thesis project for undergraduate students.
**Pre-requirements:** *Computer graphics seminar; knowledge about C++*
**Advantage are the following:** *Advanced computer graphics, GPGPU*
**Topic description:** Raytracing implementation with the help of **DXR raytracing shaders**, and their usage in simulating sonar sound-wave propagation, reverberation and refraction.  
Implementations of effective visualisation of the simulations' results. 
**C++** and **DirectX12** or **Vulkan** according to individual agreements.
## Technologies:
### Vulkan:
### DirectX 12:
DirectX 12 wrapper: https://github.com/axodox/axodox-graphics

## References:
### Assigned documents:
#### General:
##### Papers:
- [Tesselated Terrain](https://victorbush.com/2015/01/tessellated-terrain/) - [[Tessellated Terrain Notes]] #ReviewDone
- [Compute Shaders - Concurrent Binary Trees](https://www.arxiv.org/pdf/2407.02215) [[Compute Shaders Notes]] #ReviewDone
- [DXR Raytracing Tutorial](https://developer.nvidia.com/rtx/raytracing/dxr/dx12-raytracing-tutorial-part-1)
#### DXR:
- [DXR Tutorial Helpers](https://developer.nvidia.com/rtx/raytracing/dxr/DX12-Raytracing-tutorial/dxr_tutorial_helpers)
- [Mesh Shaders]([https://www.inf.elte.hu/dstore/document/2512/B%C3%A1lint%20Csaba%20Advanced%20Computer%20Graphics%20Slides.pdf](https://www.inf.elte.hu/dstore/document/2512/B%C3%A1lint%20Csaba%20Advanced%20Computer%20Graphics%20Slides.pdf "https://www.inf.elte.hu/dstore/document/2512/b%c3%a1lint%20csaba%20advanced%20computer%20graphics%20slides.pdf")) #ReviewDone
- [CPU to GPU](https://docs.google.com/presentation/d/1p9l_muLm24JNijz-glObRobwMWWbECGRE4g2hdya_PM/edit?usp=sharing](https://docs.google.com/presentation/d/1p9l_muLm24JNijz-glObRobwMWWbECGRE4g2hdya_PM/edit?usp=sharing "https://docs.google.com/presentation/d/1p9l_mulm24jnijz-globrobwmwwbecgre4g2hdya_pm/edit?usp=sharing")) - [[CPU to GPU Notes]] #ReviewDone
- [The RTX Shader Binding Table Three Ways](https://www.willusher.io/graphics/2019/11/20/the-sbt-three-ways/) - [[Shader Binding Table Notes]] #ReviewDone 

#### Monte Carlo Geometry Processing: 
##### Blogs: 
- [Keenan Crane - Monte Carlo Geometry Processing](https://www.cs.cmu.edu/~kmcrane/Projects/MonteCarloGeometryProcessing/index.html)
- [Rohan-Sawhney - MCGP Resources](https://rohan-sawhney.github.io/mcgp-resources/)
	- [Monte Carlo Method for Fluid Simulation](https://riouxld21.github.io/research/publication/MCFluid.pdf)
	- [Velocity-Based Monte Carlo Fluids](https://rsugimoto.net/VelMCFluidsProject/VelMCFluids.pdf)

#### Differential Equations:
##### Blogs/Sites:
- [Wikipedia - Frenet-Serret formulas](https://en.wikipedia.org/wiki/Frenet%E2%80%93Serret_formulas)
- [Wikipedia - Runge-Kutta Methods](https://en.wikipedia.org/wiki/Runge%E2%80%93Kutta_methods) #ToReview
- [Wikipedia - Heun's Method](https://en.wikipedia.org/wiki/Heun%27s_method) #ToReview
- [Wikipedia - Euler Method](https://en.wikipedia.org/wiki/Euler_method) #ToReview 
##### Other Rescources:
- [Julia Package - Differential Equation Solving](https://docs.sciml.ai/DiffEqDocs/stable/) - for CPU implementation
#### Sonar Technology & Simulation:
##### Papers:
- [RAYLAB - Raytracing Program in Underwater Acoustics](https://www.foi.se/rest-api/report/FOI-R--1047--SE) - DiffEq formulas with speed
- [NPL - Speed of Sound in Sea Water - Underlying Physics](http://resource.npl.co.uk/acoustics/techguides/soundseawater/underlying-phys.html)
- [Ray Trace Modeling of Underwater Sound Propagation](https://www.intechopen.com/chapters/45578) - Formulas
- [Propagation Modelling](https://dosits.org/science/advanced-topics/propagation-modeling/)
- [Ocean Acoustics Library](https://oalib-acoustics.org/)
- [Wikipedia - Geometrical Acoustics](https://en.wikipedia.org/wiki/Geometrical_acoustics)
- [Ease - Acoustic Simulation Software](https://www.afmg.eu/en/ease)
- [Sonar Propagation](https://man.fas.org/dod-101/navy/docs/es310/SNR_PROP/snr_prop.htm)- [[Sonar Propagation Notes]] #ReviewDone
- [RTX Implementation - GPU Accelerated Ray-Tracing for Simulation Sound Propagation in Water](https://liu.diva-portal.org/smash/get/diva2:1352170/FULLTEXT01.pdf) #ReviewDone
- [RTX Implementation - BELLHOP](https://oalib-acoustics.org/website_resources/AcousticsToolbox/Bellhop-2010-1.pdf) #ToReview
- [Reverberation](https://dosits.org/science/movement/how-does-sound-move/reverberation/) - [[Reverberation]] #ReviewDone 
- [ASW Systems](https://man.fas.org/dod-101/navy/docs/es310/asw_sys/asw_sys.htm) - [[Anti-submarine Warfare (ASW) Systems]] #ReviewDone
- [Sonar - Noise](https://dosits.org/science/advanced-topics/sonar-equation/sonar-equation-example-active-sonar/) #ReviewDone
- [Principles of Sonar Performance Modelling](https://vdoc.pub/download/principles-of-sonar-performance-modelling-5pken40teq10) #ToReview - Ongoing
- [PC-Based Propagation and Sonar Prediction Models](https://openlibrary.cmre.nato.int/bitstream/handle/20.500.12489/307/SR-240-UU.pdf?sequence=1&isAllowed=y) #ReviewDone - Outdated
- ![[Numerical_methods_in_underwater_aco-1.pdf | Numerical Methods in Underwater Acoustics - Sound Propagation and Backscattering]]
##### Implementations / Projects:
- [Simwave - Python (Finite Difference Method)](https://github.com/hpcsys-lab/simwave?tab=readme-ov-file) #ToReview 
	- [Simwave Paper](https://arxiv.org/pdf/2201.05278) #ToReview
- [j-Wave: Differentiable acoustic simulations in JAX](https://github.com/ucl-bug/jwave) #ToReview
- [WebGPU-base acoustic wave simulator for ultrasound NDT](https://www.ndt.net/article/ecndt2023/papers/ECNDT2023_PAPER_265.pdf)  #ReviewDone
### Other references:

#### Papers:
- [Terrain Rendering using Clipmaps](https://developer.nvidia.com/gpugems/gpugems2/part-i-geometric-complexity/chapter-2-terrain-rendering-using-gpu-based-geometry)
- [Geometry Clipmaps (related to the above link)](https://mikejsavage.co.uk/geometry-clipmaps/)
- [Introduction to SONAR](https://man.fas.org/dod-101/navy/docs/es310/uw_acous/uw_acous.htm) #ToReview
- [Introduction to Naval Weapons Engineering](https://man.fas.org/dod-101/navy/docs/es310/syllabus.htm) #ToReview
- https://apps.dtic.mil/sti/tr/pdf/ADA350893.pdf #ToReview
	- ![[ADA350893.pdf]]
- https://vis.uib.no/wp-content/papercite-data/pdfs/Solteszova12Stylized.pdf #ToReview
	- ![[Solteszova12Stylized.pdf]]
- [Sound Scattering Layers](https://dosits.org/science/movement/sound-scattering-layers/)
#### Other projects:
- [HoloOcean](https://byu-holoocean.github.io/holoocean-docs/v1.0.0/index.html) #ToReview
- [ArcGis](https://storymaps.arcgis.com/stories/e245977def474bdba60952f30576908f)  #ToReview
- [AquaCoustics](http://www.aquacoustics.com/proj_3dmodel.html)  #ToReview
- https://ieeexplore.ieee.org/document/6608090 #ToReview
- [OpenGL Raytracing](https://www.sciencedirect.com/science/article/abs/pii/S1524070320300278) #ToReview
- [OpenGL](https://www.sciencedirect.com/science/article/abs/pii/S0097849317301371) #ToReview