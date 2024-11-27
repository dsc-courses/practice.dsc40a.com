# BEGIN PROB

<i>Source: [Summer Session 2 2024 Final](../ss2-24-final/index.html), Problem 9</i>

Information about a sample of $50$ cheetahs in the San Diego Safari Park is summarized in the table below.

<br>

|                    | Golden Fur            |                        | Dark Fur            |                        | Sum of Row |
|--------------------|-----------------------|------------------------|---------------------|------------------------|------------|
|                    | **Short Claws** | **Long Claws** | **Short Claws** | **Long Claws** |            |
| **Young**              | 2           | 0          | 10          | 4          | 16         |
| **Adolescent**         | 6           | 3          | 2           | 6          | 17         |
| **Mature**             | 3           | 12         | 0           | 2          | 17         |
| **Sum of Column**  | 11          | 15         | 12          | 12         | 50         |

<br>

For instance, we're told that $10$ cheetahs with dark fur and short claws
are young and that there were $11$ cheetahs with golden fur and short
claws.

Given its other characteristics, San Diego Safari Park would like to use
this information to predict whether a new cheetah to the Park is young,
adolescent, or mature.

A new cheetah is observed with **golden fur** and **long claws**. Using
the data in the table and assuming conditional independence of features,
use the Naive Bayes formula **with smoothing** to determine which
developmental stage is most likely for the new cheetah. In this
question, you may leave your answers unsimplified, in terms of
fractions, exponents, factorials, the permutation formula $P(n, k)$, and
the binomial coefficient ${n \choose k}$.


# BEGIN SOLUTION

Mature

To figure out if the new cheetah is young, adolescent, or mature we need to find the probabilities for each stage of development.

This means we need to find the probability of a young cheetah having golden fur and long claws, the probability of a adolenscent cheetah having golden fur and long claws, and the probability of a mature cheetah having golden fur and long claws.

Let Age represent either Young, Adolescent, or Mature. We need to then follow the equation: $$P(\text{Age}|\text{Golden Fur} \cap \text{Long Claws}) = P(\text{Age}) \cdot P(\text{Golden Fur}|\text{Age}) \cdot P(\text{Long Claws}|\text{Age})$$ for all the different ages.

Recall we will also be using smoothing! This means:

$$P(\text{Feature}|\text{Class}) = \frac{\text{Count of Features in Class} + 1}{\text{Total in Class} + \text{Number of Possible Feature Values}}$$

**When Age = Young:**

- $P(\text{Young}) = \frac{16}{50}$
- $P(\text{Golden Fur}|\text{Young}) = \frac{2 + 0 + 1}{16 + 2} = \frac{3}{18}$
- $P(\text{Long Claws}|\text{Young}) = \frac{0 + 1}{16 + 2} = \frac{5}{18}$

\begin{align*}
P(\text{Young}|\text{Golden Fur} \cap \text{Long Claws}) &= P(\text{Young}) \cdot P(\text{Golden Fur}|\text{Young}) \cdot P(\text{Long Claws}|\text{Young})\\
&= \frac{3}{18} \cdot \frac{5}{18} \cdot \frac{16}{50}\\
&= \frac{2}{135}
\end{align*}

**When Age = Adolescent:**

- $P(\text{Adolescent}) = \frac{17}{50}$
- $P(\text{Golden Fur}|\text{Adolescent}) = \frac{6 + 3 + 1}{17 + 2} = \frac{10}{19}$
- $P(\text{Long Claws}|\text{Adolescent}) = \frac{3 + 6 + 1}{17 + 2} = \frac{10}{19}$

\begin{align*}
P(\text{Adolescent}|\text{Golden Fur} \cap \text{Long Claws}) &= P(\text{Adolescent}) \cdot P(\text{Golden Fur}|\text{Adolescent}) \cdot P(\text{Long Claws}|\text{Adolescent})\\
&= \frac{10}{19} \cdot \frac{10}{19} \cdot \frac{17}{50}\\
&= \frac{34}{361}
\end{align*}

**When Age = Mature:**

- $P(\text{Mature}) = \frac{17}{50}$
- $P(\text{Golden Fur}|\text{Mature}) = \frac{3 + 12 + 1}{17 + 2} = \frac{16}{19}$
- $P(\text{Long Claws}|\text{Mature}) = \frac{12 + 2 + 1}{17 + 2} = \frac{15}{19}$

\begin{align*}
P(\text{Mature}|\text{Golden Fur} \cap \text{Long Claws}) &= P(\text{Mature}) \cdot P(\text{Golden Fur}|\text{Mature}) \cdot P(\text{Long Claws}|\text{Mature})\\
&= \frac{16}{19} \cdot \frac{15}{19} \cdot \frac{17}{50}\\
&= \frac{408}{1805}
\end{align*}

When age is Mature then it has the highest probability, which means we predict the new cheetah is mature.

<average>59</average>

# END SOLUTION

# END PROB