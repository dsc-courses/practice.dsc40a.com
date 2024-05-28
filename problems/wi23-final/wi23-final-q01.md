# BEGIN PROB

**Empirical risk minimization**

For the loss functions below, find $h^*$ which minimizes the
corresponding empirical risk with respect to the data
$y_1 = -3, y_2 = 2, y_3 = 2, y_4 = -2$, $y_5 = -6$ .

::: responsebox
3.2in This question was based on Final Winter 2021 Part 1 problem 2.
:::

# BEGIN SUBPROB

\[4 points\] The **$\alpha$-absolute** loss is defined as follows:
$$L_{\alpha-\text{abs} }(h, y) = |h - (y-\alpha) |.$$

Use $\alpha=3$. Bonus \[2 points\]: What is the empirical risk
$R_{\alpha-\text{abs}} (h^*)$?

::: responsebox
3in This is equivalent to the absolute loss on the same dataset shifted
by $\alpha$. Therefore the optimal solution that minimizes this loss is
the median shifted by $-\alpha$.

$h^*=-2-3=-5$.
:::

# BEGIN SOLUTION

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

\[4 points\] The **$\beta$-zero-one** loss is defined as follows:
$$\begin{aligned}
                L_{\beta -01}(h,y) = \begin{cases}
                    0,& \text{$h = y\mathbf{\beta} $},\\
                    1,& \text{$h \neq y\mathbf{\beta} $}.
                \end{cases}
            
\end{aligned}$$

Use $\beta=2$. Hint: plot the empirical risk function for $y\in[-6, 3]$.

Bonus \[2 points\]: What is the empirical risk $R_{\beta- 01} (h^*)$?

::: responsebox
3.2in This is equivalent to the absolute loss on the same dataset scaled
by $\beta$. Therefore the optimal solution that minimizes this loss is
the mode scaled by $\beta$.

$h^*=2*2=4$.
:::

# BEGIN SOLUTION

# END SOLUTION

# END SUBPROB

# END PROB