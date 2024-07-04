# BEGIN PROB

Delta's flight operations center keeps track of weather conditions, as
they tend to impact whether or not flights are late. For each flight,
Delta keeps track of:

-   Whether or not there was **precipitation** --- i.e., rain, snow, or
    hail.

-   The **wind conditions** --- either no winds, light winds, moderate
    winds, or heavy winds.

-   The flight's **status** --- whether it was early, on time, or late.

Information about 100 flights is summarized in the table below.

::: center
![image](final-images/naive-bayes.png){width="90%"}
:::

For instance, we're told that 6 flights in moderate winds and no
precipitation landed late, and that there were 13 total flights in heavy
winds and precipitation.

Delta would like to use this information to predict whether a new flight
will be early, on time, or late, given the weather conditions.

# BEGIN SUBPROB

**Without smoothing**, what is:

$$\mathbb{P}(\text{heavy winds} \: | \: \text{early})$$

( ) $\frac{2}{7}$ ( ) $\frac{5}{7}$ ( ) $\frac{3}{8}$ ( ) $\frac{3}{10}$
( ) $\frac{14}{15}$ ( ) $\frac{3}{28}$ ( ) $\frac{5}{28}$

# BEGIN SOLUTION

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

**With smoothing**, what is:

$$\mathbb{P}(\text{heavy winds} \: | \: \text{early})$$

( ) $\frac{1}{3}$ ( ) $\frac{3}{8}$ ( ) $\frac{3}{11}$ ( )
$\frac{9}{29}$ ( ) $\frac{9}{32}$ ( ) $\frac{31}{101}$ ( )
$\frac{31}{104}$

# BEGIN SOLUTION

# END SOLUTION

# END SUBPROB

For your convenience, the table from the previous page is repeated again
below.

::: center
![image](final-images/naive-bayes.png){width="90%"}
:::

# BEGIN SUBPROB

An airline's late-to-early ratio, given a set of weather conditions, is
defined as:

$$\frac{\mathbb{P}(\text{late} \: | \: \text{conditions})}{\mathbb{P}(\text{early} \: | \: \text{conditions})}$$

Using the assumptions of the Naïve Bayes classifier **without
smoothing**, show that Delta's late-early ratio for flights in **heavy
winds and precipitation** is $\bf{\frac{7}{5}}$.

*Hint: You'll end up needing to compute 6 probabilities, one of which
you already found in **part (a)**.*

::: responsebox
3.75in
:::

# BEGIN SOLUTION

# END SOLUTION

# END SUBPROB

# END PROB