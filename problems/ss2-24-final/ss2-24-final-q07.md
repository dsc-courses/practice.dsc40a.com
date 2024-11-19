# BEGIN PROB

You go to the (world-renowned) San Diego Safari Park. The
animals you see there appear at random, depending on the exhibit. The
probabilities of seeing an animal in a given exhibit (Plains, Forest,
and Jungle) are provided in the table below. For example, the
probability of seeing a Camel if you are in the African Plains is
$\frac{3}{5} = 60\%$, and the probability you do not see a Camel if you
are in the African Plains is the complement, $\frac{2}{5} = 40\%$. Note
that you may see multiple animals in each exhibit, so the probabilities
given in each row sum to well over 100%.

On the day you go to the Safari Park, the tram navigation system
malfunctions and takes you to exhibits at random. It takes guests to the
African Plains with probability $\frac{3}{5}$, the Gorilla Forest with
probability $\frac{1}{10}$, and the Hidden Jungle with probability
$\frac{3}{10}$.

::: {#tab:animal_probs_transposed}
    **Location**      **Rhino**        **Camel**       **Gazelle**      **Lemur**      **Fruit Bat**     **Gorilla**
  ---------------- ---------------- ---------------- --------------- ---------------- ---------------- ----------------
   African Plains   $\frac{3}{10}$   $\frac{3}{5}$    $\frac{1}{2}$   $\frac{1}{10}$         \-         $\frac{1}{4}$
   Gorilla Forest   $\frac{3}{10}$   $\frac{1}{10}$   $\frac{1}{5}$   $\frac{1}{4}$    $\frac{7}{20}$   $\frac{9}{20}$
   Hidden Jungle          \-               \-              \-         $\frac{1}{5}$    $\frac{2}{5}$          \-
:::

[]{#tab:animal_probs_transposed label="tab:animal_probs_transposed"}

In this question, you may leave your answers unsimplified, in terms of
fractions, exponents, factorials, the permutation formula $P(n, k)$, and
the binomial coefficient ${n \choose k}$.

# BEGIN SUBPROB

Assume you only go to one exhibit. What is the probability you see a
Lemur at the Safari Park? Show your work, and put a around your final
answer.

# BEGIN SOLUTION

Correctly uses law of total probability: 
P(Lemur) = P(Lemur|Plains)P(Plains) + P(Lemur|Forest)P(Forest) + P(Lemur|Jungle)P(Jungle)= $$\frac{1}{10}\cdot\frac{3}{5} + \frac{1}{4}\cdot\frac{1}{10} + \frac{1}{5}\cdot\frac{3}{10}$$.

TODO

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

Assume you only go to one exhibit, and you see a Lemur. What is the
probability you are at the African Plains? Show your work, and put a
around your final answer.

# BEGIN SOLUTION

Correctly uses Bayes' Theorem and answer using Law of Total Probability from above: 
Correctly uses law of total probability: 
P(Plains | Lemur) = $$\frac{\text{P(Lemur | Plains)P(Plains)}}{\text{P(Lemur)}} = \frac{\text{P(Lemur | Plains)P(Plains)}}{\text{P(Lemur|Plains)P(Plains) + P(Lemur|Forest)P(Forest) + P(Lemur|Jungle)P(Jungle)}}$$

$$ = \frac{\frac{1}{10}\cdot\frac{3}{5}}{\frac{1}{10}\cdot\frac{3}{5} + \frac{1}{4}\cdot\frac{1}{10} + \frac{1}{5}\cdot\frac{3}{10}} = \frac{12}{29}$$.

Not penalized again if an incorrect answer in **a** above is reused.

TODO

# END SOLUTION

# END SUBPROB

*The following information is repeated from the previous page, for your
convenience.*

You go to the (world-renowned) San Diego Safari Park. The animals you
see there appear at random, depending on the exhibit. The probabilities
of seeing an animal in a given exhibit (Plains, Forest, and Jungle) are
provided in the table below. For example, the probability of seeing a
Camel if you are in the African Plains is $\frac{3}{5} = 60\%$, and the
probability you do not see a Camel if you are in the African Plains is
the complement, $\frac{2}{5} = 40\%$. Note that you may see multiple
animals in each exhibit, so the probabilities given in each row sum to
well over 100%.

On the day you go to the Safari Park, the tram navigation system
malfunctions and takes you to exhibits at random. It takes guests to the
African Plains with probability $\frac{3}{5}$, the Gorilla Forest with
probability $\frac{1}{10}$, and the Hidden Jungle with probability
$\frac{3}{10}$.

::: {#tab:animal_probs_transposed}
    **Location**      **Rhino**        **Camel**       **Gazelle**      **Lemur**      **Fruit Bat**     **Gorilla**
  ---------------- ---------------- ---------------- --------------- ---------------- ---------------- ----------------
   African Plains   $\frac{3}{10}$   $\frac{3}{5}$    $\frac{1}{2}$   $\frac{1}{10}$         \-         $\frac{1}{4}$
   Gorilla Forest   $\frac{3}{10}$   $\frac{1}{10}$   $\frac{1}{5}$   $\frac{1}{4}$    $\frac{7}{20}$   $\frac{9}{20}$
   Hidden Jungle          \-               \-              \-         $\frac{1}{5}$    $\frac{2}{5}$          \-
:::

[]{#tab:animal_probs_transposed label="tab:animal_probs_transposed"}

# BEGIN SUBPROB

Suppose you visit the Hidden Jungle four times. What is the probability
you see a Fruit Bat at least once? Show your work, and put a around your
final answer.

# BEGIN SOLUTION

Correct: $$1 - (\frac{3}{5})^4 = 1 - (1 - \frac{2}{5})^4$$

$$ = 1 - (1 - P(\text{Fruit Bat | Hidden Jungle}))^4$$

$$ = P(\text{at least 1 Fruit Bat} | \text{Hidden Jungle})$$

TODO

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

Suppose you visit the African Plains. What is the probability you see a
Rhino or a Gazelle? Assume the two events are independent. Show your
work, and put a around your final answer.

# BEGIN SOLUTION

Correctly uses inclusion-exclusion for addition rule:

P(Rhino OR Gazelle) = P(Rhino) + P(Gazelle) - P(Rhino AND Gazelle) = $$\frac{3}{10} + \frac{1}{2} - \frac{3}{10} \cdot \frac{1}{2} =\frac{6}{20} + \frac{10}{20} - \frac{3}{20} = \frac{13}{20}$$

TODO

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

In the African Plains, the probability you see a Rhino, given a Gazelle
is present, is $\frac{2}{5}$, and the probability you see a Camel, given
a Gazelle is present, is $\frac{7}{10}$. If the probability you see both
a Rhino and Camel, given a Gazelle is present, is $\frac{3}{5}$, are the
two events conditionally independent?

( ) Yes
( ) No

# BEGIN SOLUTION

Correct: answers "No", since $$\frac{3}{5} \neq \frac{2}{5} \times \frac{7}{10}$$.

TODO

# END SOLUTION

# END SUBPROB

# END PROB