
## Useful definitions

**Cost**: how much computational effort is required to provide approximation (FLOP)

**Accuracy/Error Analysis**: How closely does our (discrete) approximation estimate the exact (continuous) solution?
- How can we characterize this system?

**Goal**: We desire algorithms that achieve:
- given accuracy for a minimal cost
- maximum accuracy for a given cost

## Grade Markdown
- Assignments (6): 20%, 10% deduction per day
- Midterm: 25%, March 3rd (Will be changed)
- Final Exam: 55%

**Office Hours**: TBD

## Polynomial Interpolation

From a given set of data that follows some graph:
![[Pasted image 20250106134348.png]]

**Question**: Given n+1 data points $(x_{i}, y_{i})$, i = 1, 2, ... n+1, estimate y for any given x (i.e create a lookup table)

**Idea**: fit a polynomial through the data points and evaluate the polynomial at the point of interest (x) 

**Polynomial Interpolation**: Given $(x_{i}, y_{i})$, i = 1, 2, .. n+1, find degree-n polynomial:
$$
P_{n}(x) = \sum_{j=0}^{n} a_{j}x^j
$$ such that 
$$
P_{n}(x_{i}) = y_{i}, i = 1, 2,.. n+1
$$ 
Here $P_{n}$: interpolant and $\{x_{i}\}_{i=1}^{n+1}$ are the interpolation points

Interpolant is defined by:
1. Degree n polynomial
2. Location of interpolation points

**Goal**: given any data points, find $\{a_{j}\}_{j=0}^{n}$ in a systematic manner

### Vandermonde's Method

***Case n = 1***: Linear interpolation
- assume $x_{1} \neq x_{2}$ 
- $P_{1}(x) = a_{0} + a_{1}x$
- Interpolation condition:
$$\begin{cases}
P_{1}(x_{1}) = a_{0} + a_{1}x_{1} = y_{1} \\
P_{1}(x_{2}) = a_{0} + a_{1}x_{2} = y_{2}
\end{cases}

$$
Matrix form:
$$
\begin{pmatrix}
1 & x_{1} \\
1 & x_{2}
\end{pmatrix} \begin{pmatrix}
a_{0} \\
a_{1}
\end{pmatrix}
= \begin{pmatrix}
y_{1} \\
y_{2}
\end{pmatrix}
$$
Explicit Solution:
$$
P_{1}(x) = \underbrace{ \left( y_{1} - \frac{y_{2}- y_{1}}{x_{2}-x_{1}}x_{1} \right) }_{ a_{0} }+ \underbrace{ \left( \frac{y_{2}-y_{1}}{x_{2}-x_{1}}x \right) }_{ a_{1} } = y_{1} + \left( \frac{y_{2}- y_{1}}{x_{2}-x_{1}} \right)(x-{x_{1}})
$$
***General Case***:
- Assume $x_{1}, x_{2}\dots x_{n+1}$ are distinct
- Find $P_{n}(x) = a_{0}+a_{1}x + \dots a_{n}x^n]$