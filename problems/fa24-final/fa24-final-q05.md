# BEGIN PROB

\[(12 points)\]

You are analyzing the performance of a machine learning model that
predicts the height $h$ of basketballs after being thrown. The model's
error is measured using a loss function $L(h, y_i)$, defined for a
specific observation $y_i$ (the true height of an object) as:
$$L(h, y_i) = \frac{1}{2}(h - y_i)^2 + 3$$ Here, $h$ represents the
predicted height, and $y_i = 2$ is the true height of the object for
this task.

# BEGIN SUBPROB

() Starting from an initial predicted height $h_0 = 0$, perform *two
steps* of the gradient descent algorithm with a learning rate of
$\eta = 0.5$ to obtain predicted heights $h_1, h_2$. *Show all your
calculations.*

# BEGIN SOLUTION

# END SOLUTION

# END SUBPROB

::: responsebox
5in The gradient of the loss function $L(h, y_i)$ with respect to $h$
is: $$\frac{\partial L}{\partial h} = (h - y_i)$$

For $y_i = 2$, this becomes: $$\frac{\partial L}{\partial h} = (h - 2)$$

**Step 1:** Starting at $h_0 = 0$,
$$\frac{\partial L}{\partial h}\bigg|_{h = h_0} = (0 - 2) = -2$$ Update
$h$ using the gradient descent rule:
$$h_1 = h_0 - \eta \cdot \frac{\partial L}{\partial h} = 0 - 0.5 \cdot (-2) = 0 + 1 = 1$$

**Step 2:** Using $h_1 = 1$,
$$\frac{\partial L}{\partial h}\bigg|_{h = h_1} = (1 - 2) = -1$$ Update
$h$:
$$h_2 = h_1 - \eta \cdot \frac{\partial L}{\partial h} = 1 - 0.5 \cdot (-1) = 1 + 0.5 = 1.5$$

Thus, the predicted heights are: $$h_1 = 1, \quad h_2 = 1.5$$
:::

# BEGIN SUBPROB

On the axis below, plot a rough sketch of the following objects:

-   $h_0, h_1, h_2$

-   $L(h, y_i)$

-   The optimal height $h^\ast$.

# BEGIN SOLUTION

# END SOLUTION

# END SUBPROB

::: center
:::

# BEGIN SOLUTION

::: center
:::

The graph above shows:

-   The loss function $L(h, y_i) = \frac{1}{2}(h - 2)^2 + 3$ as a blue
    curve.

-   The initial point $h_0 = 0$, the first update $h_1 = 1$, and the
    second update $h_2 = 1.5$ marked as red points.

-   The optimal height $h^\ast = 2$ shown as a dashed vertical line.

# END SOLUTION

# BEGIN SUBPROB

Determine whether the gradient descent algorithm will converge to the
minimum of the loss function $L(h, y_i)$. *Explain your reasoning.*

# BEGIN SOLUTION

# END SOLUTION

# END SUBPROB

::: responsebox
2in The loss function $L(h, y_i) = \frac{1}{2}(h - y_i)^2 + 3$ is a
convex function because it is a quadratic function of $h$ with a
positive second derivative:
$$\frac{\partial^2 L}{\partial h^2} = 1 > 0$$

Gradient descent will converge to the minimum of a convex function if
the learning rate $\eta$ is small enough, which is the case here.
:::

# END PROB