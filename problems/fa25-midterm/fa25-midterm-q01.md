# BEGIN PROB

You are working in a biology laboratory to quantify how an antibiotic drug influences the population growth of *E. coli* bacteria. You inoculate a Petri dish with the bacteria and the drug, then monitor the culture over time. At measurement times $x_1, x_2, \dotsc, x_n$ (hours since inoculation), you estimate the total bacterial count $y_1, y_2, \dotsc, y_n$. To describe the growth pattern, you propose the exponential model
$$H(x) = h\,e^{-x}, \qquad h \in \mathbb{R}.$$

Note: in version B the given function was $H(x)=he^x$.

# BEGIN SUBPROB

Using the squared loss function $\ell_{sq}(h, (x_i, y_i)) = (he^{-x_i} - y_i)^2$, clearly write down the associated empirical risk as a function of $h$.

# BEGIN SOLUTION

**Version A:**
$$R(h)\;=\;\frac{1}{n}\sum_{i=1}^n\big(he^{-x_i}-y_i\big)^2.$$

**Version B:**
$$R(h)\;=\;\frac{1}{n}\sum_{i=1}^n\big(he^{x_i}-y_i\big)^2.$$

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

Compute $\frac{d}{dh} R(h)$.

# BEGIN SOLUTION

**Version A:**

$$R(h)=\frac{1}{n}\sum_{i=1}^n\big(he^{-x_i}-y_i\big)^2$$

Differentiate term–by–term (chain rule):
$$\frac{d}{dh}R(h)=\frac{1}{n}\sum_{i=1}^n 2\big(he^{-x_i}-y_i\big)\cdot e^{-x_i}
=\frac{2}{n}\left(h\sum_{i=1}^n e^{-2x_i}-\sum_{i=1}^n y_i e^{-x_i}\right).$$

Equivalently, expanding the square,
$$R(h)=\frac{1}{n}\sum_{i=1}^n\!\left(h^2e^{-2x_i}-2hy_ie^{-x_i}+y_i^2\right)
\;\Rightarrow\; R'(h)=\frac{2}{n}\left(h\sum e^{-2x_i}-\sum y_ie^{-x_i}\right).$$

**Version B:**

$$R(h)=\frac{1}{n}\sum_{i=1}^n\big(he^{x_i}-y_i\big)^2$$

Differentiate term–by–term (chain rule):
$$\frac{d}{dh}R(h)=\frac{1}{n}\sum_{i=1}^n 2\big(he^{x_i}-y_i\big)\cdot e^{x_i}
=\frac{2}{n}\left(h\sum_{i=1}^n e^{2x_i}-\sum_{i=1}^n y_i e^{x_i}\right).$$

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

Prove that the global minimizer $h^\ast$ for $R(h)$ is given by the formula
$$h^\ast \;=\; \frac{\sum_{i=1}^n y_i e^{-x_i}}{\sum_{i=1}^n e^{-2x_i}}.$$

# BEGIN SOLUTION

**Version A:**

Set the derivative to zero:
$$0=\frac{2}{n}\left(h^\ast\sum_{i=1}^n e^{-2x_i}-\sum_{i=1}^n y_i e^{-x_i}\right)
\;\Longrightarrow\;
h^\ast\sum_{i=1}^n e^{-2x_i}=\sum_{i=1}^n y_i e^{-x_i}$$
$$h^\ast=\frac{\sum_{i=1}^n y_i e^{-x_i}}{\sum_{i=1}^n e^{-2x_i}}.$$

Uniqueness: $R(h)$ is a quadratic with
$$R''(h)=\frac{2}{n}\sum_{i=1}^n e^{-2x_i}>0$$

Since $e^{-2x_i}>0$ for all $i$, $R'' > 0$ and the critical point is the unique minimizer.

**Version B:**

Set the derivative to zero:
$$0=\frac{2}{n}\left(h^\ast\sum_{i=1}^n e^{2x_i}-\sum_{i=1}^n y_i e^{x_i}\right)
\;\Longrightarrow\;
h^\ast=\frac{\sum_{i=1}^n y_i e^{x_i}}{\sum_{i=1}^n e^{2x_i}}.$$

Uniqueness: $R(h)$ is a quadratic with
$$R''(h)=\frac{2}{n}\sum_{i=1}^n e^{2x_i}>0$$

Since $e^{2x_i}>0$ for all $i$, $R'' > 0$ and the critical point is the unique minimizer.

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

After talking to a colleague, you decide to use the following hypothesis function instead:
$$\widetilde{H}(x) = h_0 + h_1e^{-x}.$$

Using a suitable data transformation (i.e., change of variables) and formulas we have derived in class, find a formula for the optimal parameters $h_0^\ast, h_1^\ast$ which minimize the mean squared error for the hypothesis function $\widetilde{H}(x)$ given your observations from before.

# BEGIN SOLUTION

**For Version A:**

Let $z_i:=e^{-x_i}$. Then $\widetilde{H}(x)=h_0+h_1e^{-x}=h_0+h_1 z$ is ordinary simple linear regression of $y$ on $z$ with MSE.

**For Version B:**

Let $z_i:=e^{x_i}$. Then $\widetilde{H}(x)=h_0+h_1e^{x}=h_0+h_1 z$ is ordinary simple linear regression of $y$ on $z$ with MSE.

**The rest of the solution is the same for both versions:**

With $\bar z=\frac{1}{n}\sum z_i$ and $\bar y=\frac{1}{n}\sum y_i$,
$$h_1^\ast=\frac{\sum_{i=1}^n (z_i-\bar z)(y_i-\bar y)}{\sum_{i=1}^n (z_i-\bar z)^2},
\qquad
h_0^\ast=\bar y-h_1^\ast\,\bar z.$$

Equivalently, by the normal equations
$$\begin{bmatrix} n & \sum z_i\\[2pt] \sum z_i & \sum z_i^2 \end{bmatrix}
\begin{bmatrix} h_0^\ast\\ h_1^\ast \end{bmatrix}
=
\begin{bmatrix} \sum y_i\\ \sum z_i y_i \end{bmatrix}.$$

**Alternative solution:**

Let the design matrix be
$$\mathbf{X} = \begin{bmatrix}
1 & z_1 \\ 
1 & z_2 \\
\vdots & \vdots \\
1 & z_n \\                 
\end{bmatrix}$$

Then by the normal equations
$$\mathbf{X}^T\mathbf{X} h =\mathbf{X}^Ty$$

# END SOLUTION

# END SUBPROB

# END PROB