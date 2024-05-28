# BEGIN PROB

**Probability and Counting**

# BEGIN SUBPROB

\[4 points\] There is one box of bolts that contains some long and some
short bolts. A manager is unable to open the box at present, so she asks
her employees what is the composition of the box. One employee says that
it contains 60 long bolts and 40 short bolts. Another says that it
contains 10 long bolts and 20 short bolts. Unable to reconcile these
opinions, the manager decides that each of the employees is correct with
probability 1/2. Let $B_1$ be the event that the box contains 60 long
and 40 short bolts, and let $B_2$ be the event that the box contains 10
long and 20 short bolts. What is the probability that the first bolt
selected is long?

::: responsebox
3.3in $$P(B_1)=P(B_2)=0.5.$$ $$P(long|B_1) = 0.6$$ $$P(long|B_2) = 1/3$$

$$P(long)=P(long|B_1)*P(B_1)+P(long|B_2)*P(B_2)
= 0.5*0.6+0.5*1/3=7/15$$
:::

# BEGIN SOLUTION

# END SOLUTION

# END SUBPROB # BEGIN SUBPROB

\[3 points\] How many ways can one arrange the letters A,B,C,D,E such
that A,B,C are together (in any order)?

::: responsebox
4in 3\*2\*1 for the different ways to arrange D, E and the sub-sequence
of A,B,C 3\*2\*1 for arranging A,B,C within the subsequence

Overall 3!\*3!

This is similar to homework 6 problem 3.
:::

# BEGIN SOLUTION

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

\[4 points\] Two chess players A and B play a series of chess matches
against each other until one of them wins 3 matches. Every match ends
when one of the players wins against the other that is the game does not
end in draw/tie. For example, the series ends when the outcomes of the
1st 4 games are: A wins, A wins, B wins, A wins. In how many ways can
the series be won?

::: responsebox
4in Series ends when the last game in the series is the third win by
either player. Overall there can at least 3 games and at most up to 5
games (including) before either player wins 3 games.Let's assume player
A wins, and multiply the options by 2 to count for player B winning.
Therefore

-   For 3 games - there is a single option.

-   For 4 games, the last game is player A win, therefore the 3
    preceding have C(3,2) options for player A winning 2 of the games.

-   For 5 games, the last game is player A win, therefore the 4
    preceding have C(4,2) options for player A winning 2 of the games.

Overall 2\*(1+C(3,2)+C(4,2))
:::

# BEGIN SOLUTION

# END SOLUTION

# END SUBPROB

# END PROB