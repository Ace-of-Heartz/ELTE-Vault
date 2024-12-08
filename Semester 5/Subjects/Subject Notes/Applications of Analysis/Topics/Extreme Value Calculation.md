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
