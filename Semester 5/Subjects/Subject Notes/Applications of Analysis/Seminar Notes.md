# Trigonometric formulas
- $\sin(-x) = -\sin(x)$
- $\cos(-x) = \cos(x)$

# Integration Tips & Tricks
$\int f'(g(x)) * g'(x) dx = f(g(x))$

## Integral Substitution 
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
1. Transform it into an equation with only $D$
2. Solve the equation for $D$


# Integral Transforms

## Cylindrical Transform
**Base Formulas**:
- $x = r * cos(\phi)$
- $y = r * sin(\phi)$
- $z = z$ 

$g(z,r,\phi) = (x,y,z) = (r * cos(\phi),\ r * sin(\phi),\ z)$

**Determinant** of $g'(r,z,\phi)$ : $\det(g'(r,z,\phi))=r$

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
## Finding the implicit function without the theorem
1. Try to get the other components using the designated component
2. Try to solve the equations and get solutions for the designated component
3. If the solutions don't make up an open set, then the implicit function doesn't exist
# Inverse function theorem
**Conditions**/**If**: 
- $f \in C^1$ 
- $\det f'(z) \neq 0, where\ z\in Df$  
- $f(z) = a$ 

**Then**:
- $\exists K(z), V\ open\ set: F = (f|K(z))^{-1}$
- $F \in C^{1}$
- $F'(a) = f^{-1}(z)$
# Conditional extreme values
## Lagrange-multiplicator
**Let**:
- $f:\mathbb{R}^n \to \mathbb{R}$
- $g:\mathbb{R}^n \to \mathbb{R}$ ; $\{ g=0 \}$

**Then**:
$L : \mathbb{R}^n \to \mathbb{R}$
Pl. 
- $f(x,y,z)$; $g(x,y,z)$
- $\lambda\in \mathbb{R}$
- $L(x,y,z) = f(x,y,z) + \lambda*g(x,y,z)$
1. Get the solutions of the systems of equations:
	- $\partial_{1}L(x,y,z) = 0$
	- $\partial_{2}L(x,y,z) = 0$
	- $g = 0: \ \ g(x,y,z) = 0$
2. Check for linear independence:
	- $g(c_{i})\neq 0\ \ (i =0,\dots)$ 
3. $Q(h) = <L''(x,y,z) * h,h>$, so that  $g(c_{i}) * h = 0 \ \ (h \neq \underline{0})$

## Conditional absolute extreme values
**If**: 
- $\{ g = 0 \}$ is compact (closed and limited)
- $f \in C$

**Then**:
- we can use Weierstrass's Theorem: $\exists\ abs. max ,\ abs. min$  => we just calculate  $f(c_{i})$ ($i = 1,\dots$)

# Differential Equations 
## Ordinary differential equations (ODEs)
### Separable ODE.:

1. **Check for separability**:
	- $y'(x) = g(x) * h(y(x))$ , where:
		- $h : J \to \mathbb{R} / \{0  \}$, where $J$ is an open set *and* $0 \notin R_{h}$
		- $g: I \to \mathbb{R}$ where $I$ is an open set  
	- Make differential equation separable if not explicitly separable using the following steps *v1*. :
		1. $y'(x) = f(x * a + y(x) * b + c)$  
		2. $z(x) = x*a + y(x) * b + c$ => $z'(x) = a + y'(x) * b$ => $y'(x) = \frac{z'(x) - a}{b}$
		3. $z'(x) = a + b * f(z(x)) = 1*(a + b*f(z(x)))$
	- Make differential equation separable if not explicitly separable using the following steps *v2*. :
		1. $y'(x) = f\left( \frac{a_{1}x + b_{1}y(x)+ c_{1}}{a_{2}x + b_{2}y(x) + c_{2}} \right)$, ahol $a_{1},a_{2},b_{1},b_{2},c_{1},c_{2} \in \mathbb{R}: a_{1}b_{2} - b_{1}a_{2} = 0$ vagy $a_{1}b_{2}-b_{1}a_{2} \neq 0$  
		2. Ha $a_{1}b_{2} - b_{1}a_{2} = \det \begin{bmatrix}a_{1} &b_{1} \\ a_{2} & b_{2}\end{bmatrix} = 0$  
			1. Akkor alkalmas $\lambda,\mu \in \mathbb{R}$  számokkal:
				- $a_{1} = \lambda a_{2}$ és $b_{1}=\lambda b_{2}$
				-  vagy
				- $a_{2}=\mu a_{1}$ és $b_{2}=\mu b_{1}$ 
			2. $f\left( \frac{a_{1}x + b_{1}y(x)+c_{1}}{a_{2}x+b_{2}y(x) + c_{2}} \right) =f\left( \frac{\lambda(a_{2}x + b_{2}y(x)) + c_{1}}{a_{2}x + b_{2}y(x)  +c_{2}} \right)$ vagy (ld. $\mu$-vel való helyettesítés)
			3. Ha $b_{2}=0$ vagy $b_{1} = 0$, akkor trivi.
			4. Ha nem: (most $z \equiv \psi$)
				1. $\psi(x) = a_{2}x + b_{2}\phi(x)$ vagy (ld. $\mu$)
				2. $$\psi'(x) = a_{2}+b_{2}\phi'(x) = a_{2}+b_{2}f\left( \frac{a_{1}x + b_{1}y(x)+c_{1}}{a_{2}x+b_{2}y(x) + c_{2}} \right) = a_{2}+b_{2}f\left( \frac{\lambda \psi(x)+c_{1}}{\psi(x)+c_{2}} \right) =:h(\psi(x))$$
				3. Azaz $\psi$ a $z'=h\ o\ z$ autonom diff. egy. megoldása
		 1.  Ha nem:
			 1. $a_{1}x+b_{1}y+c_{1} = 0$ és $a_{2}x+b_{2}y+c_{2}=0$ egyenletrendszernek pontosan 1 megoldása van: $x=\xi$ és $y=\eta$
			 2. Ha: $x=:u+\xi$ és $y=\nu+\eta$
				 1. $\psi(u):=\phi(u+\xi)-\eta$ ($u \in D_{\phi}-\xi$) =>
				 2. $\psi'(u) = \phi'(u+\xi)= f\left( \frac{a_{1}(u+\xi)+b_{1}\phi(u+\xi)+c_{1}}{a_{2}(u+\xi)+b_{2}\phi(u+\xi)+c_{2}} \right)=\dots=f\left( \frac{a_{1}+b_{1}\left( \frac{\psi(u)}{u} \right)}{a_{2}+b_{2}\left( \frac{\psi(u)}{u} \right)} \right)=:h\left( \frac{\psi(u)}{u} \right)$
				 3. Azaz $z'(x) = h\left( \frac{z(x)}{x} \right)$ ($x\in D_{y}-\xi$) megoldása $\psi$ 
1. **Check for interval**: 
	 - If we have a *starting value*: use the open interval that includes this *starting value* $y(\tau ) = \xi$ 
	 - If we **don't** have a *starting value*: we must continue separately with all open intervals
2.  **Algorithm**: 
	1. $y'(x) = \frac{dy}{dx} = g(x) * h(y(x))$ és $h(y) \neq 0$ és $\dots$
		-  keressük meg az intervallumokat (aszimptoták) 
	2. $\int \frac{1}{h(y)}\ dy = \int g(x)\ dz$ 
	3. Integrate both sides separately
	4. $H(y) + \tilde{c} = G(x) + c$, where we can assume that $\tilde{c} = 0$ 
	5. Calculate the value of $c$ using the *starting value*
	6. $y(x) = H^{-1}(*{G(x) + c})$ - bring the equation to an explicit solution
	7. $x \in K_{\delta}(\tau)$, where $\delta$ is sufficient (*megfelelő*)

#### Notes:
When $z=a*x + b*y + c$, we can say $z \lambda(a*x+b*y+c)$ as well in case we need to remove any additions or subtractions.
Homogén fokszámú diff. egyenlet: $y=u*x$ alakkal kell dolgozni:
- $u(x) = \frac{x}{y(x)}$
- $u'(x) = \frac{y(x) - x*y'(x)}{y^2(x)}$ 

### Exact ODE.:
ODE formája: $P(x,y)\ dx + Q(x,y)\ dy = 0 \iff y'(x) =\frac{dy}{dx} =-\frac{P(x,y)}{Q(x,y)} =-\frac{P(x,y(x))}{Q(x,y(x))}$ 
**Szükséges feltétel**: $\partial_{2}P(x,y) = \partial_{1}(Q(x,y))$ ! (*[[Analysis 3 Exam#Young tétel|Young Tétel]]*)

1. $F \in \mathbb{R}^{2} \to \mathbb{R}; F\in D; F' = (\partial_{1}F,\partial_{2}F) = (P,Q)$ fv. keresése, azaz:
	- $\partial_{1}F(x,y) = P(x,y)$
	- $\partial_{2}F(x,y) = Q(x,y)$
2. 1. Feltétel alapján: $F(x,y) = \int P(x)\ dx = F_{1}(x,y) + c(y)$, ahol:
	- $c:\mathbb{R}\to \mathbb{R}$
	- $c \in D$
3. 2. Feltétel alapján: 
	- $\partial_{2}F(x,y) = Q(x,y)$
	- $\partial_{2}(F_{1}(x,y) +c(y)) = \partial_{2}(F_{1}(x,y)) + c'(y)$ 
	- és $\partial_{2}F(x,y) = \partial_{2}(F_{1}(x,y) + c(y)) \implies Q(x,y) = \partial_{2}(F_{1}(x,y)) + c'(y)$ 
4. $c'(y) = Q(x,y) -\partial_{2}(F_{1}(x,y)) \implies c(y) = \int c'(y)\ dy$  
5. $F(x,y)$ felírása ($F(x,y) = F_{1}(x,y)+c(y)$) 

**Megoldás**:
- $\exists k \in \mathbb{R}: F(x,y(x)) = k \iff c(x) + F_{1}(x,y(x)) = \alpha$, ahol:
	- $\alpha \in \mathbb{R}$
	- $x \in K_{\delta}(\tau)$, where $\delta > 0$ is sufficient (*alkalmas*)
	- és ha  $\alpha = \xi$ -> *k.é.p.* kielégítő fv.: $x = \tau$ és $y = \xi$ most (behelyettesítés)

#### Multiplikátor Módszer
**Mikor kell**: ha $\partial_{2}P(x,y) \neq \partial_{1}Q(x,y)$ 

**Lépések**:
- $Pdx =Qdy \ | *m (\neq 0) \implies$ $P*m\ dx = Q* m\ dy \implies$ $\partial_{2}(P*m) = \partial_{1}(Q*m) \implies$ $m* \partial_{2}P + P* \partial_{2}m = m*\partial_{1}Q+Q*\partial_{1}m$ 
-  $(\partial_{2}P - \partial_{1}Q)*m =Q*\partial_{1}m - P*\partial_{2}m$
-  Ha $m$ csak $x$-től függő: $\implies (\partial_{2}P -\partial_{1}Q)*m = Q*m' \implies m(\dots) = \frac{\partial_{2}P(x,y)-\partial_{1}Q(x,y)}{Q(x,y)}$ (*csak x-től szabad függenie*)
- Ha $m$ csak $y$-től függő: $\implies (\partial_{2}P - \partial_{1}Q)m = -P*m' \implies m(\dots)=-\frac{\partial_{2}P(x,y) - \partial_{1} Q(x,y)}{P(x,y)}$ (*csak y-tól szabad függenie*)
- Ekkor pl.: $M = \int m$
- $\dots$ és a multiplikátorunk: $\mu(x,y) = e^{M(\dots)}$ 
- Ezzel a $\mu$ multiplikátorral szorozzuk be $P$ és $Q$ fv.-eket -> **Egzakt ODE-t kapunk!** 
##### Notes:
$m(x) = g(x)$ => $M(x) =G(x)$ => $e^{G(x)}$ lesz a multiplikátor fv. 
### Lineáris D.E.

**Homogén megoldások**:
- *Általános levezetés*: 
	1. $y'(x) + g(x) * y(x) = \ln(x)$ 
	2. $y'(x) + g(x) * y(x) = 0$ 
	3. $\frac{y'(x)}{y(x)} = - g(x)$
	4. $\ln| y(x)| = -\int g(x)\ dx$
	5. $|y(x)| = e^{-\int g(x)\ dx}$ 
	6. $y(x) =\pm e^{-\int g(x)\ dx} =\pm e^{G(x)+c}$, ahol $G \in \int g \neq \emptyset$ 
	7. $\dots=e^c * e^{G(x)} = \alpha*e^{G(x)}$  
- **Tömör forma**: $y_{h}(x)=\alpha*e^{-\int g(x)dx} = \dots = \alpha * h(x)$

**Partikuláris megoldás az inhomogén egyenlethez**:
1. $\exists y_{p}(x) = \beta(x) * {h(x)}$ ~ *Inhomogén megoldás*
2. **Ekkor**: $y_p'(x) = f(x,y_{p}(x))$ (D.E.) és a fenti alapján fejezzük ki $\beta'(x)$-et
	- **Fontos**: $\beta(x)$ részeknek mindig ki kell esniük -> ha nem, baj van!
3. $\beta'(x) = g(x)$ formájú egyenletet kapunk
4. Határozzuk meg $\beta(x)$-t (*integrálás*). 
	- *Megjegyzés*: Integrálás során kapott $c\in \mathbb{R}$ konstanst válasszuk meg a legegyszerűbbnek 
5. Helyettesítsük be $y_{p}(x)$-be $\beta(x)$ értékét.

**Összes megoldás**:
- $y(x) = y_{h}(x) + y_{p}(x)$ = $\alpha* h(x) + y_{p}(x)$ 
- Ekkor még $\alpha$ ismeretlen.

**Kezdeti feltétel**:
Használjuk fel a kezdeti értékünket:
- $y(\tau) = \xi$ alapján: $y(\tau) = \alpha*h(\tau) + y_{p}(\tau) = \xi \implies \alpha := \frac{\xi - y_{p}(\tau)}{h(\tau)}$  

**K.É.P. megoldása**: 
Írjuk fel $y(x)$-et az előbb kapott $\alpha$ értékével.
+ Írjuk fel $x$ legbővebb halmazát ($D_{y}$)

### Lineáris D.E. rendszerek

#### Kezdet:
- $\begin{matrix} y_{1}(x) = \dots \\ y_{2}(x) = \dots \\ \dots \\ y_{n}(x) = \dots \end{matrix}$ egyenletek
- **Kezdeti értékek**: $y_{1}(\tau) = \xi_{1}$, $y_{2}(\tau) = \xi_{2}$, $\dots$, $y_{n}(\tau) =\xi_{n}$ 
- **Legyen**: 
	- $y(x) =  \left(\begin{matrix}y_{1}(x) \\y_{2}(x) \\ \dots \\ y_{n}(x) \end{matrix} \right)$ $x\in D_{y}$ vektorfv.
	- $A:= \begin{bmatrix} 1 & 2 \\ 2 & 1\end{bmatrix}$
	- $b(x) = \left(\begin{matrix} g_{1}(x) \\ g_{2}(x) \\ \dots \\ g_{n}(x) \end{matrix}\right)$ , ahol $g_{i}(x)$ a $y_{i}(x)$ csak x-et tartalmazó része
- **Így**: $y'(x) = A*y(x) + b(x)$ , ahol $x \in D_{y} = I$  

#### Algo.:
1. Keressük meg $A$ *sajátértékeit*: $\det(A - \lambda I)$ 
2. Diszkrimináns alapján $\dots$
	- Ha $D > 0$ azaz $\lambda_{i} \neq \lambda_{j},u.h.\ j\neq i$
		1. Keressük meg $A$ *sajátvektorjait*:  $A * \begin{bmatrix}a_{1} \\ a_{2} \\ \dots \\ a_{n} \end{bmatrix} = \lambda_{} * \begin{bmatrix} a_{1} \\ a_{2}\\ \dots \\ a_{n}\end{bmatrix}$ vagy $(A-\lambda I) * s_{i} = 0$
		2. Lin. egyenlet rendszer megoldás -> Válasszunk egy tetsz. jó megoldást $s_{i}$-hez! 
		3. **Valós alaprendszer**:
			-  $\phi_{1}(x) = e^{\lambda_{1}x}*s_{1}$
			- $\phi_{2}(x) = e^{\lambda_{2}x}*s_{2}$
			- $\dots$
			- $\phi_{n}(x) = e^{\lambda_{n}x}*s_{n}$
			- és: $\Phi(x) := [\phi_{1}(x)\ \phi_{2}(x)\ \dots\ \phi_{n}(x)]$ - *alapmátrix*
	- Ha $D = 0$, azaz $\lambda_{i} = \lambda_{j}$,u.h. $j \neq i$ valamilyen $j,i$-re
		1. Keressük meg $\lambda_{i}$ sajátvektorját az előző módon 
		2. Alkalmazzunk perturbációt $\lambda_{j}$-hez tartozó sajátvektor meghatározásához (így lesz független a két s.v.) 
		3. $A*s_{j} = \lambda_{j}*s_{j} + s_{i}$ => $s_{i}$ legyen valami egyszerű
		4. **Valós alaprendszer**:
			- $\phi_{i}(x) = e^{\lambda_{i}x}* s_{i}$
			- $\phi_{j}(x) = e^{\lambda_{j}x} * (s_{j} + x*s_{i})$
			- Többi hasonlóan az előző esethez.
	- Ha $D < 0$, azaz $\lambda_{i}, \lambda_{j}$ két konjugált komplex szám
		1. $s_{i}$ hasonlóan meghatározva, csak most elemei $\in \mathbb{C}$ 
		2. $s_{j} := \bar{s_{i}}$
		3. **Valós alaprendszer**: 
			- $\phi_{i}(x) = \mathrm{Re}(e^{\lambda_{i}x} * s_ {i})$
			- $\phi_{j}(x) = \mathrm{Im}(e^{\lambda_{i}x} * s_{i})$
		- ahol:
			- $e^{\mathrm{Im}(\lambda_{i})x} =\cos(x) + i\sin(x)$
1. **Homogén lineáris D.E.R megoldásai** $y'(x) = A*y(x)$ ahol $x \in \mathbb{R}$
	- $y_{h}(x) = \alpha * \phi_{1}(x) + \beta*\phi_{2}(x) + \dots +\dots \zeta*\phi_{n}(x) = \Phi(x) * \left(\begin{matrix}\alpha \\ \beta \\ \dots \\ \zeta \end{matrix}\right)$
	- $\alpha,\beta,\dots,\zeta \in \mathbb{R}, x\in \mathbb{R}$
2. **Partikuláris megoldás megadása** (*állandók variálása*)
	- $\exists y_{p}(x) = \Phi(x) * \left( \begin{matrix}\alpha(x) \\ \beta(x) \\ \dots \\ \zeta(x)\end{matrix}\right)$, ahol $\left( \begin{matrix}\alpha(x) \\ \beta(x) \\ \dots \\ \zeta(x)\end{matrix}\right) =: c(x)$
	- **ahol**: $\Phi(x) *\left( \begin{matrix}\alpha'(x) \\ \beta'(x) \\ \dots \\ \zeta'(x)\end{matrix}\right) = b(x)$ => $c'(x) = \Phi^{-1}(x) * b(x)$, ahol $b(x)$ lásd feljebb!
	- **Fejezzük ki** $c'(x)$-et, majd írjuk fel az integrálokat! (Azaz számítsuk ki $c(x)$-et)
		- **Fontos**: a konstans $c$-ket válasszuk meg a legegyszerűbbnek (pl. 0)
	- **Fejezzük ki** $y_{p}(x) = \Phi(x)*c(x)$-et 
3. **Összes megoldás**
	- $y(x) = y_{h}(x) + y_{p}(x)$
	- Ebben még vannak ismeretlen együtthatók
4. **Kezdeti kikötés**
	1. $y(\tau) = \left(\begin{matrix}\xi_{1} \\ \xi_{2} \\ \dots \\ \xi_{n}\end{matrix} \right) = \dots$ => határozzuk meg az ismeretlen együtthatókat! 
5. **K.É.P. probléma megoldása** (felírás) + $x$ legbővebb halmaza

### Bernoulli-típusú D.E.
#### Kezdet: 
- $\emptyset = I \subseteq \mathbb{R}$ nyílt int.
- $g,h: I \to \mathbb{R}$ folytonosak
- $y'(x) + g(x)*y(x) = g(x)*y^\alpha(x)$ ($x \in D_{y} \subset I$), ahol $\alpha \in \mathbb{R}/\{ 1 \}$

#### Algo.: 
**Ötlet**: Alakítsuk lineáris. D.E-re 
1. $y'(x) * y^{-\alpha}(x) + g(x) * y^{1-\alpha}(x)= h(x)$
2. **Legyen**: $z(x) = y^{1-\alpha}(x)$ 
3. **Ekkor**: $z'(x) =(1-\alpha) * y^{-\alpha} * y'(x)$
4. **Behelyettesítve**: $\frac{z'(x)}{1-\alpha} + g(x) * z(x) = h(x)$
- Ez már *lineáris differenciál egyenlet* 

### Magasabb rendű D.E.

#### Homogén eset
##### Kezdet 
$a_{n}y^{(n)}+a_{n-1}y^{(n-1)}+\dots+a_{1}y' + a_{0}y = 0$ ~ (nem kell mindegyik derivált)
**Ötlet**: $y(x) = e^{\lambda x}$ alakban keresése
1. $a_{n}(e^{\lambda x})^{(n)}+ a_{n-1}(e^{\lambda x})^{(n-1)} + \dots + a_{1}(e^{\lambda x})^{(1)} + a_{0}(e^{\lambda x})^{(0)} = 0$
2.  $a_{n}\lambda^ne^{\lambda x} + a_{n-1}\lambda^{n-1}e^{\lambda x} + \dots + a_{1}\lambda e^{\lambda x} + a_{0}e^{\lambda x}$ $|\ \  /e^{\lambda x}$
3. $a_{n}\lambda^n + a_{n-1}\lambda^{n-1} + \dots + a_{1}\lambda + a_{0}$ 
##### Algo.: 
1. Karakterisztikus egyenlet megoldása: $\lambda_{i}$ értékeket megkapjuk
2. Ha $D > 0$: ($\lambda_{i} \neq \lambda_{j}$)
	1. **Valós alaprendszer**:
		- $y_{n}(x) = e^{\lambda_{n}x}$
		-  $y_{n-1}(x) = e^{\lambda_{n-1}x}$ 
		- $\dots$
		-  $y_{2}(x) = e^{\lambda_{2}x}$
		-  $y_{1}(x) = e^{\lambda_{1}x}$
2. Ha $D = 0$: ($\lambda_{i} = \lambda_{j}$)
	1. **Valós alaprendszer**: 
		- $y_{i}(x) = e^{\lambda_{i}x}$
		- $y_{j}(x) = e^{\lambda_{j}x}*x$
1. Ha $D < 0$: ($\lambda_{i},\lambda_{j}$ konjugált komplex szám)
	2. **Valós alaprendszer**: 
		- $y_{i} = \mathrm{Re}(y^{\lambda_{i} x})$
		- $y_{j} = \mathrm{Im}(e^{\lambda_{j}x})$
	- Ebben az esetben egy ú.n. kvázipolinom fog megjelenni
2. $y_{h}(x) = \alpha_{1} *y_{1}(x) + \alpha_{2}*y_{2}(x) + \dots + \alpha_{n} * y_{n}(x)$, azaz lesz $n$ db ismeretlenünk
3. Ez egyben az **összes megoldás** is

#### Megj.:
- $\alpha + i*\beta \in \mathbb{C}$ gyök:
	- $e^{\alpha x}*\cos(\beta x)$
	- $e^{\alpha x} * \sin(\beta x)$ 

#### Inhomogén eset

##### Kezdet
$a_{n}y^{(n)}+a_{n-1}y^{(n-1)}+\dots+a_{1}y' + a_{0}y = g(x)$ ~ (nem kell mindegyik derivált)
##### Algo.:
1. **Homogén rész**: $a_{n}y^{(n)}+a_{n-1}y^{(n-1)}+\dots+a_{1}y' + a_{0}y = 0$ ~ (nem kell mindegyik derivált) megoldása az előzőek alapján
3. **Inhomogén rész**: $a_{n}$


#### Állandó együtthatós eset *és* kvázipolinom jobb oldal