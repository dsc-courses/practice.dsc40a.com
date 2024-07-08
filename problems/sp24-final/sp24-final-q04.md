# BEGIN PROB


Consider the vectors $\vec{u}$ and $\vec{v}$, defined below.

$$\vec{u} = \begin{bmatrix} 1 \\ 0 \\ 0 \end{bmatrix} \qquad \vec{v} = \begin{bmatrix} 0 \\ 1 \\ 1 \end{bmatrix}$$

We define $X \in \mathbb{R}^{3 \times 2}$ to be the matrix whose first
column is $\vec u$ and whose second column is $\vec v$.

# BEGIN SUBPROB

In this part only, let
$\vec{y} = \begin{bmatrix} -1 \\ k \\ 252 \end{bmatrix}$.

Find a scalar $k$ such that $\vec{y}$ is in
$\text{span}(\vec u, \vec v)$. Give your answer as a constant with no
variables.

# BEGIN SOLUTION

TODO

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

Show that:
$$(X^TX)^{-1}X^T = \begin{bmatrix} 1 & 0 & 0 \\ 0 & \frac{1}{2} & \frac{1}{2} \end{bmatrix}$$

*Hint: If $A = \begin{bmatrix} a_1 & 0 \\ 0 & a_2 \end{bmatrix}$, then
$A^{-1} = \begin{bmatrix} \frac{1}{a_1} & 0 \\ 0 & \frac{1}{a_2} \end{bmatrix}$.*

# BEGIN SOLUTION

TODO

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

In parts (c) and (d) only, let
$\vec{y} = \begin{bmatrix} 4 \\ 2 \\ 8 \end{bmatrix}$.

Find scalars $a$ and $b$ such that $a \vec u + b \vec v$ is the vector
in $\text{span}(\vec u, \vec v)$ that is as close to $\vec{y}$ as
possible. Give your answers as constants with no variables.

# BEGIN SOLUTION

TODO 

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

Let $\vec{e} = \vec{y} - (a \vec u + b \vec v)$, where $a$ and $b$ are
the values you found in part (c).

What is $\lVert \vec{e} \rVert$?

( ) 0 
( ) correct$3 \sqrt{2}$ 
( ) $4 \sqrt{2}$ 
( ) 6 
( ) $6 \sqrt{2}$ 
( ) $2\sqrt{21}$

# BEGIN SOLUTION

TODO

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

Is it true that, for any vector $\vec{y} \in \mathbb{R}^3$, we can find
scalars $c$ and $d$ such that the sum of the entries in the vector
$\vec{y} - (c \vec u + d \vec v)$ is 0?

( ) Yes, because $\vec{u}$ and $\vec{v}$ are linearly independent.
( ) Yes, because $\vec{u}$ and $\vec{v}$ are orthogonal.
( ) Yes, but for a reason that isn't listed here.
( ) No, because $\vec{y}$ is not necessarily in
$\text{span}(\vec{u}, \vec{v})$.
( ) No, because neither $\vec{u}$ nor $\vec{v}$ is equal to the vector
$\begin{bmatrix} 1 & 1 & 1 \end{bmatrix}^T$.
( ) No, but for a reason that isn't listed here.

# BEGIN SOLUTION

TODO

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

Suppose that $Q \in \mathbb{R}^{100 \times 12}$,
$\vec{s} \in \mathbb{R}^{100}$, and $\vec{f} \in \mathbb{R}^{12}$. What
are the dimensions of the following product?

$$\vec{s}^T Q \vec{f}$$

 
( ) scalar                   
( ) $12 \times 1$ vector    
( ) $100 \times 1$ vector
( ) $100 \times 12$ matrix   
( ) $12 \times 12$ matrix   
( ) $12 \times 100$ matrix
( ) undefined                                            


# BEGIN SOLUTION

TODO

# END SOLUTION

# END SUBPROB

# END PROB