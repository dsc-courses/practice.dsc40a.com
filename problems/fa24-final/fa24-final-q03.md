# BEGIN PROB

\[(10 points)\]

A local farmers' market vendor sells homemade jam jars and is analyzing
the relationship between the number of hours she spends at the market
and the number of jam jars sold. Over three weekends, she collects the
following data:

-   **Weekend 1**: Worked for 1 hour, sold 2 jars.

-   **Weekend 2**: Worked for 2 hours, sold 4 jars.

-   **Weekend 3**: Worked for 3 hours, sold 6 jars.

Noticing a perfect linear trend, she decides to model this relationship
using linear regression. Let $x_1 = 1, x_2=2, x_3=3$ denote the number
of hours she worked on the corresponding weekend and let
$y_1 = 2, y_2=4, y_3=6$ denote the number of jars sold.

# BEGIN SUBPROB

First, fill in the blanks in the table below which gathers relevant
information for least squares regression. Then, find the optimal
parameters $w_0^\ast$ and $w_1^\ast$ for a simple least squares linear
model for her jar sales. *Show all your calculations.*

# BEGIN SOLUTION

# END SOLUTION

# END SUBPROB

::: center
+-----------------------+---------------------------------------------+
| $\sum_{i=1}^3 x_i$    | 6                                           |
+:=====================:+:===========================================:+
| $\sum_{i=1}^3 y_i$    | -----------------------------------------   |
+-----------------------+---------------------------------------------+
| $\sum_{i=1}^3 x_iy_i$ | 28                                          |
+-----------------------+---------------------------------------------+
| $\sum_{i=1}^3 x_i^2$  |                                             |
+-----------------------+---------------------------------------------+
:::

:::: responsebox
3.2in

::: center
    $\sum_{i=1}^3 x_i$     6
  ----------------------- ----
    $\sum_{i=1}^3 y_i$     12
   $\sum_{i=1}^3 x_iy_i$   28
   $\sum_{i=1}^3 x_i^2$    14
:::

To calculate the optimal parameters:

$$w_1^\ast = \frac{\sum_{i=1}^3 x_i y_i - \frac{1}{3} \sum_{i=1}^3 x_i \sum_{i=1}^3 y_i}{\sum_{i=1}^3 x_i^2 - \frac{1}{3} \left( \sum_{i=1}^3 x_i \right)^2}$$
Substituting values:
$$w_1^\ast = \frac{28 - \frac{1}{3}(6 \cdot 12)}{14 - \frac{1}{3}(6^2)} = \frac{28 - 24}{14 - 12} = \frac{4}{2} = 2$$

$$w_0^\ast = \frac{1}{3} \sum_{i=1}^3 y_i - w_1^\ast \cdot \frac{1}{3} \sum_{i=1}^3 x_i$$
Substituting values:
$$w_0^\ast = \frac{12}{3} - 2 \cdot \frac{6}{3} = 4 - 4 = 0$$

Thus, the optimal parameters are: $$w_0^\ast = 0, \quad w_1^\ast = 2$$
::::

# BEGIN SUBPROB

On a fourth weekend, due to a festival, she couldn't set up her stall
but managed to sell 2 jars to early customers who contacted her
directly. This data point is:

-   **Weekend 4**: Worked for 0 hours, sold 2 jars.

She now wants to understand how this outlier affects her overall
analysis. Fill out the table below based on the new data point
$x_4 = 0, y_4=2$ and then find the **new** optimal parameters $w_0'$ and
$w_1'$ for a simple least squares linear model. *Show all your
calculations.*

# BEGIN SOLUTION

# END SOLUTION

# END SUBPROB

::: center
+-----------------------+---------------------------------------------+
| $\sum_{i=1}^4 x_i$    | -----------------------------------------   |
+:=====================:+:===========================================:+
| $\sum_{i=1}^4 y_i$    | 14                                          |
+-----------------------+---------------------------------------------+
| $\sum_{i=1}^4 x_iy_i$ | 28                                          |
+-----------------------+---------------------------------------------+
| $\sum_{i=1}^4 x_i^2$  |                                             |
+-----------------------+---------------------------------------------+
:::

:::: responsebox
2.25in

::: center
    $\sum_{i=1}^4 x_i$     6
  ----------------------- ----
    $\sum_{i=1}^4 y_i$     14
   $\sum_{i=1}^4 x_iy_i$   28
   $\sum_{i=1}^4 x_i^2$    14
:::

To calculate the new parameters:

$$w_1' = \frac{\sum_{i=1}^4 x_i y_i - \frac{1}{4} \sum_{i=1}^4 x_i \sum_{i=1}^4 y_i}{\sum_{i=1}^4 x_i^2 - \frac{1}{4} \left( \sum_{i=1}^4 x_i \right)^2}$$
Substituting values:
$$w_1' = \frac{28 - \frac{1}{4}(6 \cdot 14)}{14 - \frac{1}{4}(6^2)} = \frac{28 - 21}{14 - 9} = \frac{7}{5} = 1.4$$

$$w_0' = \frac{1}{4} \sum_{i=1}^4 y_i - w_1' \cdot \frac{1}{4} \sum_{i=1}^4 x_i$$
Substituting values:
$$w_0' = \frac{14}{4} - 1.4 \cdot \frac{6}{4} = 3.5 - 2.1 = 1.4$$

Thus, the new parameters are: $$w_0' = 1.4, \quad w_1' = 1.4$$
::::

# BEGIN SUBPROB

On each axis below draw: **(i)** the scatterplot of the corresponding
data, and **(ii)** the line of best fit you found for the corresponding
dataset in the preceding parts.

# BEGIN SOLUTION

# END SOLUTION

# END SUBPROB

::: center
:::

:::: responsebox
2in

::: center
:::
::::

# BEGIN SUBPROB

Based on the pictures in part **(c)**, which dataset has greater mean
squared error with respect to its optimal parameters? Why? *You do not
need to calculate the errors by hand to answer this question. Explain
your reasoning.*

# BEGIN SOLUTION

# END SOLUTION

# END SUBPROB

::: responsebox
2in The dataset with Weekends 1, 2, 3, and 4 will have a greater mean
squared error. This is because the added outlier (Weekend 4) does not
follow the original perfect linear trend and introduces a discrepancy
between the data points and the new line of best fit.
:::

# END PROB