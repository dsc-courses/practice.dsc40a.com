# BEGIN PROB

\[(12 points)\] A sample space $S$ is partitioned by three disjoint
non-empty events $E_1 \cup E_2 \cup E_3=S$. Let $A \subset S$ be an
event and assume you are given the following probabilities:
$$P(E_1),\hspace{.1in}P(E_2),\hspace{.1in}P(A \vert E_2),\hspace{.1in}P(A \vert E_3),\hspace{.1in}\text{ and }P(A \cap E_1).$$
$\bar{A}$ denotes the complement of A.

# BEGIN SUBPROB

Show that the probability $P(E_1 \vert \bar{A})$ can be calculated using
the above terms (i.e., no probability terms are missing in order to make
this calculation).



# BEGIN SOLUTION
::: responsebox
True.
$$P(E_1 \vert \bar{A}) =  \frac{P(\bar{A} \cap E_1)}{P(\bar{A})}$$ For
the numerator $$P(\bar{A} \cap E_1) = P(\bar{A} \vert E_1)  * P( E_1)$$
which we can calculate as $$P(\bar{A} \vert E_1) = 1-P(A \vert E_1)$$
$$P(A \vert E_1) = \frac{P(A \cap E_1)}{P(E_1)}$$ Therefore
$P(\bar{A} \cap E_1)  = P(E_1)-P(A \cap E_1)$. For the denominator we
use the complement $$P(\bar{A}) = 1-P(A)$$

Using the law of total probability:
$$P(A) = P(A \vert E_1) P(E_1) +  P(A \vert E_2) P(E_2) + P(A \vert E_3) P(E_3)$$
which we can calculate using $$P(E_3)=1-P(E_2)-P(E_1)$$
:::
# END SOLUTION

# END SUBPROB

*For parts **(b)**, **(c)**, and **(d)**, you do not need to show your
work for full credit, but partial credit may be awarded for supporting
calculations and reasoning.*

# BEGIN SUBPROB

For the following statements, circle either **TRUE** or **FALSE** to
indicate whether the equation is correct.

**(i)** $P(\bar{E_1} \vert A) =  P(E_2 \vert A) + P(E_3 \vert A)$

  ----------------- ------------------
   $\bigcirc$ TRUE   $\bigcirc$ FALSE
  ----------------- ------------------



**(ii)** $P(\bar{A} \vert E_1) = 1 - P(\bar{E}_1 \vert \bar{A})$

  ----------------- ------------------
   $\bigcirc$ TRUE   $\bigcirc$ FALSE
  ----------------- ------------------



**(iii)** $P(\bar{E_1} \vert A) = 1 - P(\bar{E}_1 \vert \bar{A})$

  ----------------- ------------------
   $\bigcirc$ TRUE   $\bigcirc$ FALSE
  ----------------- ------------------



# BEGIN SOLUTION
::: responsebox
i. TRUE -
$P(\bar{E_1} \vert A) = 1 - P({E_1} \vert A) =  P(E_2 \vert A) + P(E_3 \vert A)$.
:::

::: responsebox
ii. FALSE:
$P(\bar{A} \vert E_1) = 1- P({A} \vert E_1) \neq 1 - P(\bar{E}_1 \vert \bar{A})$
:::

::: responsebox
iii. FALSE:
$P(\bar{E_1} \vert A) = 1 - P({E}_1 \vert {A}) \neq 1 - P(\bar{E}_1 \vert \bar{A})$
:::
# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

Which of the following statements concerning $E_1,E_2,E_3$ are true?
*Only one statement is true.*

  --------------------------------------------------------- -----------------------------------------------------------
  $\bigcirc$ $P(\overline{E_1} \cap \overline{E_2}) = 0$    $\bigcirc$ $P(\overline{E_1} \cup \overline{E_2}) \neq 0$
  $\bigcirc$ $E1$, $E_2$ and $E_3$ are independent events   $\bigcirc$ $P(E_1 \cup E_3) = 1$
  --------------------------------------------------------- -----------------------------------------------------------



# BEGIN SOLUTION
::: responsebox


Correct:
$\overline{E_1} \cup \overline{E_2} = (E_2 \cup E_3) \cup (E_1 \cup E_3) = S \rightarrow P(\overline{E_1} \cup \overline{E_2}) = 1$.

Incorrect:
$P(\overline{E_1} \cap \overline{E_2}) = P((E_2 \cup E3) \cap (E_1 \cup E_3)) = P(E_3) \neq 0$

Incorrect: $P(E_1 \cup E_3) = 1 - P(E_2) < 1$ since $E_2$ is non empty.

Incorrect $E1$, $E_2$ and $E_3$ are not independent since
$P(E_1,E_2,E_3) = P(E_1 \cap E_2 \cap E_3) = P(\emptyset)= 0 \neq P(E_1)P(E_2)P(E_3)>0$
:::
# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

If the event $E_1$ is fully contained within event $A$, i.e., every
outcome in $E_1$ is also an outcome in $A$, we write that
$E_1 \subseteq A$. Which if the following statements is true? *Only one
statement is true.*

  -----------------------------------------------------------------------------
  $\bigcirc$ If $E_1 \subseteq A$, then $P(E_1)\leq P(A)$.
  $\bigcirc$ If $P(E_1)\leq P(A)$, then $E_1 \subseteq A$.
  $\bigcirc$ If $E_1 \subseteq A$, then $P(E_1 \cap A)\leq P(E_2)$.
  $\bigcirc$ If $E_1 \subseteq A$, then $E_1$ and $A$ are independent events.
  $\bigcirc$ If $E_1 \subseteq A$, then $E_3$ and $A$ are independent events.
  -----------------------------------------------------------------------------



# BEGIN SOLUTION
::: responsebox


Correct: $P(E_1) = \sum_{s \in E_1} p(s)$ and
$P(A) = \sum_{s \in A} p(s)$. Since $\forall s \in E_1: s \in A$, then
$P(E_1)\leq P(A)$.

The converse is not true: $P(E_1)\leq P(A)$ can be true without
$E_1 \subseteq A$.

When $E_1 \subseteq A$ then $P(E_1)=P(E_1 \cap A)$ however we don't know
anything about the relationship between $P(E_1)$ and $P(E_2)$.

If $E_1 \subseteq A$ these are not independent events since
$P(E_1 | A) = 1 \neq P(E_1)$.
:::
# END SOLUTION

# END SUBPROB

# END PROB