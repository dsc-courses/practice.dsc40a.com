# BEGIN PROB

\[**Bayes theorem**\]

1% of the population have a certain genetic defect.

# BEGIN SUBPROB

\[4 points\] A test has been developed such that 90% of administered
tests accurately detect the gene (true positives). What needs to be the
false positive probability (administered test are positive though the
patient doesn't have a genetic defect) so that the posterior probability
(a patient having the genetic defect given a positive result) is 90%?

::: responsebox
3.4in

-   Hypothesis: patient has the gene, $P(H) = 0.01$

-   Evidence: patient got a positive test result

-   True positive: Probability of positive test result if someone has
    the gene $P(E|H)=0.9$

-   False positive: Probability of positive test result if someone
    doesn't have the gene, denote $P(E|\bar{H}) = p$

$$\begin{aligned}
P(H|E)  &= \frac{ P(E|H)P(H)}{P(E)} \\
&=\frac{ P(E|H)P(H)}{P(E|H)P(H)+ P(E|\bar{H})P(\bar{H})}\\
&=\frac{0.9 * 0.01}{0.9 * 0.01 + p * 0.99} =0.9
\end{aligned}$$

Rearranging the terms $$\begin{aligned}
0.9 * 0.01 & = 0.9*(0.9 * 0.01 + p * 0.99)\\
0.1 * 0.9 * 0.01 & = 0.9* p * 0.99 \\ 
p =P(E|\bar{H}) &=\frac{0.1*0.01}{0.99}\approx0.001
\end{aligned}$$

The probability of a false positive (positive result for someone who
doesn't have the gene) needs to be 0.001.
:::

# BEGIN SOLUTION

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

\[4 points\] A test has been developed such that 1% of administered
tests are positive when the patient doesn't have the gene (false
positives). What needs to be the true positive probability so that the
posterior probability (probability a patient having the genetic defect
given a positive result) is 50%?

::: responsebox
3.8in

-   Hypothesis: patient has the gene, $P(H) = 0.01$

-   True positive: Probability of positive test result if someone has
    the gene, denote $P(E|H)=p$

-   False positive: Probability of positive test result if someone
    doesn't have the gene, denote $P(E|\bar{H}) = 0.01$

$$\begin{aligned}
P(H|E)  &= \frac{ P(E|H)P(H)}{P(E|H)P(H)+ P(E|\bar{H})P(\bar{H})}\\
&=\frac{p * 0.01}{p * 0.01 + 0.01 * 0.99} \\
&=\frac{p}{p  + 0.99} =0.5
\end{aligned}$$

Rearranging the terms $$\begin{aligned}
p  & = 0.5*(p  + 0.99)\\
0.5 * p  & = 0.5*  0.99 \\ 
p =P(E|{H}) &=0.99
\end{aligned}$$

The probability of a true positive needs to be 0.99.
:::

# BEGIN SOLUTION

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

\[4 points\] 1% of the population have a certain genetic defect. 1% of
administered tests are positive when the patient doesn't have the gene
(false positives). Show that there is no true positive probability such
that the probability of a patient having the genetic defect given a
positive result (the posterior) can be 90%. (Hint: remember a
probability $p$ needs to fulfill $0\leq p \leq 1$.)

::: responsebox
4in

-   Hypothesis: patient has the gene, $P(H) = 0.01$

-   True positive: Probability of positive test result if someone has
    the gene, denote $P(E|H)=p$

-   False positive: Probability of positive test result if someone
    doesn't have the gene, denote $P(E|\bar{H}) = 0.01$

Let's try solving as before: $$\begin{aligned}
P(H|E)  &=\frac{ P(E|H)P(H)}{P(E|H)P(H)+ P(E|\bar{H})P(\bar{H})}\\
&=\frac{p * 0.01}{p * 0.01 + 0.01 * 0.99} \\
&=\frac{p}{p  + 0.99} =0.9
\end{aligned}$$

Rearranging the terms $$\begin{aligned}
p  & = 0.9*(p  + 0.99)\\
0.1 * p  & = 0.9*  0.99 \\ 
p =P(E|{H}) &= \frac{0.99 * 0.9}{0.1} = 8.91 > 1
\end{aligned}$$

Given the rate of false positives, we cannot find a true positive rate
such that the posterior is 0.9.
:::

# BEGIN SOLUTION

# END SOLUTION

# END SUBPROB

# END PROB