# BEGIN PROB

<i>Source: [Spring 2023 Midterm 2](../sp23-midterm2/index.html), Problem 3</i>

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


$$C(16, 8) \cdot C(8, 2) \cdot C(6, 2) \cdot C(4, 2) \cdot C(2, 1) \cdot C(1, 1) = \dfrac{16!}{8!2!2!2!}$$


Think about the problem this way. You have 16 spots on the line and for each subgroup of pieces (pawns, bishops, rooks, etc.), you need to assign spots from the line to place the pieces on that group. For example, we have 16 spots available in the line, and we want to place the pawns first. Well, since we have 8 pawns and 16 unique spots on the line, there are exactly $C(16,8)$ ways to place the pawns differently. Now, once you place the pawns you'll have only 8 remaining spots on the line, so if you wish to place the 2 bishops now, there are C(8,2)  ways to do it. This means that there are $C(16,8) \cdot C(8,2)$ ways of arranging 8 pawns and 2 bishops. Repeat the process for all subgroups and you'll get:
<br>

$C(16, 8) \cdot C(8, 2) \cdot C(6, 2) \cdot C(4, 2) \cdot C(2, 1) \cdot C(1, 1) = \dfrac{16!}{8!2!2!2!}$


# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

A chess player lines up all 16 **pawns** from the set of chess pieces. How many lineups have white pawns on both ends?

# BEGIN SOLUTION

$$C(14, 6) = C(14, 8) = \dfrac{14!}{8!6!}$$

Similarly to 3.1, you know the placement of two pawns, thus you have 14 spots remaining. Then, you only want to place the remaining white pawns, once you do that, the remaining spaces are for the black pawns. therefore the answer is $C(14,6)=C(14,8)$ 

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


$$\frac{7}{15}$$

For this question you can use your answer for 3.2. We found that there's $C(14, 6) = C(14, 8) = \dfrac{14!}{8!6!}$ lines of pawns with only whitepawns in the ends, by the same reasoning there would be another $C(14, 8) = \dfrac{14!}{8!6!}$ lines with black pawns at the ends. Then there is $2C(14, 8)$ lines with same color pawns at the end, since we know ther are $C(16, 8)$ lines in total then we can calculates the answer by $\frac{2C(14, 8)}{C(16, 8)}$=$\frac{7}{15}$

Alternatively, As soon as you know the color of the first pawn, you know that there are 15 remaining pawns, from which only 7 are the same color, since each pawn is equally likely to get placed in the last spot you get a probability of  $\frac{7}{15}$


# END SOLUTION

# END SUBPROB

# END PROB