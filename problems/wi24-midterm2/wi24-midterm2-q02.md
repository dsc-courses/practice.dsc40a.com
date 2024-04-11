# BEGIN PROB

<i>Originally Problem 2 on the Second Winter 2024 Midterm.</i>

A special poker card deck contains the 52 standard cards:


  -------------------------------------------------
  Heart: 2, 3, 4, 5, 6, 7, 8, 9, 10, J, Q, K, A
  Diamond: 2, 3, 4, 5, 6, 7, 8, 9, 10, J, Q, K, A
  Club: 2, 3, 4, 5, 6, 7, 8, 9, 10, J, Q, K, A
  Spade: 2, 3, 4, 5, 6, 7, 8, 9, 10, J, Q, K, A
  -------------------------------------------------

<br>

...plus two wildcards: Red Joker and Black Joker. 
The total number of cards in this card deck is 54. 

# BEGIN SUBPROB

How many different four-card hands can be selected from this deck?
(Note: order does not matter in a card hand.)

# BEGIN SOLUTION

$C(54, 4) = 316251$ _Note: this means "54 Choose 4"_

Since order does not matter, we would use a combination instead of a permutation here. From 54 unique cards in our poker deck, we can _choose_ 4 at random to get a card hand.

An alternative way to think about it: there are 54 options for the first card we pick, 53 for the second card, 52 for the third card, etc. For four cards, we have $54 \times 53 \times 52 \times 51$ hands. However this will count the same hand in different card orders as different hands, which we don't want. To correct this, we divide by $4!$ ($4 \times 3 \times 2 \times 1$), because each unique hand will appear 24 times but in different orders.

$$\frac{54 \times 53 \times 52 \times 51}{4 \times 3 \times 2 \times 1} = C(54, 4) = 316251.$$

# END SOLUTION

# END SUBPROB 

# BEGIN SUBPROB

For this deck, how many 5 card hands are there that include four-of-a-kind (four cards of the same _value_)? Show your work.

# BEGIN SOLUTION

Since the first 4 cards are four-of-a-kind (same number), there are 13
ways to select a four-of-a-kind. For the 5th card, there are 50 total
choices (12 remaining values $\times$ 4 suits + 2 wildcards). So there are a total $13 \times 50 = 650$ options.

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

In certain poker rules, a bomb is defined as either
four-of-a-kind, or two wildcards (red joker and black joker). Suppose
you randomly draw a 4 card hand and you found a bomb in it, what is the
probability that the bomb is four-of-a-kind? Show your work.

# BEGIN SOLUTION

<!-- Need to edit this one -->

The number of hands containing two jokers (the other two cards are arbitrary) is given by:
$$\begin{aligned}
\underbrace{C(2,2)}_{\text{Two Jokers}} \times \underbrace{C(52, 2)}_{\text{Other Two Cards}} = \frac{52 \times 51}{2} = 1326.
\end{aligned}$$ The number of hands that form four of a kind is 13, one for each of the 13 unique values in a deck.

<br>

For a bomb to occur,
the four cards either contain two jokers or form four of a kind. Hence,
$$\begin{aligned}
    P(\text{Four of a kind | Bomb}) = \frac{13}{13 + 1326} = \frac{1}{103}
\end{aligned}$$

<!-- OLD SOLUTION -->

<!-- 
The number of sequences that containing two jokers (the other two cards are arbitrary) is given by:
$$\begin{aligned}
\underbrace{C(4,2)}_{\text{Joker Locations}} \times P(2,2) \times C(52, 2) \times P(2,2) = 4 \times 3 \times 52 \times 51
\end{aligned}$$ The number of sequences that form four of a kind is
$$\begin{aligned}
C(13,1) P(4,4) = 13 \times 4 \times 3 \times 2
\end{aligned}$$ The two events are exclusive. And for a bomb to occur,
the four cards either contains two jokers or form four of a kind. Hence,
$$\begin{aligned}
    P(\text{Four of a kind | Bomb}) = \frac{13 \times 4 \times 3 \times 2}{13 \times 4 \times 3 \times 2 + 4 \times 3 \times 52 \times 51 } = \frac{1}{103}
\end{aligned}$$ -->

# END SOLUTION

# END SUBPROB

# END PROB