# BEGIN PROB

Information about a sample of 50 cheetahs in the San Diego Safari Park
is summarized in the table below.

<!-- ::: center
![image](final-images/su24_bayes.png){width="90%"}
::: -->

(In the assets/images/su-final)

For instance, we're told that 10 cheetahs with dark fur and short claws
are young and that there were 11 cheetahs with golden fur and short
claws.

Given its other characteristics, San Diego Safari Park would like to use
this information to predict whether a cheetah new to the Park is young,
adolescent, or mature.

A new cheetah is observed with **golden fur** and **long claws**. Using
the data in the table and assuming conditional independence of features,
use the Naive Bayes formula **with smoothing** to determine which
developmental stage is most likely for the new cheetah. In this
question, you may leave your answers unsimplified, in terms of
fractions, exponents, factorials, the permutation formula $P(n, k)$, and
the binomial coefficient ${n \choose k}$.


# BEGIN SOLUTION

Correctly calculates the probabilities for each stage of development:

$$P(\text{Young}) \propto \frac{3}{18} \cdot \frac{5}{18} \cdot \frac{16}{50}$$ 

$$P(\text{Adolescent}) \propto \frac{10}{19} \cdot \frac{10}{19} \cdot \frac{17}{50}$$ 

$$P(\text{Mature}) \propto \frac{16}{19} \cdot \frac{15}{19} \cdot \frac{17}{50}$$

And predicts Mature 

If a student does not receive this rubric item, they should only receive **one** of the other rubric items.

TODO

# END SOLUTION

# END PROB