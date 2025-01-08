
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

However, the issue is that Chebyshev nodes is not very practical, since it requires you having the ability to choose where you want the measurement points to be