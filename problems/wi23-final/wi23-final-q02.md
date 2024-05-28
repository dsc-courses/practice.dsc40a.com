# BEGIN PROB

<!-- Convexity Problem -->

Let $f(x):\mathbb{R}\to\mathbb{R}$ be a convex function. $f(x)$ is not
necessarily differentiable. Use Jensen's inequality (definition of
convexity) to prove the following: $$\begin{aligned}
            f(1)+f(3)\geq 2f(2).
        
\end{aligned}$$

# BEGIN SOLUTION

This is based on the review question we did in class, with
$x_1=1,x_2=2,x_3=3$.

Jensen's inequality:
$$f(tx_{1}+(1-t)x_{2})\leq tf(x_{1})+(1-t)f(x_{2})$$ Let $x_1=1$,
$x_2=3$, then for $t=0.5, x=tx_{1}+(1-t)x_{2}=2$. Therefore
$$f(x)=f(2) \leq 0.5 (f(x_{1})+f(x_{2})=0.5 (f(1)+f(3))$$
$$2f(2) \leq f(1)+f(3)$$

# END SOLUTION

# END PROB