# BEGIN PROB

<i>Source: [Summer Session 2 2024 Midterm](../ss2-24-midterm/index.html), Problem 2c</i>

Consider the following information:

- $\vec{v}$ is an $n$-dimensional vector.
- $M$ is an $m \times n$ matrix.
- $N$ is an $n \times n$ matrix.
- $s$ is a scalar.

Select the dimensionality of each of the objects below:


# BEGIN SUBPROB

$M \vec{v}$

( ) An $n \times n$ matrix.
( ) An $m \times m$ matrix.
( ) An $n \times m$ matrix.
( ) An $m$-dimensional vector.
( ) An $n$-dimensional vector.
( ) A scalar.
( ) Invalid operation.

    
# BEGIN SOLUTION

An $m$-dimensional vector.

We know the following information:

- $M$ is an $m \times n$ matrix.
- $\vec{v}$ is an $n$-dimensional vector.

This means:

$$
M = \begin{bmatrix}
& & \\
& & \\
& & \\
\end{bmatrix}_{m \times n}
\text{ and }
\vec{v} = \begin{bmatrix}
& \\
& \\
\end{bmatrix}_{n \times 1}
$$

When you multiply $M \vec{v}$ the $n$ will both cancel out leaving you with an object with the size $\begin{bmatrix}& \\& \\& \\\end{bmatrix}_{m \times 1}$, which is an $m$-dimensional vector.

<average>87</average>


# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

$M^T M$

( ) An $n \times n$ matrix.
( ) An $m \times m$ matrix.
( ) An $n \times m$ matrix.
( ) An $m$-dimensional vector.
( ) An $n$-dimensional vector.
( ) A scalar.
( ) Invalid operation.

# BEGIN SOLUTION

An $n \times n$ matrix.

We know the following information:

- $M$ is an $m \times n$ matrix.

This means:

$$
M^T = \begin{bmatrix}
& & & \\
& & & \\
\end{bmatrix}_{n \times m}
\text{ and }
M = \begin{bmatrix}
& & \\
& & \\
& & \\
\end{bmatrix}_{m \times n}
$$

When you multiply $M^T M$ the $m$ will both cancel out leaving you with an object with the size $\begin{bmatrix}& & \\& & \\\end{bmatrix}_{n \times n}$, which is an $n \times n$ matrix.

<average>87</average>

# END SOLUTION
    


# END SUBPROB


# BEGIN SUBPROB

$\vec{v}^T N \vec{v}$

( ) An $n \times n$ matrix.
( ) An $m \times m$ matrix.
( ) An $n \times m$ matrix.
( ) An $m$-dimensional vector.
( ) An $n$-dimensional vector.
( ) A scalar.
( ) Invalid operation.

# BEGIN SOLUTION

A scalar.

We know the following information:

- $\vec{v}$ is an $n$-dimensional vector.
- $N$ is an $n \times n$ matrix.

This means:

$$
\vec{v}^T = \begin{bmatrix}
& &
\end{bmatrix}_{1 \times n}
\text{, }
N = \begin{bmatrix}
& & \\
& & \\
\end{bmatrix}_{n \times n}
\text{, and }
\vec{v} = \begin{bmatrix}
& \\
& \\
\end{bmatrix}_{n \times 1}
$$

When you multiply $\vec{v}^T N$ the $n$ will both cancel out leaving you with an object with the size
$\begin{bmatrix}& &\end{bmatrix}_{1 \times n}$. When you multiply this object by $\vec{v}$ the $n$ will cancel out again leaving you with an object with the size $\begin{bmatrix}&\end{bmatrix}_{1 \times 1}$, which is a scalar.

<average>93</average>

# END SOLUTION
    


# END SUBPROB

# BEGIN SUBPROB

$N \vec{v} + s \vec{v}$

( ) An $n \times n$ matrix.
( ) An $m \times m$ matrix.
( ) An $n \times m$ matrix.
( ) An $m$-dimensional vector.
( ) An $n$-dimensional vector.
( ) A scalar.
( ) Invalid operation.

# BEGIN SOLUTION

An $n$-dimensional vector.

We know the following information:

- $\vec{v}$ is an $n$-dimensional vector.
- $N$ is an $n \times n$ matrix.
- $s$ is a scalar.

This means:

$$
\vec{v} = \begin{bmatrix}
& \\
& \\
\end{bmatrix}_{n \times 1}
\text{, }
N = \begin{bmatrix}
& & \\
& & \\
\end{bmatrix}_{n \times n}
\text{, and }
s = \begin{bmatrix}
&
\end{bmatrix}_{1 \times 1}
$$

When you multiply $N \vec{v}$ the $n$ will both cancel out leaving you with an object with the size $\begin{bmatrix}& \\& \\\end{bmatrix}_{n \times 1}$. When you multiply $s \vec{v}$ the dimensions of $\vec{v}$ does not change, so you will have an object with the size $\begin{bmatrix}& \\& \\\end{bmatrix}_{n \times 1}$. When you add these vectors the dimension will not change, so you are left with an $n$-dimensional vector.

<average>87</average>

# END SOLUTION
    


# END SUBPROB

# BEGIN SUBPROB

$M^T M \vec{v}$

( ) An $n \times n$ matrix.
( ) An $m \times m$ matrix.
( ) An $n \times m$ matrix.
( ) An $m$-dimensional vector.
( ) An $n$-dimensional vector.
( ) A scalar.
( ) Invalid operation.

# BEGIN SOLUTION

An $n$-dimensional vector.

We know the following information:

- $\vec{v}$ is an $n$-dimensional vector.
- $M$ is an $m \times n$ matrix.
- $M^T$ is an $n \times m$ matrix.

This means:

$$
M^T = \begin{bmatrix}
& & & \\
& & & \\
\end{bmatrix}_{n \times m}
\text{, }
M = \begin{bmatrix}
& & \\
& & \\
& & \\
\end{bmatrix}_{m \times n}
\text{, and }
\vec{v} = \begin{bmatrix}
& \\
& \\
\end{bmatrix}_{n \times 1}
$$

When you multiply $M^T M$ the $m$ will both cancel out leaving you with an object with the size $\begin{bmatrix}& & \\& & \\\end{bmatrix}_{n \times n}$, which is an $n \times n$ matrix.

When you multiply $\begin{bmatrix}& & \\& & \\\end{bmatrix}_{n \times n} \times \begin{bmatrix}& \\&\\\end{bmatrix}_{n \times 1}$ the $n$ will cancel out leaving you with an $n$-dimensional vector.

<average>81</average>

# END SOLUTION
    


# END SUBPROB


# END PROB