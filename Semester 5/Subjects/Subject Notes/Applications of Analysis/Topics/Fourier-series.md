**Legyen**:
- $f \in R_{2\pi}$ 
- Válasszuk meg az intervallumot:
	- $(-\pi,\pi)$ 
	- VAGY
	- $(0,2\pi)$
# Együtthatók számolása
- $b_{k} = \frac{1}{\pi}* \int^\beta_{\alpha}f(x)*\sin(k*x)\ dx$
- $a_{0} = \frac{1}{2\pi}*\int^\beta_{\alpha}f(x)\ dx$
- $a_{k}=\frac{1}{\pi}*\int^{\beta}_{\alpha}f(x)*\cos(k*x)\ dx$, úgy hogy $k >0$  
**Ekkor**: 
$Sf(x) = a_{0} + \sum_{k=1}a_{k}*\cos(kx) + b_{k}*\sin(kx)$

# Tétel
$\forall x \in \mathbb{R}:$ **Weierstrass kritérium**: $Sf$ egyenletesen konvergál $\mathbb{R}$-en $\implies$ $\forall x \in \mathbb{R}:$ $f(x) = Sf(x)$  
**Spec.:** $\forall x \in [\alpha,\beta]$:
- $|Sf(x)| \leq\dots$ valamilyen $x$-et nem tartalmazó felső becsléssel.
- Ha van ilyen, akkor $Sf$ egyenletesen konvergál 
