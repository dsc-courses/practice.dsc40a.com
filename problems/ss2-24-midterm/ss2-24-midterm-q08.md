# BEGIN PROB

Fill in the blanks for each set of vectors below to accurately describe their relationship and span.

$$\vec{a} = \begin{bmatrix} -3 \\ -2 \end{bmatrix} \qquad \vec{b} = \begin{bmatrix} -2 \\ 3 \end{bmatrix}$$

"$\vec{a}$ and $\vec{b}$ are  \_\_(i)\_\_, meaning they span a  \_\_(ii)\_\_. The vector  $\vec{a} = \begin{bmatrix} 1 \\ 1 \end{bmatrix}$  \_\_(iii)\_\_ in the span of $\vec{a}$ and $\vec{b}$. $\vec{a}$ and $\vec{b}$ are  \_\_(iv)\_\_, meaning the angle between them is \_\_(v)\_\_"

# BEGIN SUBPROB

What goes in \_\_(i)\_\_?

( ) linearly independent
( ) linearly dependent

# BEGIN SOLUTION

Linearly Independent

We can see that one vector is not a scalar multiple of the other. $\vec{a}$ has both negative components, so we would only be able to obtain scalar multiples with both negative or both positive components. On the other hand, $\vec{b}$ has one negative and one positive component. So they must be linearly independent.

<average>75</average>

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

Any two linearly independent vectors must span a plane. Geometrically, we can think of all scalar multiples of a single vector to lie along a single line. Then, linear combinations of any two vectors pointing in different directions must lie on the same plane.

<average>87</average>

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

What goes in \_\_(iii)\_\_?

( ) is
( ) is not
( ) may be

# BEGIN SOLUTION

is

Similar to Q5, we can tell that $\vec{c}$ lies in the span of $\vec{a}$ and $\vec{b}$ because we are dealing with 2-dimensional vectors, and we know that $\vec{a}$ and $\vec{b}$ span a plane (so they must span all of $\mathbb{R}^2$). $\vec{c}$ exists in 2-dimensional space, so it must exist in the span of $\vec{a}$ and $\vec{b}$.

We can also directly check if $\vec{c}$ lies in the span of $\vec{a}$ and $\vec{b}$ if there exists some constants $c_1$ and $c_2$ such that $c_1 \vec{a} + c_2 \vec{b} = \vec{c}$. Plugging in what we know: $$c_1 \begin{bmatrix} -3 \\ -2 \end{bmatrix} + c_2 \begin{bmatrix} -2 \\ 3 \end{bmatrix} = \begin{bmatrix} 1 \\ 1 \end{bmatrix}$$$ 
This gives us the system of equations:
$$c_1 (-3) + c_2 (-2) = 1$$ 
$$c_1 (-2) + c_2 (3) = 1$$
Solving this system gives us $c_1 = -\frac{5}{13}$, $c_2 = \frac{1}{13}$, which means $\vec{c}$ does lie in the span of $\vec{a}$ and $\vec{b}$.

<average>75</average>

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

What goes in \_\_(iv)\_\_?

( ) orthogonal
( ) collinear
( ) neither orthogonal nor collinear

# BEGIN SOLUTION

Orthogonal

The vectors $\vec{a}$ and $\vec{b}$ are orthogonal if $\vec{a} \cdot \vec{b} = 0$. We can compute $\vec{a} \cdot \vec{b} = (-3)(-2) + (-2)(3) = 6 - 6 = 0$, so $\vec{a}$ and $\vec{b}$ are orthogonal.

<average>87</average>

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

What goes in \_\_(v)\_\_?

( ) 0 or 180 degrees
( ) something else
( ) 90 degrees

# BEGIN SOLUTION

90 degrees

Since $\vec{a}$ and $\vec{b}$ are orthogonal, the angle between them is 90 degrees. 

<average>87</average>

# END SOLUTION

# END SUBPROB

# END PROB