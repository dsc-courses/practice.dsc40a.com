# BEGIN PROB

<!-- <i>Source: [Winter 2022 Midterm 1](../wi22-midterm1/index.html), Problem 1</i> -->

Consider a dataset of $n$ values, $y_1, y_2, ..., y_n$, where $y_1 < y_2 < ... < y_n$. Let $R_\text{abs}(h)$ be the mean absolute error of a constant prediction $h$ on this dataset of $n$ values.

Suppose that we introduce a new value to the dataset, $\alpha$. Let $S_\text{abs}(h)$ be the mean absolute error of a constant prediction $h$ on this new dataset of $n + 1$ values.

We're given that:

-  $n > 5$.
-  $\alpha$ is not equal to any of $y_1, y_2, ..., y_n$. 
-  All values of $h$ between 7 and 9 minimize $S_\text{abs}(h)$.
-  The slope of $S_\text{abs}(h)$ on the line segment immediately to the right of $\alpha$ is $\frac{5-n}{1 + n}$.

# BEGIN SUBPROB

In the problem statement, we were told that ``all values between 7 and 9 minimize $S_\text{abs}(h)$." More specifically, what interval of values $h$ minimize $S_\text{abs}(h)$? 

\bubble{$7 < h < 9$} \bubble{$7 \leq h < 9$} \bubble{$7 < h \leq 9$} \bubble{$7 \leq h \leq 9$}

# BEGIN SOLUTION

TODO

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

Which value(s) minimize $R_\text{abs}(h)$? Give your answer(s) as integer(s) with no variables. Show your work, and put a $\boxed{\text{box}}$ around your final answer(s).

<i>Hint: Don't start by trying to expand $\frac{1}{n} \sum_{i = 1}^n |y_i - h|$ --- instead, think about what removing $\alpha$ does.</i>

# BEGIN SOLUTION

TODO

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

What is the slope of $S_\text{abs}(h)$ on the line segment immediately to the left of $\alpha$? Give your answer in the form of an expression involving $n$. Show your work, and put a $\boxed{\text{box}}$ around your final answer.

# BEGIN SOLUTION

TODO

# END SOLUTION

# END SUBPROB

# END PROB