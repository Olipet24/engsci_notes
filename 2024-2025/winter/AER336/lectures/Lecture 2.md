
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
e.g
$$
l_{1}(x) = \frac{(x-x_{2})(x-x_{3}) \leftarrow\text{ 2 roots and degree 2 }}{(x_{1}-x_{2})(x_{1}-x_{2}) \leftarrow \text{ normalization }}
$$
Denominator is Normalization, and the numerator is 2 roots and 2 degree polynomial

Then $P_{n=2}(x) = y_{1}l_{1}(x)+y_{2}l_{2}(x)+y_{3}l_{3}(x)$

**Q**: Is the above a polynomial interpolant?
- Poly