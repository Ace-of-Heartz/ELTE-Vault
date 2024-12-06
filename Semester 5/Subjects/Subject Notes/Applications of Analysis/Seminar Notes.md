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
