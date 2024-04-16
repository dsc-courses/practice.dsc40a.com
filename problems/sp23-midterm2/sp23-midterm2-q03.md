# BEGIN PROB

A set of chess pieces has $32$ pieces. $16$ of these are black and $16$ of these are white. **In each color**, the $16$ pieces are:

- $8$ pawns,
- $2$ bishops,
- $2$ knights,
- $2$ rooks,
- $1$ queen, and 
- $1$ king.

When there are multiple pieces of a given color and type (for example, $8$ white pawns), we will assume they are **indistinguishable** from one another.

In this problem, a **lineup** is a way of arranging items in a straight line.

# BEGIN SUBPROB

A chess player lines up all $16$ **white pieces** from the set of chess pieces. How many different-looking lineups can be created?
Remember, some pieces look the same.

# BEGIN SOLUTION

$\dfrac{16!}{8!2!2!2!} = \dfrac{P(16,8)}{2^3} = C(16, 8)*C(8, 2)*C(6, 2)*C(4, 2)*C(2, 1)*C(1, 1)$

As you can see above there are a few ways to write the answer. You could use permutations or combinatorics.
<br> 

Here is the explanation using combinatorics:

We know from the problem we are only looking at the $16$ white pieces. This means we know we are doing $16$ choose something. From here we can look at the different possible types of chess pieces (pawns, bishops, knights, rooks, queen, and king). This means we can write $C(16, 8)$ because from $16$ pieces we are choosing $8$ pawns. Then we can multiply it by $C(8, 2)$ because $16 - 8 = 8$ pieces left and there are $2$ bishops. Following this same logic we get $C(8 - 2 = 6, 2)$ for knights, $C(6-2 = 4, 2)$ for rooks, $C(4 - 2, 1)$ for the queen, and $C(2 - 1 = 1, 1)$ for the king.

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

A chess player lines up all 16 **pawns** from the set of
chess pieces. How many lineups have white pawns on both ends?

# BEGIN SOLUTION

$C(14, 6) = C(14, 8) = \dfrac{14!}{8!6!}$

TODO

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

A chess player lines up all 16 **pawns** from the set of
chess pieces. Assuming that each different-looking lineup is equally
likely, what is the probability that the lineup has two of the
same-colored pawns on both ends (both black or both white)?

( ) $\frac{1}{4}$
( ) $\frac{1}{2}$
( ) $\frac{7}{30}$
( ) $\frac{7}{15}$
( ) None of the above.

# BEGIN SOLUTION

$\frac{7}{15}$

TODO

# END SOLUTION

# END SUBPROB

# END PROB