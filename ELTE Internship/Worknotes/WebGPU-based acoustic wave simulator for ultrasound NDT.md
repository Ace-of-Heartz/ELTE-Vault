# Overview:
## Goals of the Paper:
- Exploration of the acceleration capabilities of the WebGPU API by implementing the software described in the title itself.
- Exploration of parallel optimization in a GPU for FWI algorithms

## FWI vs. Delay-and-Sum:
**NDT - Non-Destructive Testing:**
- Quality control tool.
- Ultrasonic method is the mostly used technique
- Capable of allowing safe identification and monitoring of failures in aggressive subsea environments.  
- **FWI - Full Waveform Inversion:** 
	- Way of estimating the velocity model of inspection areas by confronting the acquired information obtained by the NDT system with theoretical simulated data.
	- **Highly computationally demanding**
	- Has been gaining traction recently
-  **SAFT & TFM**
	- Based on **delay-and-sum**: signals received by different sensors in an array are temporally aligned to compensate for different times of propagation and then summed up.
	- Produces reasonable estimates of the internal reflectivity of the specimen <mark style="background: #FF5582A6;">if the propagation is straightforward and phenomena such as refraction, diffraction, and multiple reflections are negligible</mark>

## WebGPU:
- Allows efficient and fast mapping to native GPU APIs.
- Potential for huge-cross platform access through a web browser.
- Allows the programmers low-level access to GPUs.

## Acoustic Wave Simulations:
### Two-dimensional acoustic wave equation: 
- $(\delta^2 p)/(\delta t^2) = c^2\Delta p + s$ 
	- $p = p(x,y,t)$ - pressure field
	- $c = c(x,y)$ - medium wave velocity propagation
	- $s = s(x,y,t)$ - pressure source field
	- $\Delta$ - Laplace-operator: 
		- $\Delta = \delta^2/\delta x + \delta^2/\delta y + \delta^2 / \delta z$
### Solution of Acoustic Wave Equation:
This can be determined by a numerical solution using the [[Finite Difference Method | finite difference method ]] discretization**. 
Explicit finite difference equation: (assuming temporal and spatial second-order approximation)
$p^{t+\Delta t}_{i,j} = -p^{t-\Delta t}_{i,j} + 2p^{t}_{i,j} + C^2(p^{t}_{i+1,j} - 2p^{t}_{i,j} + p^{t}_{i-1,j} + p^{t}_{i,j+1} - 2p^{t}_{i,j} + p^{t}_{i,j-1}) + s^t$
with $C = c*\Delta t/ h$ (**Courant number**)
- t - actual time
- i, j - grid point indexes in directions x and y
- $\Delta t, h$ - time and spatial discretizations, with $\Delta x = \Delta y = h$ 
Accurate results, but conditionally stable (stability depends on the Courant number)

## Implementation and Results:
- wgpu-py wrapper was used (Python-based WebGPU wrapper)
"The simulator was implemented by
parallelizing the pressure intensity calculations in a finite difference method."
"...GPU threads simultaneously calculate <mark style="background: #FF5582A6;">the pressure intensities for each simulation time frame for each grid pixel</mark>"

GPUs used in the testing:
- NVIDIA GeForce RTX 3060
- Intel(R) HD Graphics 530 (SKL GT2)

For more precise information about the results, check the paper!

# Insights:
While the topic of the paper is very interesting, the implementation and the technique used won't be of much use for the project aside from the relation of ultrasonic waves and sonar propagation.

# References: 

## The Paper:
![[ECNDT2023_PAPER_265.pdf]]

## Other:
- [Full Waveform Inversion for NDT using ultrasonic linear arrays](https://www.ndt.net/search/docs.php3?id=28120)