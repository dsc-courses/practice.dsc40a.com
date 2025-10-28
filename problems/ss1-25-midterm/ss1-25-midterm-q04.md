# BEGIN PROB
<i>Source: [Summer Session 1 2025 Midterm](../ss1-25-midterm/index.html), Problem 4a-d</i>

An automotive research team wants to build a predictive model that simultaneously estimates two performance metrics of passenger cars:

1. **City fuel consumption** (in $\text{L}/100\text{ km}$),
2. **Highway fuel consumption** (in $\text{L}/100\text{ km}$).

To capture mechanical and aerodynamic factors, the engineers record the following **four** features for each vehicle (all measured on the current model year):

1. **Engine displacement (L)**
2. **Vehicle mass (kg)**
3. **Peak horsepower**
4. **Drag coefficient**

They propose the general linear model

$$
f(\mathbf W,\vec b;\,\vec x) = \mathbf W\,\vec x+\vec b,\qquad\mathbf{W}\in\mathbb{R}^{2\times 4},\; \vec{b}\in\mathbb{R}^2,
$$

where $\vec x\in\mathbb{R}^{4}$ denotes the feature vector for a given car. Data for eight different cars are listed below.

| Feature | $\vec{x}_1$ | $\vec{x}_2$ | $\vec{x}_3$ | $\vec{x}_4$ | $\vec{x}_5$ | $\vec{x}_6$ | $\vec{x}_7$ | $\vec{x}_8$ |
|:--|--:|--:|--:|--:|--:|--:|--:|--:|
| Engine disp. (L) | 2.0 | 2.5 | 3.0 | 1.8 | 3.5 | 2.2 | 2.8 | 1.6 |
| Mass (kg) | 1300 | 1450 | 1600 | 1250 | 1700 | 1350 | 1500 | 1200 |
| Horsepower | 140 | 165 | 200 | 130 | 250 | 155 | 190 | 115 |
| Drag coeff. | 0.28 | 0.30 | 0.32 | 0.27 | 0.33 | 0.29 | 0.31 | 0.26 |
| City L/100km | 8.5 | 9.2 | 10.8 | 7.8 | 11.5 | 8.9 | 9.8 | 7.2 |
| HWY L/100km | 6.0 | 6.5 | 7.5 | 5.8 | 8.0 | 6.2 | 6.9 | 5.4 |

# BEGIN SUBPROB

Write down the design matrix $\mathbf Z$ and the target matrix $\mathbf Y$ from the data in the table.

# BEGIN SOLN
# END SOLN

# END SUBPROB

# BEGIN SUBPROB

Compute the weight matrix $\mathbf W^{\ast}$ and bias vector $\vec b^{\ast}$ that minimize the MSE for the given dataset. You can use Python for the computations where needed. You do not need to submit your code, but you do need to write down all matrices and vectors relevant to your computations (round your answers to three decimal places).

# BEGIN SOLN
# END SOLN

# END SUBPROB

# BEGIN SUBPROB

With $(\mathbf W^{\ast},\vec b^{\ast})$, predict the two fuel consumption values for each of the eight cars and report the overall MSE between the predictions and the true targets.

# BEGIN SOLN
# END SOLN

# END SUBPROB

# BEGIN SUBPROB

The team now measures two additional vehicles:

| Feature | $\vec{x}_9$ | $\vec{x}_{10}$ |
|:--|--:|--:|
| Engine disp. (L) | 2.4 | 1.5 |
| Mass (kg) | 1400 | 1150 |
| Horsepower | 170 | 110 |
| Drag coeff. | 0.29 | 0.25 |
| City L/100km | 9.0 | 7.0 |
| HWY L/100km | 6.3 | 5.2 |

Use your trained model to predict fuel consumption for these two cars. Compute the mean-squared error for the two testing examples and state whether you would recommend the model to the engineers.

# BEGIN SOLN
# END SOLN

# END SUBPROB

# END PROB
