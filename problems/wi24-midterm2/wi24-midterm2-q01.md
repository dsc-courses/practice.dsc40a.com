# BEGIN PROB

<i>Originally Problem 1 on the Second Winter 2024 Midterm.</i>

Quarks is one of the smallest fundamental particles in
physics. There are 6 **types** of quarks: up, down, top, bottom, strange,
charm. Each one of the 6 types of quarks can be in two **states**: quark or antiquark.

# BEGIN SUBPROB

Consider an experiment where we select n quarks uniformly at random. The **result** of the experiment is a description of the **type and state**
of the quark selected. For example, if $n=3$, one possible result is:

-   Selected quark 1 is a top quark.

-   Selected quark 2 is a charm antiquark.

-   Selected quark 3 is a top antiquark.

How many results are possible for this experiment with $n$ quarks?

( ) $6^n$
( ) $9^n$
( ) $12^n$
( ) $18^n$
( ) $36^n$
( ) None of the above.

# BEGIN SOLUTION

$12^n$

For each quark there are $6$ possible types $\times 2$ possible states $= 12$ possibilities. Since our experiment involves independently picking one of these 12 possibilities for each of our $n$ quarks, the total number of results for the experiment is $12^n$.

# END SOLUTION

# END SUBPROB 

# BEGIN SUBPROB

A meson is formed by combining two quarks. In order to form a meson, the two quarks must satisfy the following rules:

-   They must be in **different states**: one must be a quark and 
    the other one must be an anti-quark.

-   The two quarks can be the **same type**: i.e. top quark and top
    antiquark can form a meson.

-   The **order** of quark and antiquark does matter.

Consider an experiment where we select n mesons uniformly at random. How many results are possible for this experiment?

( ) $2^n$
( ) $6^n$
( ) $12^n$
( ) $18^n$
( ) $36^n$
( ) None of the above.

# BEGIN SOLUTION

None of the above ($72^n$).

For making a meson, we need to choose two quarks. The first quark we choose has $6$ possible types $\times 2$ possible states $= 12$ possibilities. However, our second quark cannot have the same state as our first; so the second quark has $6$ possible types $\times 1$ possible state $= 6$ possibilities.

This means a single meson has $12 \times 6 = 72$ possibilities. (If the order of the quark and antiquark did not matter, it would instead be $\frac{72}{2} = 36$ possibilities). So, an experiment where we select $n$ mesons uniformly at random has $72^n$ unique results.

# END SOLUTION

# END SUBPROB

# END PROB