# BEGIN PROB

The Avocado Cup is organized into rounds. In each round,
players who win advance to the next round, and players who lose are
eliminated. Rounds continue on like this until there is a single
tournament winner.

Define the following events in the sample space of possible outcomes of
the Avocado Cup:

-   $A =$ Avi loses in the first round.

-   $B =$ Avi wins the tournament.

-   $C =$ Avi wins in the first round.

# BEGIN SUBPROB

Which of the following statements is true? **Select all that
apply.**

[ ] $A$ and $B$ are independent.
[ ] $A$ and $B$ are conditionally independent given $C$.
[ ] $A$, $B$, and $C$ form a partition of the sample space.
[ ] None of the above.

# BEGIN SOLUTION

$A$ and $B$ are conditionally independent given $C$.

TODO

# END SOLUTION

# END SUBPROB # BEGIN SUBPROB

The events $A$ and $B$ are mutually exclusive, or disjoint.
More generally, for **any** two disjoint events $A$ and $B$, show how to
express $P(\overline{A}|(A \cup B))$ in terms of $P(A)$ and $P(B)$
**only**. For this problem only, **show your work and justify each
step.**

# BEGIN SOLUTION

There are several correct approaches to this problem. The simplest
one comes from using the definition of conditional probability to write
$$\begin{aligned}
            P(\overline{A}|(A \cup B)) &= \dfrac{P(\overline{A}\cap (A \cup B))}{P(A \cup B)}.\\
            \intertext {To evaluate the numerator, notice that since $A$ and $B$ are disjoint, any outcome that is not in $A$ but is in the union of $A$ and $B$ ($A$ or $B$) must be in $B$. The Venn diagram shown below illustrates this. Therefore, we can simplify this as}
            &= \dfrac{P(B)}{P(A \cup B)} \\
            \intertext{ and because we know $A$ and $B$ are disjoint, we can use the addition rule to expand the denominator as}
            &= \dfrac{P(B)}{P(A)+P(B)}. \\
            
\end{aligned}$$ This is the desired final expression because it uses
$P(A)$ and $P(B)$ only.

In the Venn Diagram below, $\overline{A}$ is shaded in yellow, and
$A \cup B$ is shaded in blue. Their overlap,
$\overline{A}\cap (A \cup B))$, is shaded in green, which is just $B$.

<center><img src="../assets/images/sp23-midterm2/venn.jpg" width="600" height="330"></center>

# END SOLUTION

# END SUBPROB

# END PROB