# BEGIN PROB

_Originally Problem 5 on the first Winter 2024 Midterm Exam._

Suppose the following information is given for a linear regression:

$X = \begin{bmatrix}
1 & 2\\
1 & -1
\end{bmatrix}$


$\vec{y} =
    \begin{bmatrix}
    a\\
    b\\
    \end{bmatrix}$ $\vec{w}^{*} =
    \begin{bmatrix}
    1\\
    2\\
    \end{bmatrix}$


Where X is the design matrix, $\vec{y}$ is the observation vector, and
$\vec{w}^{*}$ is the optimal parameter vector. Solve for parameter a and
b using the normal equation, show your work.

# BEGIN SOLUTION

Since $\vec{w}^{*}$ is the optimal parameter vector, it must satisfy the
Normal Equation: 

$$\begin{align*}
        X^{T}X\vec{w} = X^{T}\vec{y}
\end{align*}$$

The left hand side of the equation will read:

\begin{align*}
X^{T}X\vec{w} &=
\begin{bmatrix}
1 & 1\\
2 & -1
\end{bmatrix}

\begin{bmatrix}
1 & 2\\
1 & -1
\end{bmatrix}

\begin{bmatrix}
1\\
2
\end{bmatrix}
\\
&=


\begin{bmatrix}
2 & 1\\
1 & 5
\end{bmatrix}

\begin{bmatrix}
1\\
2
\end{bmatrix}
\\
&=

\begin{bmatrix}
4\\
11
\end{bmatrix}
\end{align*}

The right hand side of the equation is given by:

\begin{align*}
X^{T}\vec{y} &=
\begin{bmatrix}
1 & 1\\
2 & -1
\end{bmatrix}
\begin{bmatrix}
a\\
b
\end{bmatrix}

\\
&=

\begin{bmatrix}
a+b\\
2a-b
\end{bmatrix}
\end{align*}

By setting the left hand side and right hand side equal to each other,
we will obtain the following system of equations:

\begin{align*}
\begin{bmatrix}
4\\
11
\end{bmatrix}

=

\begin{bmatrix}
a+b\\
2a-b
\end{bmatrix}
\end{align*}

So we obtained this set of equations: 

$$\begin{align*}
        &4 = a + b\\
        &11 = 2a-b
\end{align*}$$

To solve this equation set, we can add them together:
$$\begin{align*}
       4+11 &= a + b + 2a -b\\
       3a &= 15\\
       \\
       \\
       \begin{cases}
       a = 5\\
       b = -1\\ 
       \end{cases}
\end{align*}$$

# END SOLUTION

# END PROB