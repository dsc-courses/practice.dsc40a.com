# BEGIN PROB

<i>Source: [Summer Session 2 2024 Midterm](../ss2-24-midterm/index.html), Problem 2d</i>

Consider the following information:

- $A$ is an $m \times n$ matrix.
- $\vec{b}$ is an arbitrary $n$-dimensional vector
- $\vec{c}$ is the $m$-dimensional vector formed by multiplying $A$ with $\vec{b}$.
- $\vec{d}$ is an arbitrary $m$-dimensional vector.
- $\vec{e}$ is the $m$-dimensional vector formed by $\vec{d} - \vec{c}$.


If $\vec{e}$ is orthogonal to every column in $A$, prove that $\vec{b}$ must satisfy the following equation:

$$
A^T A \vec{b} = A^T \vec{d}.
$$

_Hint: If the columns of a matrix $A$ are orthogonal to a vector $\vec{v}$, then $A^T \vec{v} = 0$_.


# BEGIN SOLUTION

To begin with, we know from the bullet points above that $A^T \vec e = 0$ in order for $A^T A \vec{b} = A^T \vec{d}$ to be true. So we start by interpreting $A^T \vec e = 0$ in $\vec e$'s other form $\vec{d} - \vec{c}$. We get $A^T(\vec d - \vec c)$!

We then distribute $A^T$ to get $A^T \vec d - A^T \vec c = 0$. From here we can move $A^T \vec c$ to the right to get $A^T \vec d = A^T \vec c$.

From the third bullet point we find $\vec c = A\vec{b}$, so we can write $A^T \vec d = A^T A \vec b$. Thus we have proved if $\vec{e}$ is orthogonal to every column in $A$, prove that $\vec{b}$ must satisfy the following equation: $A^T A \vec{b} = A^T \vec{d}.$

<average>58</average>

# END SOLUTION

# END PROB