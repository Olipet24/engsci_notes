
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

Idea: fit a polynomial through the data points and evaluate the polynomial at the point of interest (x) 
