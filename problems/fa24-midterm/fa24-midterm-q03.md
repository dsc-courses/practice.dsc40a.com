# BEGIN PROB

Assume you have a dataset
$\vec{x}_1, \vec{x}_2, \dotsc, \vec{x}_n\in\mathbb{R}^{d}$ of
$d$-dimensional vectors for $n$ individuals, and that each has a scalar
response value $y_1,\dotsc, y_n$. You then fit a multiple linear
regression prediction rule
$H_1(\vec{x}) = \vec{w}^T\text{Aug}(\vec{x})$, with optimal parameters
$\vec{w}^*$ whose MSE is $c_1$.

# BEGIN SUBPROB

Due to privacy reasons it turns out you are unable to use the feature
$x^{(d)}$, so you need to find a way to modify your model so that it
does not incorporate this feature. Your friend Minnie suggests using the
parameters of the prediction rule you learned already and simply setting
$w_d=0$: $$H_2(\vec{x}) = \begin{bmatrix}
                    w_0^* & w_1^* & \ldots & w_{d-1}^* & 0
                \end{bmatrix}^T \text{Aug}(\vec{x}).$$ Denote the MSE of
the model $H_2(\vec{x})$ by $c_2$.

Meanwhile, your friend Maxine recommends fitting a new prediction rule
$H_3$ to the data with only the first $d-1$ features, with MSE $c_3$.

Order the three errors $c_1, c_2, c_3$ from least to greatest. Explain
your solution. *(Use $<$ if the error is strictly smaller, $=$ if the
errors are equal or $\leq$ if the errors may be equal.)*


# BEGIN SOLUTION

$c_1 \leq c_3 \leq c_2$.

The prediction rule $H_1$ uses an additional feature compared to $H_3$.
The MSE cannot increase by adding a feature (HW4), therefore
$c_1 \leq c_3$.

The MSE $c_3$ is as small as it can possibly be when using $d-1$
features. If we were to pick other coefficients -- *whatever* they may
be -- the MSE cannot be smaller. So if we picked the coefficients
$(w^*_0, w^*_1, \ldots, w^*_{d-1})$, note that setting $w_d=0$ in $H_2$
is the same as setting a prediction rule with $d-1$ features and the
first $d$ parameters of $w^*$. Since this prediction rule is using $d-1$
features, the MSE $c_2$ of this model cannot be smaller than $c_3$.

<average>65</average>

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

You are able to add **5 additional individuals** to your datasets, so
that now you have $n+5$ **individuals**. You fit a new prediction rule
to the data whose MSE is $c_4$. Can $c_4< c_1$? Explain.

# BEGIN SOLUTION

In the case you add 5 individuals that exactly match the prediction
rule, their added squared errors are all zero and therefore the *mean*
squared error is smaller $c_4 = \frac{n c_1}{n+5}$.;

<average>41</average>

# END SOLUTION

# END SUBPROB

# END PROB