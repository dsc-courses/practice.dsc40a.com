# BEGIN PROB

<i>Originally Problem 4 on the Spring 2023 Final Part 2</i>

At Panda Express, there are 18 items available on the
menu. Food is served on plates that are divided into three equal
sections, and all sections of the plate must contain exactly one menu
item.

# BEGIN SUBPROB

Suppose each section of the plate is a different color (in a
clockwise order around the plate, the sections are red, yellow, blue).
How many different-looking plates of food can be created, if we must
have three different menu items on the plate?

One example plate of food has Honey Walnut Shrimp in the red section,
Kung Pao Chicken in the yellow section, and brown rice in the blue
section.


# BEGIN SOLUTION
${18 \choose 3} \cdot 3!$

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

Suppose each section of the plate is a different color (in a
clockwise order around the plate, the sections are red, yellow, blue).
How many different-looking plates of food can be created, if we are
allowed to have the same food in multiple sections?

# BEGIN SOLUTION

$18^3$

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

Suppose each section of the plate is the same color (white).
How many different-looking plates of food can be created, if we must
have three different menu items on the plate?

One example plate of food has, in a clockwise order around the plate,
Eggplant Tofu, Broccoli Beef, and fried rice. This is the same plate as
the one that has, in a clockwise order, Broccoli Beef, fried rice, and
Eggplant Tofu, because one plate can be rotated to look like the other
(this counts as the same.)


# BEGIN SOLUTION

$2 \cdot {18 \choose 3}$

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

Suppose each section of the plate is the same color (white).
Now we'd like to consider what happens if we can have the same food in
multiple sections. What do we need to **add to part (c)'s answer** to
get the number of different-looking plates of food that can be created,
if we are allowed to have the same food in multiple sections?

As before, two plates that can be rotated to look like one another count
as the same.

# BEGIN SOLUTION

$2 \cdot {18 \choose 2} + {18 \choose 1}$

# END SOLUTION

# END SUBPROB

# END PROB