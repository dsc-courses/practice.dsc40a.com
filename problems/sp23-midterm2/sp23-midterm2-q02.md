# BEGIN PROB

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

True.

We know that two probabilities are independent of each other if ... TODO

# END SOLUTION

# END SUBPROB

# END PROB