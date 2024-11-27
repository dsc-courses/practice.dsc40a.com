# BEGIN PROB

<i>Source: [Summer Session 2 2024 Final](../ss2-24-final/index.html), Problem 7a-e</i>

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

In this question, you may leave your answers unsimplified, in terms of
fractions, exponents, factorials, the permutation formula $P(n, k)$, and
the binomial coefficient ${n \choose k}$.

# BEGIN SUBPROB

Assume you only go to one exhibit. What is the probability you see a
Lemur at the Safari Park? Show your work, and put a around your final
answer.

# BEGIN SOLUTION

$$\frac{1}{10}\cdot\frac{3}{5} + \frac{1}{4}\cdot\frac{1}{10} + \frac{1}{5}\cdot\frac{3}{10}$

To solve this problem we need to use the law of total probability. Recall the law of total probability is: $P(A) = \sum_{i=1}^n P(A \mid B_i) P(B_i)$ where $B_i$ is a partition of a sample sapce that are mutually exclusive and collectively exhaustive.

To use the law of total probability here we need to look at the three different instances one may see a lemur! We can see that the lemur is present in the Plains, Forest, and Jungle. This means our equation will look like:

$$P(\text{Lemur}) = P(\text{Lemur}|\text{Plains})P(\text{Plains}) + P(\text{Lemur}|\text{Forest})P(\text{Forest}) + P(\text{Lemur}|\text{Jungle})P(\text{Jungle})$$

We are given the conditional probabilities in the table:

- $P(\text{Lemur}|\text{Plains}) = \frac{1}{10}$
- $P(\text{Lemur}|\text{Forest})= \frac{1}{4}$
- $P(\text{Lemur}|\text{Jungle}) = \frac{1}{5}$

In the directions we are given:

- $P(\text{Plains}) = \frac{3}{5}$
- $P(\text{Forest}) = \frac{1}{10}$
- $P(\text{Jungle}) = \frac{3}{10}$

Now all we have to do is plug them into the equation!

$$\frac{1}{10}\cdot\frac{3}{5} + \frac{1}{4}\cdot\frac{1}{10} + \frac{1}{5}\cdot\frac{3}{10}$$

Recall we can leave our answer unsimplified!

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

Assume you only go to one exhibit, and you see a Lemur. What is the
probability you are at the African Plains? Show your work, and put a
around your final answer.

# BEGIN SOLUTION

$\frac{\frac{1}{10}\cdot\frac{3}{5}}{\frac{1}{10}\cdot\frac{3}{5} + \frac{1}{4}\cdot\frac{1}{10} + \frac{1}{5}\cdot\frac{3}{10}} = \frac{12}{29}$

To solve this question we need to use Bayes' Theorem and the law of total probability from part a.

$$\frac{P(\text{Lemur}|\text{Plains})}{P(\text{Lemur})}$$

We know from part a that:

\begin{align*}
P(\text{Lemur}) &= \frac{1}{10}\cdot\frac{3}{5} + \frac{1}{4}\cdot\frac{1}{10} + \frac{1}{5}\cdot\frac{3}{10}\\
&= \frac{3}{50}+\frac{1}{40}+\frac{3}{50}\\
&= \frac{29}{200}
\end{align*}

and that $P(\text{Lemur}|\text{Plains}) = \frac{1}{10}$.

All we have to do is now combine them!

$$\frac{\text{P(Lemur | Plains)P(Plains)}}{\text{P(Lemur)}} = \frac{\frac{3}{50}}{\frac{29}{200}} = \frac{12}{29}$$

# END SOLUTION

# END SUBPROB

*The following information is repeated from the previous page, for your convenience.*

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

$1 - (\frac{3}{5})^4$

The best way to solve this problem is by using the compliment rule. We can calculate the probability of not seeing a Fruit Bat in the Hidden Jungle: $1 - P(\text{Fruit Bat | Hidden Jungle}) = 1 - \frac{2}{5} = \frac{3}{5}$. We then need to put this fraction to the power of $4$ for the four independent observations. $\frac{3}{5}^4$ says we never see the Fruit Bat in the four times we have been to the Hidden Jungle. Now we use the compliment rule again! $1 - \frac{3}{5}^4$ gives us the probability of seeing at least one Fruit Bat in 4 observations!

Essentially, $1 - (1 - P(\text{Fruit Bat | Hidden Jungle}))^4 = P(\text{at least 1 Fruit Bat} | \text{Hidden Jungle})$.

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

Suppose you visit the African Plains. What is the probability you see a
Rhino or a Gazelle? Assume the two events are independent. Show your
work, and put a around your final answer.

# BEGIN SOLUTION

$\frac{3}{10} + \frac{1}{2} - \frac{3}{10} \cdot \frac{1}{2} =\frac{6}{20} + \frac{10}{20} - \frac{3}{20} = \frac{13}{20}$

To solve this problem we know we will need to use Inclusion-Exclusion Principle ($P(\text{Rhino} \cup \text{Gazelle}) = P(\text{Rhino}) + P(\text{Gazelle}) - P(\text{Rhino} \cap \text{Gazelle})$).

We are in the African Plains! This means:

- $P(\text{Rhino}) = \frac{3}{10}$
- $P(\text{Gazelle}) = \frac{1}{2}$

Since we are told the two events are independent we can do: $P(\text{Rhino} \cap \text{Gazelle}) = P(\text{Rhino}) \cdot P(\text{Gazelle}) = \frac{3}{10} \cdot \frac{1}{2} = \frac{3}{20}$.

Now we just plug into the Inclusion-Exclusion Principle:

\begin{align*}
P(\text{Rhino} \cup \text{Gazelle}) &= P(\text{Rhino}) + P(\text{Gazelle}) - P(\text{Rhino} \cap \text{Gazelle})\\
&= \frac{3}{10} + \frac{1}{2} - \frac{3}{10} \cdot \frac{1}{2} \\
&= \frac{6}{20} + \frac{10}{20} - \frac{3}{20}\\
&= \frac{13}{20}
\end{align*}

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

No

Two events are conditionally independent given a third event if: $P(A \cap B | C) = P(A|C) \cdot P(B|C)$.

We can replace the variables for our scenario: $P(\text{Rhino} \cap \text{Camel})|\text{Gazelle} = P(\text{Rhino}|\text{Gazelle}) \cdot P(\text{Camel}|\text{Gazelle})$.

We are given:

- $P(\text{Rhino}|\text{Gazelle}) = \frac{2}{5}$
- $P(\text{Camel}|\text{Gazelle}) = \frac{7}{10}$
- $P(\text{Rhino} \cap \text{Camel})|\text{Gazelle} = \frac{3}{5}$

We can simply plug the given values into the equation to see if it holds: $$\frac{2}{5} \cdot \frac{7}{10} = \frac{7}{25}$$

This means the answer is "No" because $\frac{3}{5} \neq \frac{7}{25}$.

# END SOLUTION

# END SUBPROB

# END PROB