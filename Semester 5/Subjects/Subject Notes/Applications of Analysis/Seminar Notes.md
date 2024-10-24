# Trigonometric formulas
- $\sin(-x) = -\sin(x)$
- $\cos(-x) = \cos(x)$

# Integration Tips & Tricks
$\int f'(g(x)) * g'(x) dx = f(g(x))$

## Integral Transforming
$\int f(x)dx = \int f(g(t)) * g'(t) dt\ |\ t = g^{-1}(x)$ 
### Trigonometric Functions
Mivel $\cos^2(\alpha) = \frac{1}{1+\tan^2(\alpha)}$
- $\sin(x) = \frac{2*\tan\left( \frac{x}{2} \right)}{1+\tan^2\left( \frac{x}{2} \right)} = \frac{2t}{1+t^2}$ 
- $\cos(x) = \frac{1-\tan^2\left( \frac{x}{2} \right)}{1+\tan^2\left( \frac{x}{2} \right)} = \frac{1-t^2}{1+t^2}$ 
*ahol*:
- $t = \tan\left( \frac{x}{2} \right)$ (néha $t=\tan(x)$ is megjelenhet tetszés szerint)
*ekkor* persze:
- $g(t) = 2 \arctan(t) = x$  
- $dx = \frac{2}{1+t^2}$

## Partial Integration 
$(f*g)' = f'*g + f*g' \implies \int (f*g)' =\int f'*g + \int f*g' \implies \int f*g' = f*g - \int f'*g$

## Solving Integrals using Equations

# Common Surfaces

## Triangles
$Ax + By + Cz = D$, **where** $(A,B,C)$ are the give points of the triangle
=> Transform it into an equation with only $D$ => get the actual equation


# Integral Transforms

## Cylindrical Transform
**Base Formulas**:
- $x = r * cos(\phi)$
- $y = r * sin(\phi)$
- $z = z$ 
$g(z,r,\phi) = (x,y,z) = (r * cos(\phi),\ r * sin(\phi),\ z)$
**Determinant** of $g'(r,z,\phi)$ : $det(g'(r,z,\phi))=r$

## Polar Coordinates in Plane
 **Base Formulas**:
- $x = r * \cos(\phi)$
- $y = r*\sin(\phi)$
$g(r,\phi) =(x,y) = (r*\cos(\phi),r*\sin(\phi))$
**Determinant** of $g'(r,\phi)$:  $\det(g'(r,\phi)) = r$

## Polar Coordinates in Space
**Base Formulas**:  
- $x = r * sin(\psi) * cos(\phi)$
- $y = r * sin(\psi) * sin(\phi)$
- $z = r * cos(\psi)$ 
$g(r,\phi,\psi) = (x,y,z) = (r * sin(\psi) * cos(\phi),\ r * sin(\psi) * sin(\phi),\ r * cos(\psi))$
**Determinant** of $g'(r,\phi,\psi)$ : $\det(g'(r,\phi,\psi)) = r^2 * sin(\psi)$  

# Applications of Integrals

## Volume
- $V(E) = \int \int \int_{E}\ 1\ dx\ dy\ dz$
## Mass
**Base formulas**: 
- $m(E) = \int \int \int_E \rho(x,y,z)\ dx\ dy\ dz$ 
- $\rho(x,y,z)$ - density function

## Centre of Mass 
**Base formulas**:  (*Coordinates*)
- $x_{tkp} = 1/m(E) * \int \int \int_E x*\rho(x,y,z)\ dx\ dy\ dz$     
- $y_{tkp} = 1/m(E) * \int \int \int_E y*\rho(x,y,z)\ dx\ dy\ dz$ 
- $z_{tkp} = 1/m(E) * \int \int \int_E z*\rho(x,y,z)\ dx\ dy\ dz$ 
- $\rho(x,y,z)$ - density function
## Inertia
**Base formulas**: 
- $T(E) = \int \int \int_{E}\ \rho(x,y,z) *r^2(x,y,z)\ dx\ dy\ dz$ 
- "Density times Distance squared"
## Surfaces
1. Euler-Monge paraméterezés
2. Felszín menti norma kiszámítása vektoriális szorzattal

| **i**              | **j**              | **k**              |
| ------------------ | ------------------ | ------------------ |
| $\delta_1f(x,y).x$ | $\delta_1f(x,y).y$ | $\delta_1f(x,y).z$ |
| $\delta_2f(x,y).x$ | $\delta_2f(x,y).y$ | $\delta_2f(x,y).z$ |
$$
S = \int \int \lvert\lvert n_{\phi}(u,v) \rvert\rvert_{2} \ du\ dv
$$
**ahol**:
- $\partial_{1}\phi \times \partial_{2}\phi = n_{\phi}$  
### Gauss paraméterezés
Pl. 
$$
\psi(u,v) := (u * \cos(v), u * \sin(v),u)\ ; (u,v) \in [a,b] *[c,d]
$$
### Euler-Monge paraméterezés 
Pl. 
$$
z = f(x,y) 
$$
Azaz egy függvény egy kimeneti komponensének kifejezése a többi komponenssel.

## Fluxus / Surface Integral
- 2-es integrál
- $\phi$ fv. ~ felület megadása (jelenleg 2 paraméterrel), azaz $\phi \in \mathbb{R}^2 \to \mathbb{R}^3$
$$
\int \int < f(\phi(u,v)), n_{\phi}(u,v)>\ du \ dv
$$
**ahol**:
- $\partial_{1}\phi \times \partial_{2}\phi = n_{\phi}$  

## Parametric Integrals
$$
F(a) = \int f(a,x)\ dx
$$
**where**
- $f:V \times U$, where V is an open set
- $V \subset \mathbb{R}^n$  
**if**
- $f \in C$ **then** $f \in R \implies \exists F \in C$ 
- $\exists\partial_{i}f\in C \implies \exists\partial_{i}F = \int \partial_{i}f\ dx$ 
# Implicit function theorem
**Conditions**/**If**:
- $f : R^m \times R^n \to R^n$ 
- $f \in C^1$ 
- $\det \partial_{2} f(a,b) \neq 0$, where $f(a,b) = 0$
**Then**:
- $\exists K(a),K(b)$ hogy ha $\phi:K(a) \to K(b)$, akkor $\forall x \in K(a):$ 
	- $f(x,\phi(x)) = 0$ 
	- $\phi(a) = b$ 
	- $\phi \in C^1$  
	- $\phi'(a) = -[\partial_{2}f(a,b)]^{-1} *\partial_{1}f(a,b)$ 

# Inverse function theorem

# Lagrange-multiplicator
**Legyen**:
- $f:\mathbb{R}^n \to \mathbb{R}$
- $g:\mathbb{R}^n \to \mathbb{R}$ ; $\{ g=0 \}$
**Ekkor**:
$L : \mathbb{R}^n \to \mathbb{R}$
Pl. 
- $f(x,y,z)$; $g(x,y,z)$
- $\lambda\in \mathbb{R}$
- $L(x,y,z) = f(x,y,z) + \lambda*g(x,y,z)$
1. Egyenletrendszer megoldásai:
	- $\partial_{1}L(x,y,z) = 0$
	- $\partial_{2}L(x,y,z) = 0$
	- $g = 0: \ \ g(x,y,z) = 0$
2. Lineáris függetlenség:
	- $g(c_{i})\neq 0\ \ (i =0,\dots)$ 
3. $Q = <L''(x,y,z) * h,h>$, úgy hogy $g(c_{i}) * h = 0 \ \ (h \neq \underline{0})$