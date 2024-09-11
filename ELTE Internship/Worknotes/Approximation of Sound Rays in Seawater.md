# Overview:
- Demo is done in Julia

## Questions:
- Waterlayer representation
	- Information about salinity, temperature, depth?
		- We need these to calculate the speed of sound in a certain layer
	- The actual representation of these layer?
		- Implicit layers? 
	- Speed and velocity are necessary to approximate the propagation path of a ray
- Input data: what kind of information will we have about our surroundings, and what kind of representation will we use for these?
## Notes:
According to my understanding, to properly simulate the propagation of sound, we need to have the following initial data for the "initial value problem": 
- Initial depth
- Initial angle of ray
- Initial speed
To calculate the individual steps we need to be able to compute and/or have data about the following:
- ~~Change of angle of ray depending on the distance travelled (AKA current speed)~~ -> After thinking it through, this method would be wrong follow, because the temperature and other varying factors are necessary to examine for the simulation, and thus the only using distance for our calculations would be completely wrong.
OR 
- Speed of sound in a given depth
- Velocity of sound in a given depth

For the latter two, the [following research paper](https://liu.diva-portal.org/smash/get/diva2:1352170/FULLTEXT01.pdf) gives insight into the process of their calculation. 
However, the project seems to have used predefined/pre-calculated values for these variables, which were then associated with water layers used in their simulation.
In our project, this would mean we would either need to be able to access a predefined values for these variables as well, or calculate the speed of sound in a given depth using either Mackenzie's or another, more accurate formula.

[Speed of sound in sea water](http://resource.npl.co.uk/acoustics/techguides/soundseawater/underlying-phys.html)
