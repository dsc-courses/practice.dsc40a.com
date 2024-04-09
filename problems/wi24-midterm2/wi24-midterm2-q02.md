# BEGIN PROB

\[(12 points)\] A special poker card deck contains the 52 standard card:

::: center
  -------------------------------------------------
  Heart: 2, 3, 4, 5, 6, 7, 8, 9, 10, J, Q, K, A
  Diamond: 2, 3, 4, 5, 6, 7, 8, 9, 10, J, Q, K, A
  Club: 2, 3, 4, 5, 6, 7, 8, 9, 10, J, Q, K, A
  Spade: 2, 3, 4, 5, 6, 7, 8, 9, 10, J, Q, K, A
  -------------------------------------------------

\
:::

Plus two wildcard: Red Joker and Black Joker. The total numbers of card
in this card deck is 54. # BEGIN SUBPROB

(2 points) How many ways to select a 4 card hand from this card deck?
(Note: order does not matter in a card hand.)

::: center
:::

# BEGIN SOLUTION

CAN NEVER BE EMOTY

# END SOLUTION

# END SUBPROB 

# BEGIN SUBPROB

(4 points) For this deck, how many 5 card hands are there that include a
four-of-a-kind (four cards of the same value)? Show your work.

::: mdframed
**Proof:**
:::

# BEGIN SOLUTION

Since the first 4 cards are four-of-a-kind (same number), there are 13
ways to select four-of-a-kind. For the 5th card, there are 50 total
choices (12 values $\times$ 4 suits $\times$ + 2 wildcards). So there
are total 13\*50=650 options.

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

(6 points) In certain poker rules, a bomb is defined as either
four-of-a-kind, or two wildcards (red joker and black joker). Suppose
you randomly draw 4 card hand and you found a bomb in it, what is the
probability that the bomb is four-of-a-kind? Show your work.

::: mdframed
**Proof:**
:::

# BEGIN SOLUTION

The number of sequences that containing two jokers (the other two cards
are arbitrary) is given by: $$\begin{aligned}
\underbrace{C(4,2)}_{\mbox{Joker Locations}} \times P(2,2) \times C(52, 2) \times P(2,2) = 4 \times 3 \times 52 \times 51
\end{aligned}$$ The number of sequences that form four of a kind is
$$\begin{aligned}
C(13,1) P(4,4) = 13 \times 4 \times 3 \times 2
\end{aligned}$$ The two events are exclusive. And for a bomb to occur,
the four cards either contains two jokers or form four of a kind. Hence,
$$\begin{aligned}
    P(\mbox{Four of a kind} | \mbox{Bomb}) = \frac{13 \times 4 \times 3 \times 2}{13 \times 4 \times 3 \times 2 + 4 \times 3 \times 52 \times 51 } = \frac{1}{103}
\end{aligned}$$

# END SOLUTION

# END SUBPROB

# END PROB