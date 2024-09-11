# Overview:
## Techniques:
### Determining if a known function is **Solution**
1. Given a function $y = ...$
2. Determine its derivatives that occur in the given equation
3. Substitute

### Initial-value problem:
**Geometrically:** we look at the family of solution curves and pick the one that passes through the point $(t_0,y_0)$. 
**Physically:** using the state of a system at time (or in general an attribute) $t_0$ and using the solution of the initial-value problem, we predict the future behaviour of our system.

### Direction Fields:
**Geometrical point-of-view**

Allows us to visualize the general shape of the solution curves by indicating the direction in which the curves proceed at each point.
Other names: *slope field* 

### Euler's Method:
**Numerical method/point-of-view**

Approximate the values for the solution of the initial-value problem 
$y' = F(x,y) ; y(x_0) = y_0$ 
with step size $h$, at $x_n = x_{n-1} + h$
$y_n = y_{n-1} + h F(x_{n-1},y_{n-1})$ $n = 1,2,3,...$ 

### Separable Differential Equations:
When the expression "on the right side" can be "separated" into a function of x and a function of y
1. $dy/dx = g(x)/h(y)$ where $h(y) = 1/f(y)$ if $f(y) \neq 0$ 
2. Rewrite it into differential form:
	$h(y) dy = g(x) dx$ 
3. Integrate both sides
4. Use Chain Rule

### Linear Equations:
1.) $dy/dx + P(x) y = Q(x)$ 
where $P$ and $Q$ are continuous functions on a given interval.
We use this when the expression cannot be separated with the above method.

1. Rewrite the equation
2. Integrate both sides

General steps:
*Integrating factor ~ I*
1. Find $I$ so that the left side of 1.), when multiplited by $I(x)$, becomes the derivative of the product $I(x)y$: $I(x)(y' + P(x)y) = (I(x)y)'$ 
2. With this: $(I(x)y)' = I(x)Q(x)$ holds true
3. Integrate both sides
4. Rearrange for $y(x)$
5. For such an $I$, we expand the term in the 1. point: $I(x)y' + I(x)P(x)y = (I(x)y)' = I'(x)y + I(x)y'$ =>  $I(x)P(x) = I'(x)$ 
6. This is a separable equation for I, which we solve: $\int dI/I = \int P(x) dx$ => $ln|I| = \int P(x) dx$ => $I = Ae^{\int P(x) dx}$ where $A = +/- e^C$ 
7. For a particular $I$, we take $A = 1$
8. $I(x) = e^{\int P(x) dx}$  
TL/DR: Multiply both sides by the **integrating factor I(x)** and integrate both sides.

### Predator-prey Equations
When the model is more complex.
Other name: *Lotka-Volterra equations*
**Solutions**: $R(t)$ and $W(t)$ as functions of time. The system is coupled, therefore we need to solve them simultaneously.
## Keywords:
- **Differential Equation**: an equation that contains an unknown function and one or more of its derivatives
- **Order of a differential equation**: the order of the highest derivative that can be found in the equation 
- **Solution**: a function which satisfies a  given differential equation when $y = f(x)$ and its derivatives are substituted into the equation.
- **Family of solutions**: aka. the *general solution*
- **Initial condition**: $y_0 = y(t_0)$ 
- **Initial-value problem**
- **Direction Fields**
- **Solution Curve**
- **Autonomous differential equation**: a differential equation that which is missing the independent variable from the "right side" (the one without $dy/dt$)
- **Orthogonal Trajectory**: a curve that intersects a family of curves orthogonally 
- **Equilibrium Solution**: the constant solution