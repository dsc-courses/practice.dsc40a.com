# BEGIN PROB

\[(13 points)\]

Robert has a sock drawer containing exactly eight socks: one pair each
of plain socks, dotted socks, striped socks, and plaid socks.

# BEGIN SUBPROB

On Monday morning while getting ready, Robert selects two socks at
random from the drawer. What is the probability that the socks are
matching? *Explain your reasoning.*

# BEGIN SOLUTION
::: responsebox
1in There are ${8\choose 2}$ ways to pick the two socks from the drawer,
of which exactly four pairs are matching. Therefore the probability is
$$\frac{4}{{8\choose 2}} = \frac{(4)(2)}{(8)(7)} = \frac{1}{7}.$$
:::
# END SOLUTION

# END SUBPROB



# BEGIN SUBPROB

After wearing the socks on Monday he places them in a laundry basket
separate from the drawer. On Tuesday morning, as Robert gets ready, he
selects another two socks at random from the six remaining in the
drawer. What is the probability that the socks are matching on Tuesday?
*Show all your calculations.*

# BEGIN SOLUTION
We can condition on whether the socks were matching on Monday and use this information to our advantage. Specifically,

$$
\begin{align*}
P[\text{match on Tues.}] &= P[\text{match on Tues.}|\text{match on Mon.}]P[\text{match on Mon.}] \\
&+ P[\text{match on Tues.}|\text{don't match on Mon.}]P[\text{don't match on Mon.}] \\
&= P[\text{match on Tues.}|\text{match on Mon.}]\frac{1}{7} \\
&+ P[\text{match on Tues.}|\text{don't match on Mon.}]\left(1 - \frac{1}{7}\right)
\end{align*}
$$

If the socks were matching on Monday, there are now three pairs of matching socks in the drawer. So we have, by the same logic as before,

$$
\begin{align*}
P[\text{match on Tues.}|\text{match on Mon.}] &= \frac{3}{\binom{6}{2}} = \frac{(3)(2)}{(6)(5)} = \frac{1}{5}.
\end{align*}
$$

If the socks were not matching on Monday, there are now two pairs of matching socks plus two mismatching socks. The total number of pairs is still $\binom{6}{2}$ but now only two such pairs match. Therefore,

$$
\begin{align*}
P[\text{match on Tues.}|\text{don't match on Mon.}] &= \frac{2}{\binom{6}{2}} = \frac{(2)(2)}{(6)(5)} = \frac{2}{15}.
\end{align*}
$$

Thus in conclusion we have

$$
\begin{align*}
P[\text{match on Tues.}] &= \frac{1}{5}\cdot\frac{1}{7} + \frac{2}{15}\cdot\frac{6}{7}.
\end{align*}
$$
# END SOLUTION

# END SUBPROB



# BEGIN SUBPROB

($\times$`<!-- -->`{=html}6) On Tuesday evening Robert does laundry so
that when he gets ready on Wednesday morning all of the socks are clean
again. As usual he selects another two socks at random, a selection
which is independent of any of his choices on Monday or Tuesday. What is
the probability that he wears at least one striped sock on Monday,
Tuesday, **and** Wednesday? *Show all your calculations.*

# BEGIN SOLUTION
Based on the setup, Robert must have worn exactly one striped sock on both Monday and Tuesday, and then wore either a single striped sock or a pair of striped socks on Wednesday. By the definition of conditional probability, we have

$$P(\text{1 striped on Mon.} \cap \text{1 striped on Tues.}) = P(\text{1 striped on Tues.} \mid \text{1 striped on Mon.}) \times P(\text{1 striped on Mon.})$$

For Monday, there are $\binom{2}{1}\binom{6}{1} = 12$ possible pairs of socks so that exactly one is striped. Thus the probability is given by

$$P(\text{1 striped Mon.}) = \frac{12}{\binom{8}{2}} = \frac{(12)(2)}{(8)(7)} = \frac{3}{7}.$$

Alternatively, you could write this as 1 minus the probability of getting either no striped socks or two striped socks. For the second part, by similar logic, we have

$$P(\text{1 striped on Tues.} \mid \text{1 striped on Mon.}) = \frac{\binom{1}{1}\binom{5}{1}}{\binom{6}{2}} = \frac{(5)(2)}{(6)(5)} = \frac{1}{3}.$$

Therefore we have

$$P(\text{1 striped on Mon.} \cap \text{1 striped on Tues.}) = \frac{3}{7} \cdot \frac{1}{3} = \frac{1}{7}.$$

For Wednesday, he can select either one or two striped socks. Earlier we counted 12 pairs which contain exactly one striped sock, so there are 13 which contain either one or two. Thus

$$P(\text{1 or 2 striped on Weds.}) = \frac{13}{\binom{8}{2}} = \frac{13}{28}.$$

By the independence assumption, we have

$$\begin{align}
&P(\text{1 striped on Mon.} \cap \text{1 striped on Tues.} \cap \geq\text{1 striped Weds.}) \\
&= P(\text{1 striped on Mon.} \cap \text{1 striped on Tues.}) \times P(\geq\text{1 striped Weds.}) \\
&= \frac{13}{(7)(28)}
\end{align}$$
# END SOLUTION

# END SUBPROB



# END PROB