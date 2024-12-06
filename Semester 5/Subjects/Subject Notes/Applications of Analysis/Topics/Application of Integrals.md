# Applications of Integrals

## Area (*Terület*)
**Base formulas**:
- $t(E) = \int \int_{E} 1\ dx \ dy$

## Geometric Center (*Súlypont*)
**Base formulas**: (*Coordinates*)
- $x_{s} = \frac{1}{t(E)} \int \int_{E} x\ dx\ dy$
- $y_{s} = \frac{1}{t(E)} \int \int_{E} y\ dx \ dy$

## Volume (*Térfogat*)
**Base formulas**:
- $V(E) = \int \int \int_{E}\ 1\ dx\ dy\ dz$

## Mass (*Tömeg*)
**Base formulas**: 
- $m(E) = \int \int \int_E \rho(x,y,z)\ dx\ dy\ dz$ 
- $\rho(x,y,z)$ - density function

## Center of Mass (*Tömeg középpont*)
**Base formulas**:  (*Coordinates*)
- $x_{tkp} = 1/m(E) * \int \int \int_E x*\rho(x,y,z)\ dx\ dy\ dz$     
- $y_{tkp} = 1/m(E) * \int \int \int_E y*\rho(x,y,z)\ dx\ dy\ dz$ 
- $z_{tkp} = 1/m(E) * \int \int \int_E z*\rho(x,y,z)\ dx\ dy\ dz$ 
- $\rho(x,y,z)$ - density function

## Moment of Inertia (*Tehetetlenségi nyomaték*)
**Base formulas**: 
- $T(E) = \int \int \int_{E}\ \rho(x,y,z) *r^2(x,y,z)\ dx\ dy\ dz$ 
- "Density times Distance squared"

## Surface (*Felszín*)
1. Euler-Monge paraméterezés
2. Felszín menti norma kiszámítása vektoriális szorzattal

| **i**              | **j**              | **k**              |
| ------------------ | ------------------ | ------------------ |
| $\delta_1f(x,y).x$ | $\delta_1f(x,y).y$ | $\delta_1f(x,y).z$ |
| $\delta_2f(x,y).x$ | $\delta_2f(x,y).y$ | $\delta_2f(x,y).z$ |

$$
S = \int \int_{E} \lvert\lvert n_{\phi}(u,v) \rvert\rvert_{2} \ du\ dv
$$

**ahol**:
- $\partial_{1}\phi \times \partial_{2}\phi = n_{\phi}$  
### Gauss parametrization
Pl. 
$$
\psi(u,v) := (u * \cos(v), u * \sin(v),u)\ ; (u,v) \in [a,b] *[c,d]
$$
### Euler-Monge parametrization  
Pl. 
$$
z = f(x,y) 
$$
Azaz egy függvény egy kimeneti komponensének kifejezése a többi komponenssel.

## Fluxus / Surface Integral (*Fluxus*)
- 2-es integrál
- $\phi$ fv. ~ felület megadása (jelenleg 2 paraméterrel), azaz $\phi \in \mathbb{R}^2 \to \mathbb{R}^3$
$$
\int \int < f(\phi(u,v)), n_{\phi}(u,v)>\ du \ dv
$$
**ahol**:
- $\partial_{1}\phi \times \partial_{2}\phi = n_{\phi}$  

## Parametric Integrals (*Parametrikus integrál*)
$$
F(a) = \int f(a,x)\ dx
$$
**where**
- $f:V \times U$, where V is an open set
- $V \subset \mathbb{R}^n$  
**if**
- $f \in C$ **then** $f \in R \implies \exists F \in C$ 
- $\exists\partial_{i}f\in C \implies \exists\partial_{i}F = \int \partial_{i}f\ dx$ 