# BEGIN PROB

- Each plot on the left contains a collection of ten points $\{(x_i, y_i)\}_{i=1}^{10}$, along with the line of best fit for an unknown hypothesis function and risk function.
- Next to each plot, clearly state the hypothesis function $H(x)$ and risk function $R(\vec{w})$ which *best match* the data and line of best fit. The placeholder $\vec{w}$ can denote either a single parameter or a vector of multiple parameters.
- Your hypothesis functions and risk functions should be borrowed from the formula bank provided below. *Some functions may be used more than once and others not at all*.
- In order to receive full credit, you must explain your reasoning using the box below each part of the problem.

**Hypothesis functions:**
- $H(x) = w_0 + w_1x$
- $H(x) = w_0$
- $H(x) = w_0\sin(w_1\,x)$
- $H(x) = w_0+w_1e^{-x}$
- $H(x) = w_0+w_1x+w_2x^2$

**Risk functions:**
- $R(\vec{w}) = \frac{1}{n}\sum_{i=1}^{n}(H(x_i) - y_i)^2$
- $R(\vec{w}) = \frac{1}{n}\sum_{i=1}^{10}\ln(H(x_{i}) - y_{i})$
- $R(\vec{w}) = \frac{1}{n}\sum_{i=1}^{n} |H(x_i) - y_i|$
- $R(\vec{w}) = \max_{1\leq i\leq n} |H(x_i) - y_i|$
- $R(\vec{w}) = (H(x_{10}) - y_{10})^2$

# BEGIN SUBPROB

[Plot a): Constant model with extreme outlier and maximum loss]

What are $H(x)$ and $R(\vec{w})$?

# BEGIN SOLUTION

$H(x)=w_0$ (constant). 

$R(w_0)=\max_i |y_i-w_0|$ (max loss).

Reason: the fitted line is the midrange level $\frac{\min y+\max y}{2}$, which minimizes the worst-case deviation.

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

[Plot b): Linear model with outliers and square loss]

What are $H(x)$ and $R(\vec{w})$?

# BEGIN SOLUTION

$H(x)=w_0 + w_1x$ (linear). 

$R(w_0, w_1)=\frac{1}{n}\sum_{i=1}^n\big(y_i-(w_0 + w_1x_i)\big)^2$ (squared loss/OLS).

Reason: line is pulled toward multiple high outliers, characteristic of L₂ sensitivity. Also, if LAD were used, the line would intersect two or more points, which isn't shown here.

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

[Plot c): Constant model with two outliers and square loss]

What are $H(x)$ and $R(\vec{w})$?

# BEGIN SOLUTION

$H(x)=w_0$ (constant). 

$R(w_0)=\frac{1}{n}\sum_{i=1}^n (y_i-w_0)^2$.

Reason: horizontal fit at the sample mean (two outliers shift the mean above the median, below the midrange).

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

[Plot d): Quadratic model with outliers]

What are $H(x)$ and $R(\vec{w})$?

# BEGIN SOLUTION

$H(x) = w_0 + w_1x + w_2x^2$

$R(\vec{w}) = \frac{1}{n}\sum_{i=1}^{n} (H(x_i) - y_i)^2$ or $R(\vec{w}) = \max_{1\le i\le n} |H(x_i) - y_i)|$. 

Reason: The curve is influenced by the three outlier points and does not pass through 3 points, so MAE can be ruled out (By Hwk 3 problem 7). Thus the only ones that make sense are $R(\vec{w}) = \frac{1}{n}\sum_{i=1}^{n} (H(x_i) - y_i)^2$ or $R(\vec{w}) = \max_{1\le i\le n} |H(x_i) - y_i)|$, and any justification of these is valid depending on the student's interpretation.

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

[Plot e): Linear model with outliers and absolute loss]

What are $H(x)$ and $R(\vec{w})$?

# BEGIN SOLUTION

$H(x)=w_0 + w_1x$ (linear). 

$R(w_0, w_1)=\frac{1}{n}\sum_{i=1}^n |y_i-(w_0 + w_1x_i)|$ (LAD / L₁ loss).

Reason: line tracks the trend with reduced influence from large outliers above. It also intersects two or more points, which is another clue.

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

[Plot f): Constant model with five outliers and absolute loss]

What are $H(x)$ and $R(\vec{w})$?

# BEGIN SOLUTION

$H(x) = w_0$

$R(w_0) = \frac{1}{n}\sum_{i=1}^{n} |H(x_i) - y_i|$

The line is flat so it must be a constant model, and the line passed through the median as opposed to the mean or midrange.

# END SOLUTION

# END SUBPROB

# END PROB