# BEGIN PROB

Solve the linear regression for this dataset
$\mathcal{D} = \{(0, 0), (4, 2), (5, 1)\}$.\
$\bar x = \phantom{\hspace{.5in}}$\
$\bar y = \phantom{\hspace{.5in}}$\
$w_1^* =$\
$w_0^* =$

::: center
  $x_i$   $y_i$   $(x_i - \bar x)$   $(y_i - \bar y)$   $(x_i - \bar x)(y_i - \bar y)$   $(x_i - \bar x)^2$
  ------- ------- ------------------ ------------------ -------------------------------- --------------------
  0       0                                                                              
  4       2                                                                              
  5       1                                                                              
:::

Finally, what can we say about the correlation $r$ and the slope for
this dataset (mathematically)?

# BEGIN SOLUTION

$$\bar x = \frac{1}{3}(0 + 4 + 5) = 3$$
$$\bar y = \frac{1}{3}(0 + 2 + 1) = 1$$
\begin{center}
    \begin{tabular}{llllll}\toprule
        $x_i$ & $y_i$ & $(x_i - \bar x)$ & $(y_i - \bar y)$ & $(x_i - \bar x)(y_i - \bar y)$ & $(x_i - \bar x)^2$
        \\\midrule
        0 & 0 & -3 & -1 & 3 & 9 \\
        4 & 2 & 1 & 1 & 1 & 1 \\
        5 & 1 & 2 & 0 & 0 & 4 \\
        \bottomrule
    \end{tabular} \\
\end{center}
$$w_1^* =
\frac{
\displaystyle
\sum_{i=1}^n (x_i - \bar x)(y_i - \bar y)
}{
\displaystyle
\sum_{i=1}^n (x_i - \bar x)^2
}
= \frac{3 + 1 + 0}{9 + 1 + 4} = \frac{4}{14} = \frac{2}{7}
$$
$$w_0^* = \bar y - w_1^* \bar x = 1 - \frac{2}{7} \cdot 3 = 1 - \frac{6}{7} = \frac{1}{7}$$
Because $w_1^* = r \frac{\sigma_y}{\sigma_x}$ where the standard deviations $\sigma_y$ and $\sigma_x$ are non-negative, and $w_1^* = 2/7 > 0$, thus the correlation $r$ is positive and the slope is positive.

# END SOLUTION

# END PROB