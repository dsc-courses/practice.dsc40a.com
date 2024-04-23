# BEGIN PROB

Suppose you have a dataset 
$$\{(x_1, y_1), (x_2,y_2), \dots, (x_8, y_8)\}$$ 
with $n=8$ ordered pairs such that the variance of $\{x_1, x_2, \dots, x_8\}$ is $50$. Let $m$ be the slope of the regression line fit to this data.

Suppose now we fit a regression line to the dataset
$$\{(x_1, y_2), (x_2,y_1), \dots, (x_8, y_8)\}$$ 
where the first two $y$-values have been swapped. Let $m'$ be the slope of this new regression line.

If $x_1 = 3$, $y_1 =7$, $x_2=8$, and $y_2=2$, what is the difference between the new slope and the old slope? That is, what is $m' - m$? The answer you get should be a number with no variables.

**Hint:** There are many equivalent formulas for the slope of the regression line. We recommend using the version of the formula without $\overline{y}$.

# BEGIN SOLUTION
Using the formula for the slope of the regression line, we have
$$
\begin{aligned}
m &= \frac{\sum_{i=1}^n (x_i - \overline x)y_i}{\sum_{i=1}^n (x_i - \overline x)^2}\\
&= \frac{\sum_{i=1}^n (x_i - \overline x)y_i}{n*\sigma_x^2}\\
&= \frac{(3-\bar{x})*7 + (8 - \bar{x})*2 + \sum_{i=3}^n (x_i - \overline x)y_i}{8*50}. \\
&\text{Note that by switching the first two $y$-values, the terms in the sum from $i=3$ to $n$,} \\
&\text{the number of data points $n$, and the variance of the $x$-values are all unchanged.} \\
\text{So the slope becomes:} \\
m' &= \frac{(3-\bar{x})*2 + (8 - \bar{x})*7 + \sum_{i=3}^n (x_i - \overline x)y_i}{8*50} \\
\text{and the difference between these slopes is given by} \\
m'-m &= \frac{(3-\bar{x})*2 + (8 - \bar{x})*7 - ((3-\bar{x})*7 + (8 - \bar{x})*2)}{8*50}\\
&= \frac{(3-\bar{x})*2 + (8 - \bar{x})*7 - (3-\bar{x})*7 - (8 - \bar{x})*2}{8*50}\\
&= \frac{(3-\bar{x})*(-5) + (8 - \bar{x})*5}{8*50}\\
&= \frac{ -15+5\bar{x} + 40 -5\bar{x}}{8*50}\\
&= \frac{ 25}{8*50}\\
&= \frac{ 1}{16}
\end{aligned}
$$
# END SOLUTION
# END PROB