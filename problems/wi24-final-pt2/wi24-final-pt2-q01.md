# BEGIN PROB

<i>Source: [Winter 2024 Final Part 2](../wi24-final-pt2/index.html), Problem 1</i>

Consider an experiment where each of $n$ people selects
one piece from their own set of 32 chess pieces, uniformly at random.
The **result** of the experiment is a description of the **colors and
types** of the pieces each person selected. For example, if $n=3$, one
possible result is:

-   Person 1 selected a white knight.

-   Person 2 selected a black queen.

-   Person 3 selected a black pawn.

# BEGIN SUBPROB

How many results are possible for this experiment with $n$
people?

( ) $2^n$
( ) $6^n$
( ) $12^n$
( ) $16^n$
( ) $32^n$
( ) None of the above.

# BEGIN SOLUTION

$12^n$

To answer this question we must determine how many **different** pieces each person can choose. In a complete chess set we know that there's pawns, knights, bishops, rooks, queens, and kings. Then we also know that each of these pieces can be aither black or white, therefore there's a totoal of $6 \cdot 2 = 12$ different pieces. Notice that a complete chess set has 32 total pieces, but there's multiple duplicates in those 32 pieces that is why we say there's only 12 different pieces on a chess set.

Now since every person has their own chess set, we know that each of them can get any of the 12 pieces, therefore if we do this with one person there would be $12$ possible outcomes, now if we do it with two persons the first person can get any of the 12 pieces, but then for each piece that person 1 can choose person 2 can choose from their 12 pieces, which means that in this case there's $12 \cdot 12$ outcomes. if we keep doing this for n persons we'll get that there's $12 \cdot \dots \cdot 12 = 12^n$.   

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

As $n$ becomes large, what fraction of n people has selected a black pawn? Choose the answer that's closest to the actual fraction.

( ) 1/32
( ) 1/12
( ) 1/4
( ) 1/2
( ) None of the above.

# BEGIN SOLUTION

1/4 

First lets calculate the probability of one person choosing a black pawn. Well, we know that the complete chess set has 32 pieces and from those 32 there's 8 black pawns, that gives us a probability of $\frac{8}{32} = \frac{1}{4}$. Now think about how we interpret probabilities, for example if I say that the probability of getting heads when flipping a coin is $\frac{1}{2}$ that just means that if I flip a coin undefinetely, I expect to see heads $\frac{1}{2}$ of the time. Similarly when we say that the probability of choosing a black pawn is $\frac{1}{4}$, that means that if we were to do the experiment undefinetely, we expect to choose a black pawn $\frac{1}{4}$ of the time, but it does not matter if you are doing it undefinetly or if you have an infinete amount of people doing it once the experiemnt remains the same, therefore you still expect to see the black pawn $\frac{1}{4}$ of the time.

# END SOLUTION

# END SUBPROB # BEGIN SUBPROB

True or False: Having two pawns is **independent** of having two white pieces.

( ) True
( ) False

# BEGIN SOLUTION

True

There are multiple ways to check the independence between two events, in this case I will use the fact that two events (A and B) are indepedent whenever $P(A|B) = P(A)$.

No lets define  A as the event where you choose two pawns, and B as the event of choosing two white pieces. Then if we have a white piece the probability of that white piece being also a pawn would be $\frac{8}{16}$ because there's 8 white pawns and 16 white pieces total, thus if we know that we have another white piece the probability for that piece to be also a pawn is $\frac{8}{16}$ again, Therefore $P(A|B) = (\frac{8}{16})^2 = \frac{1}{4} $. Now the probability of having a pawn is $\frac{16}{32}$ because there's 16 pawns and 32 total pieces, therefore the probability of doing that twice would be $(\frac{16}{32})^2 = \frac{1}{4}$. So we conclude that

\begin{align*}
P(A|B) = \frac{1}{4} = P(A)
\end{align*}

which means A and B are independent.

# END SOLUTION

# END SUBPROB

# END PROB