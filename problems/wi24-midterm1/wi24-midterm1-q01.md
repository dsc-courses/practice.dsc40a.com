# BEGIN PROB

_Originally Problem 1 on the first Winter 2024 Midterm Exam._

Consider a dataset $D$ with 5 data points
$\{7,5,1,2,a\}$, where a is a positive real number. Note that $a$ is not
necessarily an integer.

# BEGIN SUBPROB

Express the mean of $D$ as a function of $a$, simplify the
expression as much as possible.

# BEGIN SOLUTION

$$\text{Mean($D$)} = \frac{a}{5} + 3$$

# END SOLUTION

# END SUBPROB 

# BEGIN SUBPROB

Depending on the range of $a$, the median of $D$ could assume
one of three possible values. Write out all possible median of $D$ along
with the corresponding range of $a$ for each case. Express the ranges
using double inequalities, e.g., i.e. $3<a\leq8$:


# BEGIN SOLUTION

$$\begin{cases}
\text{Median($D$)} = 2 & \text{if a is in the range of } 0<a\leq2 \\
\text{Median($D$)} = a & \text{if a is in the range of } 2<a\leq5 \\
\text{Median($D$)} = 5 & \text{if a is in the range of } 5<a\leq\infty \\
\end{cases}$$

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

Given that $Mean_{d} < Median_{D}$, determine the range of
$a$ that satisfies this condition. make sure to show your work

::: mdframed
**Range of a:**

**Supporting Work:**
:::

# BEGIN SOLUTION

Since there are 3 possible median values, we will have to discuss each
situation separately. In case 1, when $0<a\leq2$, $Median_{D} = 2$,
therefore we have: $$\begin{aligned}
            3 + \frac{a}{5} < 2\\
            a<-5
        
\end{aligned}$$ But $a<-5$ is in conflict with the condition $0<a\leq2$,
therefore there is no solution in this situation, and $Median_{D} = 2$
is impossible.

In case 2 when $2<a<5$, $Median_{D} = a$, therefore we have:
$$\begin{aligned}
            3 + \frac{a}{5} < a\\
            3 < \frac{4}{5} a\\
           a > \frac{15}{4}\\
        
\end{aligned}$$ So $a$ has to be larger than $\frac{15}{4}$. But
remember from the prerequisite condition that $2<a<5$. To satisfy both
conditions, we must have $\frac{15}{4}<a<5$.

In case 3 when $a\geq5$, $Median_{D} = 5$, therefore we have:
$$\begin{aligned}
        3 + \frac{a}{5} < 5\\
        a<10
    
\end{aligned}$$ combining with the prerequisite condition, we have
$5\leq a<10$

Combining the range of case 2 and 3, we have $\frac{15}{4}<a<10$ as our
final answer.

# END SOLUTION

# END SUBPROB

# END PROB