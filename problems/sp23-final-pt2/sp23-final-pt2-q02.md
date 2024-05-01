# BEGIN PROB

<i>Source: [Spring 2023 Final Part 2](../sp23-final-pt2/index.html), Problem 2</i>

You roll a 12-sided die 8 times.

# BEGIN SUBPROB

What is the probability you roll 8 distinct values?

# BEGIN SOLUTION

$\dfrac{{12 \choose 8}\cdot8!}{12^8} = \dfrac{12}{12}\cdot\dfrac{11}{12}\cdot\dfrac{10}{12}\cdot\dots\cdot\dfrac{5}{12}$

The numerator ${12 \choose 8}\cdot8!$ is the number of total possible permutations of 8 distinct values; ${12 \choose 8}$ possible sets of 8 distinct values times $8!$ orderings, because the die could roll the same set of distinct values in $8!$ different ways. The denominator $12^8$ is the number of total possible outcomes. Altogether, dividing the numerator by the denominator gives us the probability of rolling 8 distinct values. 

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

What is the probability you roll exactly 7 distinct values?

# BEGIN SOLUTION

$\dfrac{{8 \choose 2}\cdot{12 \choose 7}\cdot7!}{12^8}$

# END SOLUTION

# END SUBPROB

# END PROB