# BEGIN PROB

For each of the following statements, **clearly** fill in **TRUE** or **FALSE**. You do not need to show any work to earn full credit, but you can provide justification to possibly earn partial credit.

In parts **(a)**–**(d)**, let $\{(\vec{x}_i, y_i)\}_{i=1}^n$ be a fixed dataset, where each $\vec{x}_i \in \mathbb{R}^d$ and $y_i \in \mathbb{R}$. Let $X \in \mathbb{R}^{n \times (d+1)}$ be the corresponding design matrix defined in the usual way. (For simple linear regression, $d = 1$ and each $\vec{x}_i$ is a scalar.)

# BEGIN SUBPROB

For a simple linear regression model:
$$\min_{\vec{w} = (w_0, w_1)} \frac{1}{n}\sum_{i=1}^{n} |y_i -(w_0+w_1x_i)| = \min_{\vec{w} = (w_0, w_1)} \frac{1}{n} \| \vec{y} - X\vec{w}\|.$$

TRUE or FALSE?

# BEGIN SOLUTION

**FALSE.** LHS is MAE (L₁); RHS is the Euclidean norm (L₂). They minimize different objectives.

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

$\nabla \|X\vec{w} - \vec{y}\|^2 = X^\top X \vec{w} - X^\top \vec{y}$.

TRUE or FALSE?

# BEGIN SOLUTION

**FALSE.** $\nabla\|X\vec w-\vec y\|^2=2X^\top(X\vec w-\vec y)=2X^\top X\vec w-2X^\top \vec y$ (missing factor 2).

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

$d+1 = \mathrm{rank}(X^\top X) + \textrm{dim}(\mathrm{null}(X) )$.

TRUE or FALSE?

# BEGIN SOLUTION

**TRUE.** Rank–nullity: $\mathrm{rank}(X)+\mathrm{null}(X)=d+1$ and $\mathrm{rank}(X^\top X)=\mathrm{rank}(X)$.

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

If the columns of $X$ are orthonormal (so $X^\top X = I$), then the optimal parameter $w_i^\ast$ is given by $w_{i}^\ast = \vec{c}_i\cdot \vec{y}$, where $\vec{c}_i$ is the $i$-th column of $X$.

TRUE or FALSE?

# BEGIN SOLUTION

**TRUE.** The OLS estimator minimizes $\| \vec y - X\vec w\|^2$. Setting the gradient to zero gives the normal equations
$$2X^\top (X\vec w - \vec y)=0 \;\;\Longrightarrow\;\; X^\top X\,\vec w = X^\top \vec y.$$

If the columns of $X$ are orthonormal, then $X^\top X=I$, hence
$${\vec w}^*=(X^\top X)^{-1}X^\top \vec y = I^{-1}X^\top \vec y = X^\top \vec y.$$

Since $X^\top X=I$ is invertible, the solution is unique. Geometrically, the coefficients are the inner products with the orthonormal regressors.

# END SOLUTION

# END SUBPROB

For parts **(e)**–**(g)**, consider the following scenario.

Glinda's dataset has two features, $x^{(1)}$ and $x^{(2)}$. She first fits a simple linear regression model $H_1(\vec{\alpha})$ using only the feature $x^{(1)}$. By minimizing $R_{1}$, the mean squared error (MSE) associated with this model, she obtains the optimal parameter vector $\vec{\alpha}^{*} = (\alpha_0^{*}, \alpha_1^{*})$. She then fits a second simple linear regression model $H_2(\vec{\beta})$ using only the feature $x^{(2)}$ and, after minimizing $R_{2}$, the MSE for this model, obtains $\vec{\beta}^{*} = (\beta_0^{*}, \beta_1^{*})$. Finally, she fits a multiple linear regression model using both features,
$$H_3(\vec{w},\vec{x}) = 
\begin{bmatrix} 1 & x^{(1)} & x^{(2)} \end{bmatrix} 
\begin{bmatrix} w_0 \\ w_1 \\ w_2 \end{bmatrix},$$
where $x^{(1)}$ and $x^{(2)}$ are the feature values for a single observation. Minimizing $R_{3}$, the MSE for this model, yields the optimal parameter vector $\vec{w}^{*} = (w_0^{*}, w_1^{*}, w_2^{*})$.

# BEGIN SUBPROB

$w^*_1=\alpha^*_1$ and $w^*_2=\beta_1^*$.

TRUE or FALSE?

# BEGIN SOLUTION

**FALSE.** Adding a second feature generally changes both coefficients; equality only under special conditions (e.g., orthogonality/centering).

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

$R_3(\vec{w}^\ast) = R_1(\vec{\alpha}^\ast) - R_2(\vec{\beta}^\ast)$

TRUE or FALSE?

# BEGIN SOLUTION

**FALSE.** There is no subtraction relation between optimal MSEs; moreover the RHS can be negative. Typically $R_3\le\min\{R_1,R_2\}$.

# END SOLUTION

# END SUBPROB

Elphaba collects an additional feature $x^{(3)}$ and adds it to Glinda's dataset. She calculates a multiple linear regression model $H_4(\vec{v})$ using all 3 features, and minimizes the associated MSE $R_4$ to obtain an optimal parameter vector $\vec{v}^\ast$.

# BEGIN SUBPROB

$R_3(\vec{w}^\ast) \geq R_4(\vec{v}^\ast)$.

TRUE or FALSE?

# BEGIN SOLUTION

**TRUE.** Adding features cannot increase the minimized in-sample MSE: $R_4(\vec v^\ast)\le R_3(\vec w^\ast)$.

# END SOLUTION

# END SUBPROB

# END PROB