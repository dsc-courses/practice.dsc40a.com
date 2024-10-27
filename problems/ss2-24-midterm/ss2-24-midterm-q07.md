# BEGIN PROB

<i>Source: [Summer Session 2 2024 Midterm](../ss2-24-midterm/index.html), Problem 3c</i>

Fill in the blanks for each set of vectors below to accurately describe their relationship and span.

$$\vec{a} = \begin{bmatrix} -1 \\ 4 \end{bmatrix} \qquad \vec{b} = \begin{bmatrix} 0.5 \\ -2 \end{bmatrix}$$

"$\vec{a}$ and $\vec{b}$ are  \_\_(i)\_\_, meaning they span a  \_\_(ii)\_\_. The vector  $\vec{c} = \begin{bmatrix} -3 \\ 4 \end{bmatrix}$  \_\_(iii)\_\_ in the span of $\vec{a}$ and $\vec{b}$. $\vec{a}$ and $\vec{b}$ are  \_\_(iv)\_\_, meaning the angle between them is  \_\_(v)\_\_"

# BEGIN SUBPROB

What goes in \_\_(i)\_\_?

( ) linearly independent
( ) linearly dependent

# BEGIN SOLUTION

Linearly Dependent

Upon inspection, we can see that $\vec{b} = -\frac{1}{2}\vec{a}$. Therefore, these vectors are linearly dependent.

<average>81</average>

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

What goes in \_\_(ii)\_\_?

( ) line
( ) plane
( ) cube
( ) unknown

# BEGIN SOLUTION

Line

Since we found that $\vec{a}$ and $\vec{b}$ are linearly dependent, they must span a space of only 1-dimension. This means that $\vec{a}$ and $\vec{b}$ lie the same line.

<average>87</average>

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

What goes in \_\_(iii)\_\_?

( ) is
( ) is not
( ) may be

# BEGIN SOLUTION

is not

We know that $\vec{a}$ and $\vec{b}$ span a line consisting only of vectors that are scalar multiples of $\vec{a}$ or $\vec{b}$. We can see that the first component of $\vec{c}$ is three times larger than the first component of $\vec{a}$, but they both share the same second component. This means it is not possible to scale $\vec{a}$ by a constant to obtain $\vec{c}$, and so $\vec{c}$ does not lie on the same line spanned by $\vec{a}$ and $\vec{b}$.

<average>93</average>

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

What goes in \_\_(iv)\_\_?

( ) orthogonal
( ) collinear
( ) neither orthogonal nor collinear

# BEGIN SOLUTION

Collinear

The vectors $\vec{a}$ and $\vec{b}$ are collinear if we can write one vector as a scalar multiple of the other. We saw that $\vec{b} = -\frac{1}{2}\vec{a}$, so they are collinear.

<average>62</average>

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

What goes in \_\_(v)\_\_?

( ) 0 or 180 degrees
( ) something else
( ) 90 degrees

# BEGIN SOLUTION

0 or 180 degrees

If two vectors are collinear, the angle between them is 0 or 180 degrees. This is because they lie on the same line and either point in the same or opposite directions from the origin. 

<average>81</average>

# END SOLUTION

# END SUBPROB

# END PROB