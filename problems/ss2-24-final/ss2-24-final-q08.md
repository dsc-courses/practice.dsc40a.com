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

Correctly calculates all of the probabilities for 
$$\frac{P(\text{Dark Fur} \cap \text{Short Claws} | \text{Young}) \cdot P(\text{Young})}{P(\text{Dark Fur} \cap \text{Short Claws})}$$, and arrives at the correct answer of $$\frac{7}{13}$$, or an equivalent form.

<average>50</average>

# END SOLUTION

# END PROB