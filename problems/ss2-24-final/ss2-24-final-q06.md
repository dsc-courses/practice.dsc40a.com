# BEGIN PROB

<i>Source: [Summer Session 2 2024 Final](../ss2-24-final/index.html), Problem 6a-d</i>

Euchre is a card game popular in the Midwest United States
and is played with a partial deck of 24 cards: the 9, 10, Jack, Queen,
King, and Ace of all four suits (Hearts, Diamonds, Spades, Clubs). A
hand of cards in Euchre is 5 cards.

Assume cards are dealt by drawing at random **without replacement** from
the set of 24 possible cards. The order of cards in a hand does not
matter.

In this question, you may leave your answers unsimplified, in terms of
fractions, exponents, factorials, the permutation formula $P(n, k)$, and
the binomial coefficient ${n \choose k}$.

# BEGIN SUBPROB

How many possible hands of 5 cards are there in total?

# BEGIN SOLUTION

$\binom{24}{5}$

We are sampling without replacement, and the order in which we select the cards does not matter. The formula to count this is given by the choose formula ${n \choose k} = \frac{n!}{k!(n-k)!}$, where $n=24$ is the total number of objects we can choose from, and $k=5$ is the size of the set of objects we're sampling. Therefore, the total possible hands is $\binom{24}{5}$.

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

What is the probability that all five cards in a hand of Euchre are from
the same suit?

# BEGIN SOLUTION

$\frac{\binom{6}{5}\binom{4}{1}}{\binom{24}{5}}$

First, we want to count the number of five card hands of the same suit. There are 4 suits, so there are $\binom{4}{1}$ ways to choose a suit. We want to multiply this choice by the possible ways to choose a set of 5 distinct card "faces". Since there are 6 card faces (the 9, 10, Jack, Queen, King, and Ace), we count this with $\binom{6}{5}$. From the previous part, we found the total 5 card hands is $\binom{24}{5}$. So the probability that we want is $\frac{\binom{6}{5}\binom{4}{1}}{\binom{24}{5}}$.

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

What is the probability that exactly two cards in a hand of Euchre are
from the same suit?

# BEGIN SOLUTION

$\frac{\binom{4}{1} \cdot \binom{6}{2} \cdot \binom{3}{3} \cdot \binom{6}{1}^3}{\binom{24}{5}}$

First, we want to count the number of hands where exactly 2 cards are from the same suit. This means that 2 of the 5 cards are any of the 4 suits, and the remaining 3 cards are each a different suit. We begin by counting the ways to choose 1 suit that 2 of the cards will share: $\binom{4}{1}$. Then, we must multiply the ways to choose 2 card faces out of the 6 possibilities, which is $\binom{6}{2}$. The remaining 3 cards in our hand must each be a distinct suit out of the 3 remaining suits; there is exactly $\binom{3}{3} = 1$ way to choose these suits. Each of the remaining cards can be 1 of 6 card faces, so we choose these 3 cards with $\binom{6}{1}^3$. The number of hands we want to count is $\binom{4}{1} \cdot \binom{6}{2} \cdot \binom{3}{3} \cdot \binom{6}{1}^3$.

Similar to the previous problem, we divide by the total number of hands to obtain the probability: 
$$\frac{\binom{4}{1} \cdot \binom{6}{2} \cdot \binom{3}{3} \cdot \binom{6}{1}^3}{\binom{24}{5}}$$

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

Euchre is played by four players, so when all cards are dealt, there are
four remaining cards $(24 - 4\cdot 5)$. What is the probability that all
four remaining cards are Jacks (the strongest card in Euchre)?


# BEGIN SOLUTION

$\frac{4}{24} \cdot \frac{3}{23} \cdot \frac{2}{22} \cdot \frac{1}{21}$

TODO

# END SOLUTION

# END SUBPROB

# END PROB