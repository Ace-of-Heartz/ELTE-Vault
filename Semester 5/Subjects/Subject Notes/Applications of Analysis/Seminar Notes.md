# Integral Transforms
## Cylindrical Transform
**Base Formulas**:
- $x = r * cos(\phi)$
- $y = r * sin(\phi)$
- $z = z$ 
$g(z,r,\phi) = (x,y,z) = (r * cos(\phi),\ r * sin(\phi),\ z)$
**Determinant** of $g'(r,z,\phi)$ : $det(g'(r,z,\phi))=r$
## Polar Coordinates in Space
**Base Formulas**:  
- $x = r * sin(\psi) * cos(\phi)$
- $y = r * sin(\psi) * sin(\phi)$
- $z = r * cos(\psi)$ 
$g(r,\phi,\psi) = (x,y,z) = (r * sin(\psi) * cos(\phi),\ r * sin(\psi) * sin(\phi),\ r * cos(\psi))$
**Determinant** of $g'(r,\phi,\psi)$ : $det(g'(r,\phi,\psi)) = r^2 * sin(\psi)$  

# Applications of Integrals
## Mass
**Base formulas**: 
- $m(E) = \int \int \int_E \rho(x,y,z)$ 

## Centre of Mass 
**Base formulas**:  (*Coordinates*)
- $x_{tkp} = 1/m(E) * \int \int \int_E x*\rho(x,y,z)\ dx\ dy\ dz$     
- $y_{tkp} = 1/m(E) * \int \int \int_E y*\rho(x,y,z)\ dx\ dy\ dz$ 
- $z_{tkp} = 1/m(E) * \int \int \int_E z*\rho(x,y,z)\ dx\ dy\ dz$ 
## Surfaces
1. Euler-Monge paraméterezés
2. Felszín menti norma kiszámítása vektoriális szorzattal
	- 

| i                  | j                  | k                  |
| ------------------ | ------------------ | ------------------ |
| $\delta_1f(x,y).x$ | $\delta_1f(x,y).y$ | $\delta_1f(x,y).z$ |
| $\delta_2f(x,y).x$ | $\delta_2f(x,y).y$ | $\delta_2f(x,y).z$ |
 
### Euler-Monge paraméterezés 
