# BEGIN PROB

<i>Source: [Summer Session 2 2024 Midterm](../ss2-24-midterm/index.html), Problem 2a-b</i>

Prove the following statement or provide a counterexample: 

# BEGIN SUBPROB

If a vector $\vec{v}$ is orthogonal to a vector $\vec{w}$, then $\vec{v}$ is also orthogonal to the projection of an arbitrary vector $\vec{u}$ onto $\vec{w}$.

# BEGIN SOLUTION

The statement above is true.

Let the following information hold:

- $c$ is a scalar.
- $c\vec{w}$ is the projection of $\vec{u}$ onto $\vec{w}$.

When a vector is orthogonal to another their dot product will equal zero. This means $\vec{v} \cdot \vec{w} = 0$.

From lecture we know:
$$c\vec{w} = \frac{\vec{w} \cdot \vec{u}}{\vec{u} \cdot \vec{u}} \cdot \vec{w}$$

So, now we can solve $c\vec{w} \cdot \vec{v} = \frac{\vec{w} \cdot \vec{u} \cdot \vec{w} \cdot \vec{v}}{\vec{u} \cdot \vec{u}}$. The numerator becomes zero because $\vec{v} \cdot \vec{w} = 0$ and anything multiplied by zero will also be zero. This means the projection of $\vec{u}$ onto $\vec{w}$ is orthogonal to $\vec v$.

<average>52</average>

# END SOLUTION


# END SUBPROB


# BEGIN SUBPROB

If a vector $\vec{v}$ is orthogonal to a vector $\vec{w}$, then $\vec{v}$ is also orthogonal to the projection of $\vec{w}$ onto an arbitrary vector $\vec{u}$.

# BEGIN SOLUTION

This statement is true.

The projection of $\vec w$ onto $\vec u$ gives us the formula $\frac{\vec w \cdot \vec u}{\vec u \cdot \vec u} \vec u$. This projection is a scalar multiple of $\vec u$. This means that the projection of $\vec w$ onto $\vec u$ lies along the direction of $\vec u$.

Furthermore, we know that $\vec v$ is orthogonal to $\vec w$, which means $\vec v \cdot \vec w = 0$.

We need to prove that $\vec v \cdot \frac{\vec w \cdot \vec u}{\vec u \cdot \vec u} \vec u = 0$ to say the statement is true. To do this we simplify the equation. Recall that $\frac{\vec w \cdot \vec u}{\vec u \cdot \vec u}$ is just a scalar!

$$
\vec v \cdot \frac{\vec w \cdot \vec u}{\vec u \cdot \vec u} \vec u = \frac{\vec w \cdot \vec u}{\vec u \cdot \vec u} (\vec v \cdot \vec u)
$$

We can pull scalars out of the dot product!

Since we know $\vec v$ is orthogonal to $\vec w$, this implies that $\vec v$ is also orthogonal to any component of $\vec w$. This means $\vec v$ is also orthogonal to the projection of $\vec w$ onto $\vec u$.

<average>50</average>

# END SOLUTION
    


# END SUBPROB


# END PROB