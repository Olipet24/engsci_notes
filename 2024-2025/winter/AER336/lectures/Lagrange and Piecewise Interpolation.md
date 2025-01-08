
**Recap**

Vandermonde's method:
$$
P_{n}(x) = a_{0}+a_{1}x+\dots+a_{n}x^n
$$

Interpolation Conditions:
$$
P_{n}(x_{i}) = a_{0}+ a_{1}x_{i}+\dots+a_{n}x^n_{i}= y_{i}
$$
For $i= 1,2,\dots, n$

Cost and error

## Lagrange's Basis Polynomials

**Case n = 2**:

***Idea***: Choose degree 2 polynomial basis function $\{l_{j}\}$ s.t 
$$
l_{j}(x_{i})=\begin{cases}
1 \text{ if } i = j\\
0 \text{ if } i \neq j
\end{cases}

$$
e.g.
$$
l_{1}(x) = \frac{(x-x_{2})(x-x_{3})}{(x_{1}-x_{2})(x_{1}-x_{3}) } \frac{\leftarrow\text{ 2 roots and degree 2 }}{\leftarrow \text{ normalization }}
$$
Denominator is Normalization, and the numerator is 2 roots and 2 degree polynomial

Then $P_{n=2}(x) = y_{1}l_{1}(x)+y_{2}l_{2}(x)+y_{3}l_{3}(x)$

**Q**: Is the above a polynomial interpolant?
- Polynomial of degree 2
- interpolation conditions: $P_{2}(x)= y_{1}l_{1}(x_{1}) + \cancelto{ 0 }{ y_{2}l_{2}(x_{1}) } + \cancelto{ 0 }{ y_{3}l_{3}(x_{1}) } = y_{1}$

**Q**: Is $P_{n=2}^{\text{lagrage}}(x)= P_{n=2}^{\text{Vandermonde}}(x)$? => Yes

### Generalization

degree n polynomials $\{l_{j}\}_{j=1}^{n+1}$ s.t. 
$$
l_{j}(x_{j})= \begin{cases}
1 & \text{if } i=j \\
0 & \text{if } i \neq j
\end{cases}
$$
is give by
$$
l_{j}(x) = \prod_{\substack{1 \leq k \leq n+1 \\ k\neq j }} \frac{x-x_{k}}{x_{j}-x_{k}}, j = 1, \dots n+1
$$
**Notes**:
1. no linear system to solve
2. $P_{n}^\text{lag}(x) = P_{n}^{\text{Vandermonde}}$ => some error analysis

### Runge's Phenomenon
- oscillation that polynomial interpolants exhibit for some functions when equispaced interpolation points are used
- e.g. Runge's Function $f(x) = \frac{1}{1+25^2}, x\in[-1, 1]$
	- smooth but $|f(x)- P_{n}(x)| \cancel{ \to } 0$ as $n \to \infty$

### Chebyshev nodes

***Idea***: use non-equispaced nodes

**Def**: Chebyshev nodes for $[-1, 1]$
$$
x_i = \cos\left( \frac{(i-1)}{n} \pi\right) 
$$
I.e. points cluster at the ends of the interval

**Derivation**:
$$
|f(x)-P_{n}(x)| = \frac{1}{(n+1)!} |f^{(n+1)}(\xi)|\underbrace{ |\prod_{i=j}^{n+1} (x-x_{i})| }_{ \text{ Chebyshev nearly mininmizes this} }
$$

However, the issue is that Chebyshev nodes is not very practical, since it requires you having the ability to choose where you want the measurement points to be.
- Possible solution is to use piecewise interpolation

## Piecewise Polynomial Interpolation (Lecture 2)

### Piecewise linear interpolation
- Basically have straight lines connecting each interpolation point

Given $x_{1} < x < x_{2}<\dots<x_{n+1}$, introduce n segments:
$$
S_{k} = [x_{k}, x_{k+1}], k = 1, 2, \dots, n
$$
Define $h \equiv x_{k+1} - x_{k}$

Over each $S_{k}$, introduce $$P_{h,1}^{(k)}(x) = a_{0}^k +a_{1}^k x$$
s.t.
$$
\begin{cases}
P_{n,1}^{(k)}(x_{k}) = y_{k} \\
P_{n,1}^{(k)}(x_{k+1})= y_{k+1}
\end{cases}
$$
where subscript is segment length, and polynomial degree. Superscript is segment \#. These $P_{n,1}^{(k)}$ can be found through Vandermonde or Lagrange mthd.

Global function:
$$
P_{n,1}(x)= \begin{cases}
P_{n,1}^{(k=1)}, & x \in S_{1} \\
 & \vdots \\
P_{n,1}^{(k=n)}(x), & x \in S_{n}
\end{cases}
$$
### Evaluation of $P_{n,1}(x)$
1. Find $k^*$ s.t. $x \in S_{k^*}$ (non-equispaced use bisection method ($O(\log_{2}(N))$))
	1. Envision all the segments as being in a sorted list
2. Evaluate $P_{n,1}^{(k^*)}(x)$

### Piecewise degree-p polynomial interpolation
- Basically fit a degree p polynomial between each point
	- This means that each segment might have more than one nodes in it
	- i.e. $x^{(\text{segment number})}_{\text{node number}}$
As before:
$$
P_{h, p}^{(k)} = \sum_{j=0}^P a_{j}^{(k)}x^j
$$
s.t.
$$
P_{h,p}^{(k)}(x_{i}^{(k)}) = y_{i}^{(k)}, i = 1, \dots,p+1
$$
**Note**: This does guarantee better error then linear piecewise polynomial

### Error Analysis
- Apply previous analysis to each segment: [[Introduction_interpolation#^ae6b86]]
- Assumptions:
	- $f$ is smooth on each $S_{k}$
	- $N$ equispaced segments
$$
|f(x)- P_{n,p}(x) |\leq \frac{1}{(p+1)!} \max_{S \in {a, b}}|f^{(p+1)}|h^{p+1}
$$

**Observations**:
1. error depends on $f^{p+1}, p, \text{\& } h$
2. For a fixed $h$, if $|f^{(p+1)}|h^{p+1}$ grows slower than $(p+1)!$, then error converges with $p$
3. For a fixed $p$, error converges as $h^{p+1}$, where $p+1$ is the convergence rate

Looking at the error diagram, the slope can be defined as:
$$
\underbrace{ |f(x)- P_{n,p}(x) | }_{ e }\leq \underbrace{ \frac{1}{(p+1)!} \max_{S \in {a, b}}|f^{(p+1)} }_{ C }|h^{p+1}
$$
=> $e \leq Ch^{p+1}$
=>$\log(e) \leq \log(C)+ \underbrace{ (p+1) }_{ slope }\log(h)$
Which makes sense, since $p+1$ is the convergence rate

## Spline Interpolation
Save for next lecture