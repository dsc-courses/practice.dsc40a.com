# BEGIN PROB

<i>Source: [Spring 2023 Final Part 2](../sp23-final-pt2/index.html), Problem 4</i>

At Panda Express, there are $18$ items available on the menu. Food is served on plates that are divided into three equal sections, and all sections of the plate must contain exactly one menu
item.

# BEGIN SUBPROB

Suppose each section of the plate is a different color (in a clockwise order around the plate, the sections are red, yellow, blue). How many different-looking plates of food can be created, if we must have three different menu items on the plate?

One example plate of food has Honey Walnut Shrimp in the red section, Kung Pao Chicken in the yellow section, and brown rice in the blue section.


# BEGIN SOLUTION
${18 \choose 3} \cdot 3!$

This problem is exactly asking for the number of permutations of three elements from a pool of 18 elements, which is 
\begin{align*}
18\cdot17\cdot16 = \frac{18!}{15!} = {18 \choose 3} \cdot 3!
\end{align*}

You should remember that whenever you draw items **without replacement** and the **order matters** then you are calculating a permutation.  Alternatively, you can reason that in the red segment of the plate, you can have any of the 18 different menu items, then for the yellow segment you only have 17 menu items available, since the red already has one, lastly you have 16 items left for the blue part of the plate. Then just multiply all the ways you can choose menu items for each segment getting a total of
\begin{align*}
18\cdot17\cdot16 = {18 \choose 3} \cdot 3!
\end{align*}

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

Suppose each section of the plate is a different color (in a clockwise order around the plate, the sections are red, yellow, blue). How many different-looking plates of food can be created, if we are allowed to have the same food in multiple sections?

# BEGIN SOLUTION

$18^3$

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

Suppose each section of the plate is the same color (white). How many different-looking plates of food can be created, if we must have three different menu items on the plate?

One example plate of food has, in a clockwise order around the plate, Eggplant Tofu, Broccoli Beef, and fried rice. This is the same plate as the one that has, in a clockwise order, Broccoli Beef, fried rice, and Eggplant Tofu, because one plate can be rotated to look like the other (this counts as the same.)


# BEGIN SOLUTION

$2 \cdot {18 \choose 3}$

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

Suppose each section of the plate is the same color (white). Now we'd like to consider what happens if we can have the same food in multiple sections. What do we need to **add to part (c)'s answer** to get the number of different-looking plates of food that can be created, if we are allowed to have the same food in multiple sections?

As before, two plates that can be rotated to look like one another count as the same.

# BEGIN SOLUTION

$2 \cdot {18 \choose 2} + {18 \choose 1}$

# END SOLUTION

# END SUBPROB

# END PROB