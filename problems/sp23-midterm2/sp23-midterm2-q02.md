# BEGIN PROB

A set of chess pieces has 32 pieces. 16 of these are black and 16 of these are white. **In each color**, the 16 pieces are:

- 8 pawns,
- 2 bishops,
- 2 knights,
- 2 rooks,
- 1 queen, and 
- 1 king.

When there are multiple pieces of a given color and type (for example, 8 white pawns), we will assume they are **indistinguishable** from one another.

Suppose you randomly select $2$ pieces from a set of $32$ chess pieces, **without replacement**.

# BEGIN SUBPROB

You glance at the pieces just long enough to see that both pieces are white. What is the probability that you have $2$ pawns?

# BEGIN SOLUTION

$$
\dfrac{8}{16}*\dfrac{7}{15} = \dfrac{7}{30}
$$

We get $\dfrac{8}{16}$ from the fact there are $8$ white pawns and $16$ white chess pieces. So the chance of first getting a pawn is $\dfrac{8}{16}$.

Now we assume that we have a white pawn, meaning there are $8-1=7$ white pawns left and $16 - 1 = 15$ white chess pieces, which means we have a $\dfrac{7}{15}$ chance for getting another white pawn.

From here we simplify the answer by doing:

$$
\dfrac{8 * 7}{16 * 15} = \dfrac{56}{240} = \dfrac{7}{30}
$$

<br>

Another way to solve this is using combinatorics: Note that $C(8, 2)$ means "$8$ choose $2$."

$\dfrac{C(8, 2)}{C(16, 2)} = \dfrac{\frac{8}{32}*\frac{7}{31}}{\frac{16}{32}*\frac{15}{31}} = \dfrac{7}{30}$

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

True or False: Having two pawns is **independent** of having two white pieces.

( ) True
( ) False

# BEGIN SOLUTION

False.

We know that two probabilities are independent of each other if $\mathbb{P}(A \cap B) = \mathbb{P}(A) \cdot \mathbb{P}(B)$.

- Let $\mathbb{P}(A)$ be the probability of getting a white piece twice in a row.
- Let $\mathbb{P}(B)$ be the probability of getting a pawn twice in a row.

We can calculate the probability of getting a white piece twice in a row $\mathbb{P}(A) = \frac{16}{32} \cdot \frac{15}{31} = \frac{15}{62}$. We get $\frac{16}{32}$ from the fact there are $16$ white pieces out of the $32$ total pieces. We get $\frac{15}{31}$ from the fact there are now $15$ white pieces out of the $31$ pieces left after taking out a white piece.

We can also calculate the probability of getting a pawn twice in a row. Note that the color of the pawn does not matter! $\mathbb{P}(B) = \frac{16}{32} \cdot \frac{15}{31} = \frac{15}{62}$. We get $\frac{16}{32}$ from the fact there are $16$ pawns ($8$ black pawns plus $8$ white pawns) out of the $32$ total pieces. We get $\frac{15}{31}$ from the fact there are now $15$ pawns out of the $31$ pieces left after taking out a pawn.

We can now calculate $\mathbb{P}(A) \cdot \mathbb{P}(B)$:
$$
\frac{15}{62} \cdot \frac{15}{62} = \frac{225}{3844}
$$

Recall we calculate $\mathbb{P}(A \cap B) = \mathbb{P}(A) \cdot \mathbb{P}(B|A)$.

We solved for $\mathbb{P}(B|A)$ in part A of the problem: $\frac{7}{30}$. We also already solved for $\mathbb{P}(A)$ above: $\frac{15}{62}$.

$$
\frac{15}{62} \cdot \frac{7}{30} = \frac{7}{124}
$$

We can see that $\mathbb{P}(A \cap B) \neq \mathbb{P}(A) \cdot \mathbb{P}(B)$ because $\frac{7}{124} \neq \frac{225}{3844}$, so the answer is False.

# END SOLUTION

# END SUBPROB

# END PROB