# BEGIN PROB

Let $\vec{y}_1, \vec{y}_2, \dotsc, \vec{y}_n \in\mathbb{R}^2$ be a collection of two-dimensional vectors and let $\overline{y} = \frac{1}{n}\sum_{i=1}^n \vec{y}_i$. Suppose we wish to model the $\vec{y}_i$'s using a single *vector* of the form $c\vec{z}$ where $\vec{z} = \begin{bmatrix} -1 & 1 \end{bmatrix}^T$ and $c\in\mathbb{R}$ is a real number (to be determined).

# BEGIN SUBPROB

Suppose we use the loss function $L_{\mathrm{sq}}(\vec{y}_i, c) = |\vec{y}_i^{(1)} + c|^2 + |\vec{y}_i^{(2)} - c|^2$. Write down the empirical risk function $R_{\mathrm{sq}}(\{\vec{y}_i\}_{i=1}^n, c)$.

# BEGIN SOLUTION

$R_{\mathrm{sq}}(\{\vec{y}_i\}_{i=1}^n, c) = \frac{1}{n}\sum_{i=1}^n \left(|\vec{y}_i^{(1)} + c|^2 + |\vec{y}_i^{(2)} - c|^2\right)$.

# END SOLUTION

# END SUBPROB


# BEGIN SUBPROB

Show that $c^\ast = \frac{1}{2}\vec{z}^T \overline{y}$ is the only
critical point for the empirical risk function
$R_{\mathrm{sq}}(\{\vec{y}_i\}_{i=1}^n, c)$ you found in part **(a)**.


# BEGIN SOLUTION

\begin{align*}
\frac{d}{dc} R_{\mathrm{sq}}((\vec{y}_i), c) &= \frac{d}{dc} \frac{1}{n}\sum_{i=1}^n \left(|\vec{y}_i^{(1)} + c|^2 + |\vec{y}_i^{(2)} - c|^2\right)\\
&= \frac{1}{n}\sum_{i=1}^n \left( 2(\vec{y}_i^{(1)} + c)- 2(\vec{y}_i^{(2)} - c)\right)\\
&= 4c - \frac{2}{n}\sum_{i=1}^n\mathbf{1}^T \vec{y}_i\\
&=4c - 2\vec{z}^T \overline{y}.          
\end{align*}
Therefore, the one critical point occurs when $c = \frac{1}{2}\vec{z}^T \overline{y}$.

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

Given the dataset: $$\vec{y_1}=\begin{bmatrix}
                    1 \\ - 2
                \end{bmatrix}
                \quad
                \vec{y_2}=\begin{bmatrix}
                    -3 \\ 4
                \end{bmatrix}
                \quad
                \vec{y_3}=\begin{bmatrix}
                    2 \\ - 2
                \end{bmatrix}$$ what is
$R_{\mathrm{sq}}(\{\vec{y}_1, \vec{y}_2, \vec{y}_3\}, c^\ast)$?

# BEGIN SOLUTION

=

::: bmatrix
0\
0
:::

$c^*=\frac{1}{2}\vec{z}^T \overline{y} = 0$

$$\begin{aligned}
             R_{\mathrm{sq}}((\vec{y}_i), c)  & = \frac{1}{n}\sum_{i=1}^n \left(|\vec{y}_i^{(1)} - c|^2 + |\vec{y}_i^{(2)} - c|^2\right) \\ 
             & = \frac{1}{3} \left( (1^2+2^2) + (3^2+4^2) + (2^2+2^2) \right) = \frac{38}{3}
         
\end{aligned}$$

# END SOLUTION

# END SUBPROB

# END PROB