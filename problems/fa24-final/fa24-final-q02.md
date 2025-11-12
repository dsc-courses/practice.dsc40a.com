# BEGIN PROB

\[(12 points)\] Suppose you are designing a central temperature control
system for a network of $n\geq 1$ houses in a small town. Each house $i$
has a preferred temperature $y_i$, and the importance of satisfying
house $i$'s preference is represented by a weight $a_i > 0$, which
represents the number of residents in each house.

The system is set to maintain a single uniform temperature $h$ across
all houses. To minimize dissatisfaction, you aim to minimize the
weighted squared error:

$$R(h) = \frac{1}{n}\sum_{i=1}^n a_i (y_i - h)^2.$$

# BEGIN SUBPROB

Find a formula for the optimal temperature $h^\ast$ in terms of the
various preferred temperatures $y_1,\dotsc, y_n$. *Show all your
calculations.*

# BEGIN SOLUTION

# END SOLUTION

# END SUBPROB

::: responsebox
2in To minimize the function $R(h) = \sum_{i=1}^n a_i (y_i - h)^2$, we
differentiate $R(h)$ with respect to $h$ and set the derivative equal to
zero:
$$\frac{dR(h)}{dh} = \frac{d}{dh} \sum_{i=1}^n a_i (y_i - h)^2 = -2 \sum_{i=1}^n a_i (y_i - h).$$
Setting $\frac{dR(h)}{dh} = 0$, we get:
$$\sum_{i=1}^n a_i y_i - \sum_{i=1}^n a_i h = 0.$$ Simplifying:
$$h \sum_{i=1}^n a_i = \sum_{i=1}^n a_i y_i.$$ Solving for $h^\ast$:
$$h^\ast = \frac{\sum_{i=1}^n a_i y_i}{\sum_{i=1}^n a_i}.$$ Thus, the
optimal temperature $h^\ast$ is the weighted average of the preferred
temperatures.
:::

# BEGIN SUBPROB

Suppose that the family which lives in house $1$ has a baby, and their
weight $a_1$ increases by one. Assuming their preferred temperature does
not change, find an expression which relates the *new* optimal
temperature $h'$ to the old optimal temperature $h^\ast$ you found in
(a). *Show all your calculations.*

# BEGIN SOLUTION

# END SOLUTION

# END SUBPROB

::: responsebox
2in Let $h'$ denote the new optimal temperature. The new weight for
house $1$ becomes $a_1' = a_1 + 1$. Using the formula for $h^\ast$, the
new optimal temperature is:
$$h' = \frac{(a_1 + 1)y_1 + \sum_{i=2}^n a_i y_i}{(a_1 + 1) + \sum_{i=2}^n a_i}.$$
Expanding $h'$:
$$h' = \frac{a_1 y_1 + y_1 + \sum_{i=2}^n a_i y_i}{a_1 + 1 + \sum_{i=2}^n a_i}= \frac{ y_1 + \sum_{i=1}^n a_i y_i}{  1 + \sum_{i=1}^n a_i}.$$
Factoring out the original terms for $h^\ast$:
$$h' = \frac{h^\ast \sum_{i=1}^n a_i + y_1}{\sum_{i=1}^n a_i + 1}.$$
This relates the new optimal temperature $h'$ to the original $h^\ast$
by accounting for the additional weight and the corresponding
preference.
:::

# BEGIN SUBPROB

You and your colleagues are discussing new and improved ways to set the
weights used in the cost function. Your team comes up with three
alternatives for setting the weights:

-   $a_i = (\text{the number of residents in house $i$})$,

-   $b_i = 1$ for all houses,

-   $c_i = 1/(\text{the number of windows in house $i$})$.

Assume each house is occupied by at least one person and has at least
one window. Let

-   $A$ denote the optimal risk of $R(h)$ with respect to the weights
    $a_i$

-   $B$ denote the optimal risk of $R(h)$ with respect to the weights
    $b_i$

-   $C$ denote the optimal risk of $R(h)$ with respect to the weights
    $c_i$

**Using the relations** $<,\leq,>,\geq,=$, rank the numbers $A,B,C$ from
least to greatest. *Explain your reasoning and don't forget about the
baby!*

# BEGIN SOLUTION

# END SOLUTION

# END SUBPROB

::: responsebox
3in Note that for any choice of $h$, we have the following inequalities:
$$\sum_{i=1}^n c_i (y_i - h)^2\leq \sum_{i=1}^n b_i (y_i - h)^2 <\sum_{i=1}^n a_i (y_i - h)^2.$$
since $c_i \leq 1$ for all $i$, $b_i = 1$ for all $i$, and $a_i\geq 1$
for all $i$. Therefore the minimum values for each such function with
respect to $h$ will follow these inequalities. That is, $$C\leq B < A.$$

(Note we also accepted solution $C\leq B \leq A$ for those who forgot
about the baby ;) )
:::

# END PROB