# BEGIN PROB

<i>Originally Problem 1 on the Spring 2023 Final Part 1</i>

For a given dataset $\{y_1, y_2, \dots, y_n\}$, let
$M_{abs}(h)$ represent the **median** absolute error of the constant
prediction $h$ on that dataset (as opposed to the mean absolute error
$R_{abs}(h)$).

# BEGIN SUBPROB

(3 points) For the dataset $\{4, 9, 10, 14, 15\}$, what is $M_{abs}(9)$?

$M_{abs}(9) =$

# BEGIN SOLUTION

$5$

TODO

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

For the same dataset $\{4, 9, 10, 14, 15\}$, find another
integer $h$ such that $M_{abs}(9) = M_{abs}(h)$.

$h =$

# BEGIN SOLUTION

$5$ or $15$

TODO

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

Based on your answers to parts (a) and (b), discuss in **at
most two sentences** what is problematic about using the median absolute
error to make predictions.

# BEGIN SOLUTION

The numbers 5 and 15 are clearly bad predictions (close to the
extreme values in the dataset), yet they are considered just as good a
prediction by this metric as the number 9, which is roughly in the
center of the dataset. Intuitively, 9 is a much better prediction, but
this way of measuring the quality of a prediction does not recognize
that.

# END SOLUTION

# END SUBPROB

# END PROB