# BEGIN PROB

(14 points) Albert collected 400 data points from a radiation detector.
Each data point contains 3 feature: feature A, feature B and feature C,
along with the true particle energy E. Albert want to design a linear
regression algorithm to predict the energy E of each particle, given one
or a combination(s) of feature A, B, C. As the first step, Albert
calculated the correlation coefficients among A, B, C and E. He wrote it
down in the following table, where each cell of the table represents the
correlaton of two terms:

::: center
                  **Feature A**   **Feature B**   **Feature C**   **Energy E**
  --------------- --------------- --------------- --------------- --------------
  **Feature A**   1               -0.99           0.13            0.8
  **Feature B**   -0.99           1               0.25            -0.95
  **Feature C**   0.13            0.25            1               0.72
  **Energy E**    0.8             -0.95           0.72            1
:::

# BEGIN SUBPROB

(4pt) Albert want to start with a simple model: fitting only a single
feature to obtain the true energy (i.e. $y = w_0+w_1 x$). Which feature
should he choose as $x$ to get the lowest mean square error?

( ) A
( ) B
( ) C

# BEGIN SOLUTION

B is the correct answer, because it has the highest absolute correlation
(0.95), the negative sign in front of B just means it is negatively
correlated to energy and it can be compensated by a negative sign in the
weight.

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

(2pt) Albert want to add another feature into his linear regression in
part a) to further boost the model's performance. (i.e.
$y = w_0+w_1 x + +w_2 x_2$) Which feature should he choose as $x_2$ to
make additional improvements?

( ) A
( ) B
( ) C

# BEGIN SOLUTION

C is the correct answer, because although A has a higher correlation
with energy, it also has an extremely high correlation with B (-0.99),
that means adding A into the fit will not be too much useful, since it
provides almost the same information as B.

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

Albert further refine his algorithm by fitting a prediction rule of the
form: $$\begin{aligned}
H(A,B,C) = w_0 + w_1 \cdot A\cdot C + w_2 \cdot B^{C-7}
\end{aligned}$$

(3pt)Given this prediction rule, What are the dimensions of the design
matrix X? AKA what is $r$ and $c$?

$r \text{rows} \times c \text{columns}$

# BEGIN SOLUTION

$400 \text{rows} \times 3 \text{columns}$

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

(5pt) Now Albert solve the normal equations and find the solution to be:
$$\vec{w}^* = \begin{bmatrix} w_0^* \\ w_1^* \\ w_2^*  \end{bmatrix}$$
To improve on this result, Albert decides to modify his design matrix
with the following steps:

1.  Add 1 to every entry to the first column

2.  Interchange the second and the third column

Let $X_a$ be the modified design matrix. Let
$\vec{w_a}^* = (X_a^TX_a)^{-1}X_a^T\vec{y}$. Express the components
$\vec{w_a}^*$ in terms of $w_0^*, w_1^*, w_2^*$, which were the
components of $\vec{w}^*$.

$$\vec{w_a}^* = \begin{bmatrix} \phantom{XXX} \\ \phantom{XXX} \\ \phantom{XXX} \\ \phantom{XXX} \\ \phantom{XXX} \end{bmatrix}$$

# BEGIN SOLUTION

$$\vec{w}^* = \begin{bmatrix} w_0^*/2 \\ w_2^* \\ w_1^*  \end{bmatrix}$$

# END SOLUTION

# END SUBPROB

# END PROB