# BEGIN PROB

Suppose that there are three possible experience levels
in chess (beginner, intermediate, advanced). Only **10%** of beginner
players beat Avi at a game of chess, while **50%** of intermediate
players and **80%** of advanced players do.

Avi signs up to participate in a certain chess tournament called the
Avocado Cup. Aside from Avi, **50%** of the players in the tournament
are beginners, **40%** are intermediate, and **10%** are advanced.

The tournament proceeds in rounds. In the first round of the tournament,
players are **randomly paired up** for a game of chess.

# BEGIN SUBPROB

What is the probability that Avi wins in the first round of
the tournament?

( ) $33 \%$
( ) $50 \%$
( ) $67 \%$
( ) $83 \%$
( ) None of the above.

# BEGIN SOLUTION

$67 \%$

We know the percentages of players that beat Avi (meaning Avi loses) and the percentages of different types of players inside the Avocado Cup.

We can use the percentage of players that beat Avi to figure out the percentage of times Avi wins by doing $1 - p$!

Avi wins against beginners $1 - 0.1 = 0.9\%$ of the time, against intermediate players $1 - 0.4 = 0.6\%$ of the time, and against advanced players $1 - 0.8 = 0.2 \%$ of the time.

Now we can multiply the percentage of time Avi wins with the percentage of different players types to find the probability Avi will win in the first round! We can do this because you can imagine we are multiplying the probability Avi wins with the amount of people in the tournament of that level.

$$\begin{align*}
0.9 * 0.5 &= 0.45 \\
0.4 * 0.5 &= 0.2 \\
0.2 * 0.1 &= 0.02 \\
0.45 + 0.2 + 0.02 &= 0.67
\end{align*}$$

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

It turns out that, sadly, Avi loses to his opponent in the
first round. What is the probability that Avi's opponent is an advanced
player? Choose the **closest answer** among the choices listed.

( ) $15 \%$
( ) $25 \%$
( ) $35 \%$
( ) $45 \%$

# BEGIN SOLUTION

$25 \%$

- Let $\mathbb{P}(A)$ be the probability of Avi losing a match
- Let $\mathbb{P}(B)$ be the probability of Avi playing against an advanced player

We can use Bayes theorem to help us find the probability that Avi lost the match to an advanced player ($\mathbb{P}(A|B)$). Recall Bayes' theorem is:

$$
\mathbb{P}(A|B) = \frac{\mathbb{P}(B|A) \cdot \mathbb{P}(A)}{\mathbb{P}(B)}
$$

We are given $\mathbb{P}(A) = 0.1$ and $\mathbb{P}(B|A) = 0.8$.

We can calculate $\mathbb{P}(B)$ with the law of total probability:
$$
\mathbb{P}(B) = \mathbb{P}(B|A) \cdot \mathbb{P}(A) + \mathbb{P}(B|\text{not }A)\cdot \mathbb{P}(\text{not }A)
$$
Note that $\mathbb{P}(\text{not }A)$ means the probability of A not happening.

We are able to calculate $\mathbb{P}(B|\text{not }A)$ because we know the percentage of times Avi wins against advanced players: $1 - 0.8 = 0.2$. We are also able to calculate $\mathbb{P}(\text{not }A)$ because we know the probability of Avi winning a match is $67 \% = 0.67$.

Plugging in what we know into the law of total probability equation we get:
$$\begin{align*}
\mathbb{P}(B) &= 0.8 \cdot 0.1 + 0.2 \cdot 0.67 \\
&=0.08 + 0.134 \\
&= 0.214
\end{align*}$$

Back to Bayes theorem we have:
$$\begin{align*}
\mathbb{P}(A|B) &= \frac{0.8 \cdot 0.1}{0.214} \\
&= \frac{0.08}{0.214}\\
&= 0.35
\end{align*}$$

# END SOLUTION

# END SUBPROB

# END PROB