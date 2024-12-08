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