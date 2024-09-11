# Transmission Loss (TL)
To a rough degree, it can be predicted solely from the following factors:
- [[Sonar Propagation Notes#Transmission Loss (TL)#Range|Range]]
- Frequency
## Range
**Spherical spreading loss function:**
	$TL_{spherical} = -10 * Log\{I(R) / I(1 m)\} = -10 * Log(1/R^2) = 20*Log(R)$
**Cylindrical spreading loss:**
This occurs because typcially the accustic energy will be confined between the seafloor and the surface of the water.
	$SPL(R_2) = SPL(R_1) - 10*Log(R_2/R_1)$
We **cannot** assume that $R_1 = 1$ like in the Spherical spreading loss, because the range of our sonar might be lower than it's distance from the seafloor, in which case the above loss function should be used.
Because of this, we will transition into this spreading loss function when we reach the halfway of the [[Sonar Propagation Notes|waterdepth]].
**Notes:**
- ^1 the average ocean depth is around 2000 m

**Absorption/Scattering:**
Dependence on range will be identical to [Bougher's law](https://en.wikipedia.org/wiki/Beer%E2%80%93Lambert_law) in decibel form:
	$TL_{abs} = -10*Log(e^{-bR}) = (10 b) R$
	where b is the "extinction coefficient"
 A factor of 10 and a unit conversion into km is absorbed in the definition of the absorption coefficient (b/100), therefore:
		 $TL_{abs} = a*R$ 
The absorption coefficient has a strong frequency dependency, which results in much greater losses at higher frequency.
Formula:
	a = $0.0036f^2/(f^2 + 3600) +3.2*10^{-7}f^2$
	where f is in kHz, and the result for a is in dB/km

# Transmission loss anomaly
Formula:
	$TL = 10 *Log(R) + 30 + aR + A$ 

# Propagation paths
## Sound velocity profile (SVP)
Variations in the speed of sound occur because of: 
- depth (also most important factor)
- salinity

## Vertical regions of water
- Surface / Seasonal layer
	- profile changes depending on time of day and depending on seasons
- Main thermocline
- Deep isothermal layer

# Ray tracing
- negative gradient of propagation speed => rays deflect downward
- positive gradient of propagation speed => rays bend upwards
## Surface duct
- **occurs when**: rays reach the surface
- **effect**: rays are reflected downwards, same process begins (with energy loss of course)
	- effectively the rays are trapped in a relatively small layer below the surface
## Layer depth (LD)
A positive gradient over a negative gradient.
The boundary at which rays split.
Maximum sound velocity
- above layer: produces a **surface duct**
- below layer: rays are deflected downward

## Shadow zone
Location below the layer depth, where the rays never reach
	Optimum depth to operate = *best depth* **(BD)**

## Special cases of propagation:
### A) Sound channel
- **occurs when**: the negative gradient is over the positive gradient
- **effect:** sound channel is created - rays confined in a small region
- sound channel won't work for rays that begin at the surface, instead <mark style="background: #ABF7F7A6;">the source must be located around the axis</mark>
### B):
- **phenomenon**: no sound rays can reach the bottom without being deflected upwards by the positive gradient in the isothermal layer
- requires min. 200 m depth excess


**Depth excess:** distance from the lower boundary of the sound channel to the bottom 

## Convergence zones:
- **occurs when**: the sound rays are returned to near the surface
- **effect**: the sound pressure is increased, forming **convergence zones (CZ)**
- tends to be at large distances (20-30 nm from source)
- multiple convergence zones are possible at regular intervals

## Bottom bounce: 
- **occurs when**: the sound is strongly reflected from the ocean floor
- **effect**: tends to converge near the surface => results in a reduced transmission loss
- typically occurs at angles more than 30°
- depends on the type/condition of the ocean floor

# Transmission loss curves
- certain ranges exist where TL goes down due to, for example CZ or bottom bounce <=> geometrical TLs don't show these

If SNR < DT, then detection is possible.
**Solving the range:**
	Passive case: we define figure of merit (FOM):
		$FOM_{passive} SL + DI - NL - DT$ => FOM > TL becomes the detection criterion
	Interpretation:
		 FOM = maximum transmission loss of the system, at which it can still detect the target (50% of the time) 

From this, we can plot FOM (if it's known) on the TL curve. If FOM > TL => means detectable.


# Complications with active systems
1. ???
2. transmission loss is incurred twice (back and forth)
	- **1. Solution:** Using a separate curve with twice the TL vs. range
	- **2. and preferred Solution**: use one half of the FOM
	- AKA:  $FOM > 2*TL$ 