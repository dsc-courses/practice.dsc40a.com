# BEGIN PROB

<i>Source: [Summer Session 2 2024 Midterm](../ss2-24-midterm/index.html), Problem 3b</i>

Fill in the blanks for each set of vectors below to accurately describe their relationship and span.

$$\vec{a} = \begin{bmatrix} -2 \\ 1.5 \\ 4 \end{bmatrix} \qquad \vec{b} = \begin{bmatrix} 1 \\ 2 \\ -2.5 \end{bmatrix} \qquad \vec{c} = \begin{bmatrix} -6 \\ 10 \\ 11 \end{bmatrix}$$

"$\vec{a}$, $\vec{b}$, and $\vec{c}$ are  \_\_(i)\_\_, meaning they span a  \_\_(ii)\_\_. The vector  $\vec{a} = \begin{bmatrix} -2 \\ 15 \\ -7 \end{bmatrix}$  \_\_(iii)\_\_ in the span of $\vec{a}$, $\vec{b}$, and $\vec{c}$. $\vec{a}$, $\vec{b}$, and $\vec{c}$ are \textbf{all}  \_\_(iv)\_\_, meaning the angle between them is \_\_(v)\_\_"

# BEGIN SUBPROB

What goes in \_\_(i)\_\_?

( ) linearly independent
( ) linearly dependent

# BEGIN SOLUTION

Linearly Dependent

To check if $\vec{a}, \vec{b}, \vec{c}$ are linearly independent or dependent, it is possible to try a few different linear combinations of two vectors, and see if it equals the third vector. In this case, we can see that $4\vec{a} + 2\vec{b} = \vec{c}$, so they are linearly dependent. 
For a more straight-forward computation, we can arrange these vectors as the columns of a matrix and compute their rank:
$$A = \begin{bmatrix} -2 & 1 & -6 \\ 1.5 & 2 & 10 \\ 4 & -2.5 & 11\end{bmatrix}$$
Then, we can perform row operations to reduce the matrix $A$. This gives us
$$RREF(A) = \begin{bmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 0\end{bmatrix}$$
From here, we see that there only two columns with leading 1s, which implies the vectors are linearly dependent.

<average>94</average>

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

What goes in \_\_(ii)\_\_?

( ) line
( ) plane
( ) cube
( ) unknown

# BEGIN SOLUTION

Plane

We know from above that the three vectors are linearly dependent. It is clear that they all do not lie on the same line, since we can't multiply any single vector by a constant to obtain another vector. If all three vectors were independent, they would span all of $\mathbb{R}^3$, or 3-dimensional space. Since this isn't the case, they must span a plane.

<average>63</average>

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

What goes in \_\_(iii)\_\_?

( ) is
( ) is not
( ) may be

# BEGIN SOLUTION

is not

If $\vec{d}$ was in the span of $\vec{a}, \vec{b}, \vec{c}$, then there should exist constants to fulfill the equation: $$c_1 \vec{a} + c_2 \vec{b} + c_3 \vec{c} = \vec{d}$$
We can set this up as an augmented matrix:
$$A = \begin{bmatrix} -2 & 1 & -6 & -2 \\ 1.5 & 2 & 10 & 15 \\ 4 & -2.5 & 11 & -7 \end{bmatrix}$$
After performing row operations, we obtain:
$$RREF(A) = \begin{bmatrix} 1 & 0 & 4 & 0 \\ 0 & 1 & 2 & 0 \\ 0 & 0 & 0 & 1\end{bmatrix}$$
This tells us our system of equations is inconsistent because the last row implies $0=1$. Therefore, there does not exist a solution, and $\vec{d}$ is not in the span of $\vec{a}, \vec{b}, \vec{c}$.

<average>50</average>

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

What goes in \_\_(iv)\_\_?

( ) orthogonal
( ) collinear
( ) neither orthogonal nor collinear

# BEGIN SOLUTION

neither orthogonal nor collinear

We can tell that $\vec{a}, \vec{b}, \vec{c}$ are not collinear because their span isn't a line. In order to check if these vectors are orthogonal, we can compute the dot product between each pair of vectors; if any of the three dot products are not equal to 0, then they are not orthogonal. 

We see that $\vec{a} \cdot \vec{b} = (-2)(1) + (1.5)(2) + (4)(-2.5) = -9 \neq 0$, so the three vectors together are not orthogonal.

<average>81</average>

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

What goes in \_\_(v)\_\_?

( ) 0 or 180 degrees
( ) something else
( ) 90 degrees

# BEGIN SOLUTION

something else

If two vectors are orthogonal, the angle between them is 90 degrees. If two vectors are collinear, the angle between them is 0 or 180 degrees. Since each pair of the vectors $\vec{a}, \vec{b}, \vec{c}$ are neither of these, then the angles between them must be something else.

<average>81</average>

# END SOLUTION

# END SUBPROB

# END PROB