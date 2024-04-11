# BEGIN PROB

<i>Originally Problem 3 on the Second Winter 2024 Midterm.</i>

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

Suppose the cat has 90% of the chance to die if the decay
happens. The cat also has 10% chance to die even if the decay does not
happen. Suppose the decay happens with a 20% probability. After you open
the box, you find the cat dead. What is the probability that the decay
happened?

# BEGIN SOLUTION

The probability we are looking for is $P(\text{Decay|Dead})$. Using Baye's
equation, we can write: $$\begin{aligned}
P(\text{Decay|Dead}) = \frac{P(\text{Dead|Decay})P(\text{Decay})}{P(\text{Dead})}
\end{aligned}$$ Using the Law of Total Probability, we can rewrite the
denominator: $$\begin{aligned}
P(\text{Decay|Dead}) = \frac{P(\text{Dead|Decay})P(\text{Decay})}{P(\text{Dead|Decay})P(\text{Decay}) + P(\text{Dead|Not Decay})P(\text{Not Decay})}
\end{aligned}$$ We know that: $$\begin{aligned}
    P(\text{Dead|Decay}) &= 90\% = 0.9\\
    P(\text{Dead|Not Decay}) &= 10\% = 0.1\\
    P(\text{Decay}) &= 20\% = 0.2
\end{aligned}$$ Plugging these numbers, we have: $$\begin{aligned}
P(\text{Decay|Dead}) &= \frac{0.9\times 0.2}{0.9 \times 0.2 + 0.1 \times (1-0.2)}\\
=\frac{18}{26}
\end{aligned}$$

# END SOLUTION

# END SUBPROB 

# BEGIN SUBPROB

Quantum superposition is a mind-bending and
counter-intuitive concept in physics. In the Schrödinger's cat scenario, when the box is closed, the cat can be **both dead and alive** simultaneously. However, once we open the box and observe, the superposition collapses, and the cat must be either dead or alive, not both. 

The Venn Diagram below depicts the Schrödinger's cat scenario
with the box closed. In this diagram, the black dotted line is the event of cat dead, the red dashed line denotes the event of cat being alive, and the shaded region is the event of decay.

<center><img src="../assets/images/wi24-midterm2/venn_diag.png" width="630" height="330"></center>

<br>

Based on this Venn diagram, which of the following is true? Select all
that apply:

[ ] Decay is independent of Cat Dead
[ ] Decay is independent of Cat Alive
ensp;
[ ] Cat Dead and Cat Alive are mutually exclusive.
[ ] Cat Dead, Cat Alive, and Decay form a partition of the sample
space.
[ ] None of Above.

# BEGIN SOLUTION
Statements 1 and 2 are true. Statements 3, 4, and 5 are false.

<br>

When two events are independent, the following statement is true:
$P(\text{Event 1}) = P(\text{Event 1} | \text{Event 2})$. So for statement 1, we need to show: $P(\text{Decay}) = P(\text{Decay} | \text{Cat Dead})$

- $P(\text{Decay})$ is the fraction of the **total Venn Diagram** that is green.
- $P(\text{Decay}|\text{Cat Dead})$ is the fraction of the **"Cat Dead" region** that is green.

These two fractions look the same. So that means the independence equation holds, and statement 1 is true.

We can do the same thing but instead with the "Cat Alive" region to also show that statement 2 is true.

The "Cat Alive" and "Cat Dead" regions intersect, implying those two events can occur at the same time. If two events can occur at the same time, they are not mutually exclusive, so statement 3 is false.

A partition of a sample is a _perfect division_ the sample space into a bunch of little pieces, without any overlaps or empty space. For this problem, it would mean finding a way to perfectly divide the Venn Diagram. You cannot divide the Venn Diagram into the regions "Cat Dead", "Cat Alive", and "Decay"; go ahead and try, no matter how you slice it the overlaps will mess up the division. This means that "Cat Dead", "Cat Alive", and "Decay" do not form a partition of the sample, so statement 4 is false.

Since statements one and two were true, the answer cannot be none of the above, so statement 5 is false.

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

You're given the following probabilities:

-   $P$(Cat Dead $\cup$ Decay) = $\frac{4}{5}$

-   $P$(Cat Alive $\cup$ Decay) = $\frac{1}{2}$

-   $P$(Cat Alive $\cup$ Cat Dead) = 1

-   $P$(Decay) = $\frac{1}{5}$

Using the Venn diagram in Problem 3.2, calculate the probability for
Schrodinger's cat to be in the superposition state (i.e. both dead and
alive):

# BEGIN SOLUTION

Since we know that the decay is independent to cat's state, we have:
$$\begin{aligned}
    P(\text{Dead} \cup \text{Decay}) &= P(\text{Dead}) + P(\text{Decay}) - P(\text{Dead} \cap \text{Decay})\\
    &=P(\text{Dead}) + P(\text{Decay}) - P(\text{Dead})\cdot P(\text{Decay}) = \frac{4}{5}
\end{aligned}$$ 

Similarly, we have: 
$$\begin{aligned}
    P(\text{Alive} \cup \text{Decay}) &= P(\text{Alive}) + P(\text{Decay}) - P(\text{Alive} \cap \text{Decay})\\
    &=P(\text{Alive}) + P(\text{Decay}) - P(\text{Alive})\cdot P(\text{Decay}) = \frac{1}{2}
\end{aligned}$$ 

Plugging in $P(\text{Decay})$ = $\frac{1}{5}$, we have:
$$\begin{aligned}
    &P(\text{Dead}) + \frac{1}{5} - \frac{1}{5} P(\text{Dead}) = \frac{4}{5}\\
    \\
    &P(\text{Alive}) + \frac{1}{5} - \frac{1}{5} P(\text{Alive}) = \frac{1}{2}\\
    \\
\end{aligned}$$ 

Solving these two equations, we have: 
$$\begin{aligned}
    &P(\text{Dead}) = \frac{3}{4}\\
    \\
    &P(\text{Alive}) = \frac{3}{8}\\
    \\
\end{aligned}$$ 

The probability of superposition state is P(Alive $\cap$ Dead). Since we know that P(Alive $\cup$ Dead) = 1 we have:

$$\begin{aligned}
    P(\text{Alive} \cup \text{Dead}) &= P(\text{Alive}) + P(\text{Dead}) - P(\text{Alive} \cap \text{Dead})\\
\end{aligned}$$ 

Rearranging terms, we have: 
$$\begin{aligned}
    P(\text{Alive} \cap \text{Dead}) &= P(\text{Alive}) + P(\text{Dead}) - P(\text{Alive} \cup \text{Dead})\\
    &= \frac{3}{4} + \frac{3}{8} - 1\\
    \\
    &= \frac{6}{8} + \frac{3}{8} - 1\\
    \\
    &=\frac{1}{8}
\end{aligned}$$

# END SOLUTION

# END SUBPROB

# END PROB