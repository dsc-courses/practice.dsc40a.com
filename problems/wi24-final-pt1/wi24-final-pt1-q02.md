# BEGIN PROB

You and a friend independently perform gradient descent on the same function (meaning everything is the same except for the conditions below), but after $200$ iterations, you have different results. Which of the following is sufficient **on its own** to explain the difference in your results? **Select all that apply.**

[ ] The function is nonconvex.
[ ] The function is not differentiable.
[ ] You and your friend chose different learning rates.
[ ] You and your friend chose the same initial predictions.
[ ] None of the above.

# BEGIN SOLUTION

The function is nonconvex and You and your friend chose different learning rates.

If the function is nonconvex it is possible for you and your friend to end in different places if you start in different places. For example if you have a polynomial with a local minima and a global minimum then it is possible you could find the local minima and your friend could find the global minima, which would mean you have different results.

If the function is not differentiable then you cannot perform gradient descent, so this cannot be an answer.

If you and your friend chose different learning rates it is possible to have different results because if you have a really large learning rate you might be hopping over the global minimum without properly converging. Your friend could choose a smaller learning rate, which will allow you to converge to the global minimum.

If you and your friend chose the same initial predictions you are guaranteed to end up in the same spot.

Because two of the option choices are possible the answer cannot be "None of the above."

# END SOLUTION

# END PROB