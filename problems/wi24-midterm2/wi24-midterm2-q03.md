# BEGIN PROB

Schrödinger's cat is a famous thought experiment in
quantum mechanics proposed by physicist Erwin Schrödinger in 1935. The
experiment is described below:

"Imagine there's a hypothetical cat in a closed box with a toxic
radioactive element that might decay. If it decays, the cat dies; if
it doesn't, the cat lives."

Please note that Schrödinger's Cat is a purely theoretical concept---a
thought experiment. It has never been executed in the real world, and no
cats have ever been harmed as a result of it.

# BEGIN SUBPROB

(6 points) Suppose the cat has 90% of the chance to die if the decay
happens. The cat also has 10% chance to die even if the decay does not
happen. Suppose the decay happens with a 20% probability. After you open
the box, you find the cat dead. What is the probability that the decay
happened?

::: mdframed
**Proof:**
:::

# BEGIN SOLUTION

The probability we are looking for is $P(Decay|Dead)$. Using Baye's
equation, we can write: $$\begin{aligned}
P(Decay|Dead) = \frac{P(Dead|Decay)P(Decay)}{P(Dead)}
\end{aligned}$$ Using the Law of Total Probability, we can rewrite the
denominator: $$\begin{aligned}
P(Decay|Dead) = \frac{P(Dead|Decay)P(Decay)}{P(Dead|Decay)P(Decay) + P(Dead|Not Decay)P(Not Decay)}
\end{aligned}$$ We know that: $$\begin{aligned}
    P(Dead|Decay) &= 90\% = 0.9\\
    P(Dead|Not Decay) &= 10\% = 0.1\\
    P(Decay) &= 20\% = 0.2
\end{aligned}$$ Plugging these numbers, we have: $$\begin{aligned}
P(Decay|Dead) &= \frac{0.9\times 0.2}{0.9 \times 0.2 + 0.1 \times (1-0.2)}\\
=\frac{18}{26}
\end{aligned}$$

# END SOLUTION

# END SUBPROB 
Quantum superposition is a mind-bending and
counter-intuitive concept in physics. In Schrödinger's cat scenario,
when the box is closed, the cat can be **both dead and alive**
simultaneously. However, once we open the box and observe, the
superposition collapses, and the cat must be either dead or alive, not
both. 

# BEGIN SUBPROB

(4 points) The Venn Diagram below depicts Schrödinger's cat scenario
with the box closed. In this diagram, the black dotted line is the event
of cat dead, the red dashed line denotes the event of cat being alive,
and the shaded region is the event of decay.

<center><img src="../assets/images/wi24-midterm2/venn_diag.png" width="630" height="330"></center>


Based on this Venn diagram, which of the following is true? Select all
that applies:

[ ] Decay is independent of Cat Dead
[ ] Decay is independent of Cat Alive
ensp;
[ ] Cat Dead and Cat Alive are mutually exclusive.
[ ] Cat Dead, Cat Alive, and Decay form a partition of the sample
space.
[ ] None of Above.

# BEGIN SOLUTION

NO EMPTY SOLNS 

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

(6 points) Given the following probabilities:

-   P(Cat Dead $\cup$ Decay) = $\frac{4}{5}$

-   P(Cat Alive $\cup$ Decay) = $\frac{1}{2}$

-   P(Cat Alive $\cup$ Cat Dead) = 1

-   P(Decay) = $\frac{1}{5}$

Using the Venn diagram in part b), calculate the probability for
Schrodinger's cat to be in superposition state (i.e. both dead and
alive):

::: mdframed
**Proof:**
:::

# BEGIN SOLUTION

Since we know that the decay is independent to cat's state, we have
$$\begin{aligned}
    P(Dead \cup Decay) &= P(Dead) + P(Decay) - P(Dead \cap Decay)\\
    &=P(Dead) + P(Decay) - P(Dead)\cdot P(Decay) = \frac{4}{5}
\end{aligned}$$ Similarly, we have: $$\begin{aligned}
    P(Alive \cup Decay) &= P(Alive) + P(Decay) - P(Alive \cap Decay)\\
    &=P(Alive) + P(Decay) - P(Alive)\cdot P(Decay) = \frac{1}{2}
\end{aligned}$$ Plugging in P(Decay) = $\frac{1}{5}$, we have:
$$\begin{aligned}
&P(Dead) + \frac{1}{5} - \frac{1}{5} P(Dead) = \frac{4}{5}\\
&P(Alive) + \frac{1}{5} - \frac{1}{5} P(Alive) = \frac{1}{2}\\
\end{aligned}$$ Solving these two equations, we have: $$\begin{aligned}
&P(Dead) = \frac{3}{4}\\
&P(Alive) = \frac{3}{8}\\
\end{aligned}$$ The probability of superposition state is P(Alive $\cap$ Dead). Since we know that P(Alive $\cup$ Dead) = 1 we have:
$$\begin{aligned}
P(Alive \cup Dead) &= P(Alive) + P(Dead) - P(Alive \cap Dead)\\
\end{aligned}$$ Rearranging terms, we have: $$\begin{aligned}
P(Alive \cap Dead) &= P(Alive) + P(Dead) - P(Alive \cup Dead)\\
&= \frac{3}{4} + \frac{3}{8} - 1\\
&= \frac{6}{8} + \frac{3}{8} - 1\\
&=\frac{1}{8}
\end{aligned}$$

# END SOLUTION

# END SUBPROB

# END PROB