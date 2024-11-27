# BEGIN PROB

<i>Source: [Summer Session 2 2024 Final](../ss2-24-final/index.html), Problem 8</i>

The San Diego Safari Park has one of the world's most successful cheetah
breeding programs. To support this, they keep track of their cheetahs'
characteristics. For each cheetah, the Safari Park keeps track of:

-   Whether **color** of the cheetah's fur; golden or dark.

-   The **length** of the cheetah's claws; short or long.

-   The cheetah's **development**; whether it is young, adolescent, or
    mature.

We're given the following information about the cheetahs in the park:

-   $P(\text{Young}) = 0.25$

-   $P(\text{Adolescent}) = 0.40$

-   $P(\text{Mature}) = 0.35$

-   $P(\text{Short Claws} \mid \text{Young}) = 0.70$

-   $P(\text{Dark Fur} \mid \text{Young}) = 0.80$

-   $P(\text{Long Claws} \mid \text{Adolescent}) = 0.40$

-   $P(\text{Golden Fur} \mid \text{Adolescent}) = 0.50$

-   $P(\text{Long Claws} \mid \text{Mature}) = 1$

-   $P(\text{Dark Fur} \mid \text{Mature}) = 0.10$

A new cheetah is observed with **dark fur** and **short claws**.
Assuming conditional independence of features (color, length) within a
class (development), calculate the probability that this cheetah is
**young** using Bayes' Theorem. In this question, you may leave your
answers unsimplified, in terms of fractions, exponents, factorials, the
permutation formula $P(n, k)$, and the binomial coefficient
${n \choose k}$.

# BEGIN SOLUTION

$\frac{7}{13}$

To calculate the probability that a cheetah is young given that it has dark fur and short claws we can use Bayes' Theorem!

$$\frac{P(\text{Dark Fur} \cap \text{Short Claws} | \text{Young}) \cdot P(\text{Young})}{P(\text{Dark Fur} \cap \text{Short Claws})}$$

We first need to calculate: $P(\text{Dark Fur} \cap \text{Short Claws} | \text{Young})$.

We can do this using the equation: $P(\text{Dark Fur} \cap \text{Short Claws} | \text{Young}) = P(\text{Dark Fur} | \text{Young}) \cdot P(\text{Short Claws} | \text{Young})$.

We are given:

- $P(\text{Dark Fur} \mid \text{Young}) = 0.80$
- $P(\text{Short Claws} \mid \text{Young}) = 0.70$

This means: $$P(\text{Dark Fur} \cap \text{Short Claws} | \text{Young}) = 0.8 \cdot 0.7 = 0.56$$

Notice the denominator of our Bayes' Theorem is $P(\text{Dark Fur} \cap \text{Short Claws})$ this means we need to probability of seeing Dark Fur or Short Claws regardless of the development stage.

This follows the equation for the law of total probability:

\begin{align*}
P(\text{Dark Fur} \cap \text{Short Claws}) &= P(\text{Dark Fur} \cap \text{Short Claws} | \text{Young}) * P(\text{Young})\\
&+ P(\text{Dark Fur} \cap \text{Short Claws} | \text{Adolescent}) * P(\text{Adolescent})\\
&+ P(\text{Dark Fur} \cap \text{Short Claws} | \text{Mature}) * P(\text{Mature})
\end{align*}

This means we need to calculate: $P(\text{Dark Fur} \cap \text{Short Claws} | \text{Adolescent})$ and $P(\text{Dark Fur} \cap \text{Short Claws} | \text{Mature})$.

**For Adolescent we are given:**

- $P(\text{Golden Fur} \mid \text{Adolescent}) = 0.50$
- $P(\text{Long Claws} \mid \text{Adolescent}) = 0.40$

We have to take the compliments of these qualities to get short claws and dark fur!

- $P(\text{Dark Fur} \mid \text{Adolescent}) = 1 - P(\text{Golden Fur} \mid \text{Adolescent}) = 1 - 0.50 = 0.5$
- $P(\text{Short Claws} \mid \text{Adolescent}) = 1 - P(\text{Long Claws} \mid \text{Adolescent}) = 1 - 0.40 = 0.6$

This means: $$P(\text{Dark Fur} \cap \text{Short Claws} | \text{Adolescent}) = 0.5 \cdot 0.6 = 0.3$$

**For Mature we are given:**

- $P(\text{Long Claws} \mid \text{Mature}) = 1$
- $P(\text{Dark Fur} \mid \text{Mature}) = 0.10$

We have to take the compliments of long claws to get short claws!

- $P(\text{Dark Fur} \mid \text{Mature}) = 1 - P(\text{Golden Fur} \mid \text{Mature}) = 1 - 1 = 0$

This means: $$P(\text{Dark Fur} \cap \text{Short Claws} | \text{Mature}) = 0 \cdot 0.1 = 0$$

To finally calculate the denominator we need these probabilities:

-   $P(\text{Young}) = 0.25$
-   $P(\text{Adolescent}) = 0.40$
-   $P(\text{Mature}) = 0.35$

Now we can simply plug our numbers into the equation!

\begin{align*}
P(\text{Dark Fur} \cap \text{Short Claws}) &= P(\text{Dark Fur} \cap \text{Short Claws} | \text{Young}) * P(\text{Young})\\
&+ P(\text{Dark Fur} \cap \text{Short Claws} | \text{Adolescent}) * P(\text{Adolescent})\\
&+ P(\text{Dark Fur} \cap \text{Short Claws} | \text{Mature}) * P(\text{Mature})\\
&= 0.56 \cdot 0.25 + 0.3 * 0.4 + 0 * 0.35 \\
&= 0.14 + 0.12\\
&= 0.26
\end{align*}

Now we have all the components to answer the question: 

$$\frac{P(\text{Dark Fur} \cap \text{Short Claws} | \text{Young}) \cdot P(\text{Young})}{P(\text{Dark Fur} \cap \text{Short Claws})} = \frac{0.56 \cdot 0.25}{0.26} = \frac{7}{13}$$


<average>50</average>

# END SOLUTION

# END PROB