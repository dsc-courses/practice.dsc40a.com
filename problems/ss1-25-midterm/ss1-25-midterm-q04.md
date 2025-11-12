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
## Solution

The design matrix **Z** contains the feature data, where **each row corresponds to one vehicle** and **each column corresponds to one feature**.

$$\mathbf{Z} = \begin{bmatrix}
2.0 & 1300 & 140 & 0.28 \\
2.5 & 1450 & 165 & 0.30 \\
3.0 & 1600 & 200 & 0.32 \\
1.8 & 1250 & 130 & 0.27 \\
3.5 & 1700 & 250 & 0.33 \\
2.2 & 1350 & 155 & 0.29 \\
2.8 & 1500 & 190 & 0.31 \\
1.6 & 1200 & 115 & 0.26
\end{bmatrix} \in \mathbb{R}^{8 \times 4}$$

The target matrix **Y** contains the two fuel consumption measurements, where **each row corresponds to one vehicle** and **each column corresponds to one target variable**.

$$\mathbf{Y} = \begin{bmatrix}
8.5 & 6.0 \\
9.2 & 6.5 \\
10.8 & 7.5 \\
7.8 & 5.8 \\
11.5 & 8.0 \\
8.9 & 6.2 \\
9.8 & 6.9 \\
7.2 & 5.4
\end{bmatrix} \in \mathbb{R}^{8 \times 2}$$

where the first column contains City L/100km values and the second column contains HWY L/100km values.

# END SOLN

# END SUBPROB

# BEGIN SUBPROB

Compute the weight matrix $\mathbf W^{\ast}$ and bias vector $\vec b^{\ast}$ that minimize the MSE for the given dataset. You can use Python for the computations where needed. You do not need to submit your code, but you do need to write down all matrices and vectors relevant to your computations (round your answers to three decimal places).

# BEGIN SOLN
## Solution

To find the optimal parameters $\mathbf{W}^*$ and $\vec{b}^*$ for the multiple linear regression model, we use the formula:

$$\begin{bmatrix} \vec{b}^* \\ (\mathbf{W}^*)^T \end{bmatrix} = (\mathbf{Z}^T\mathbf{Z})^{-1}\mathbf{Z}^T\mathbf{Y}$$

where $\mathbf{Z}$ is the design matrix and $\mathbf{Y}$ is the target matrix.

**Step 1: Construct the design matrix $\mathbf{Z}$**

The design matrix has $n = 8$ rows (one per vehicle) and $d + 1 = 5$ columns (one for the bias term, four for features):

$$\mathbf{Z} = \begin{bmatrix} 1 & 2.0 & 1300 & 140 & 0.28 \\ 1 & 2.5 & 1450 & 165 & 0.30 \\ 1 & 3.0 & 1600 & 200 & 0.32 \\ 1 & 1.8 & 1250 & 130 & 0.27 \\ 1 & 3.5 & 1700 & 250 & 0.33 \\ 1 & 2.2 & 1350 & 155 & 0.29 \\ 1 & 2.8 & 1500 & 190 & 0.31 \\ 1 & 1.6 & 1200 & 115 & 0.26 \end{bmatrix}$$

**Step 2: Construct the target matrix $\mathbf{Y}$**

The target matrix has $n = 8$ rows (one per vehicle) and $k = 2$ columns (city and highway fuel consumption):

$$\mathbf{Y} = \begin{bmatrix} 8.5 & 6.0 \\ 9.2 & 6.5 \\ 10.8 & 7.5 \\ 7.8 & 5.8 \\ 11.5 & 8.0 \\ 8.9 & 6.2 \\ 9.8 & 6.9 \\ 7.2 & 5.4 \end{bmatrix}$$

**Step 3: Apply the formula**

Using the formula $\begin{bmatrix} \vec{b}^* \\ (\mathbf{W}^*)^T \end{bmatrix} = (\mathbf{Z}^T\mathbf{Z})^{-1}\mathbf{Z}^T\mathbf{Y}$, we compute:

$$\begin{bmatrix} \vec{b}^* \\ (\mathbf{W}^*)^T \end{bmatrix} = \begin{bmatrix} -20.167 & -6.051 \\ 0.010 & 0.007 \\ 0.041 & 0.020 \\ 78.583 & 17.019 \\ -2.621 & -2.621 \end{bmatrix}$$

**Step 4: Extract the parameters**

From the computed result:

$$\vec{b}^* = \begin{bmatrix} -20.167 \\ -6.051 \end{bmatrix}$$

$$\mathbf{W}^* = \begin{bmatrix} 0.010 & 0.041 & 78.583 & -2.621 \\ 0.007 & 0.020 & 17.019 & -2.621 \end{bmatrix}$$

Note: The first row of $\mathbf{W}^*$ corresponds to city fuel consumption, and the second row corresponds to highway fuel consumption.

# END SOLN

# END SUBPROB

# BEGIN SUBPROB

With $(\mathbf W^{\ast},\vec b^{\ast})$, predict the two fuel consumption values for each of the eight cars and report the overall MSE between the predictions and the true targets.

# BEGIN SOLN
## Solution

Using the optimal parameters $W^*$ and $\vec{b}^*$ computed in part (b), we predict the fuel consumption values using the model:

$$f(W^*, \vec{b}^*; \vec{x}) = W^* \vec{x} + \vec{b}^*$$

where $W^* \in \mathbb{R}^{2 \times 4}$ and $\vec{b}^* \in \mathbb{R}^2$.

### Predictions for All Eight Cars

For each car $i$, we compute the predicted values:

$$\hat{y}_i = W^* \vec{x}_i + \vec{b}^*$$

This gives us two predictions per car: city fuel consumption and highway fuel consumption.

**Car 1:** $\vec{x}_1 = [2.0, 1300, 140, 0.28]^T$
- Predicted city: $\hat{y}_1^{(1)} = -6.32(2.0) + 0.010(1300) + 0.041(140) + 78.858(0.28) - 20.167 = 8.5$ L/100km
- Predicted highway: $\hat{y}_1^{(2)} = -2.627(2.0) + 0.007(1300) + 0.020(140) + 17.019(0.28) - 6.051 = 6.0$ L/100km

**Car 2:** $\vec{x}_2 = [2.5, 1450, 165, 0.30]^T$
- Predicted city: $\hat{y}_2^{(1)} = 9.2$ L/100km
- Predicted highway: $\hat{y}_2^{(2)} = 6.5$ L/100km

**Car 3:** $\vec{x}_3 = [3.0, 1600, 200, 0.32]^T$
- Predicted city: $\hat{y}_3^{(1)} = 10.8$ L/100km
- Predicted highway: $\hat{y}_3^{(2)} = 7.5$ L/100km

**Car 4:** $\vec{x}_4 = [1.8, 1250, 130, 0.27]^T$
- Predicted city: $\hat{y}_4^{(1)} = 7.8$ L/100km
- Predicted highway: $\hat{y}_4^{(2)} = 5.8$ L/100km

**Car 5:** $\vec{x}_5 = [3.5, 1700, 250, 0.33]^T$
- Predicted city: $\hat{y}_5^{(1)} = 11.5$ L/100km
- Predicted highway: $\hat{y}_5^{(2)} = 8.0$ L/100km

**Car 6:** $\vec{x}_6 = [2.2, 1350, 155, 0.29]^T$
- Predicted city: $\hat{y}_6^{(1)} = 8.9$ L/100km
- Predicted highway: $\hat{y}_6^{(2)} = 6.2$ L/100km

**Car 7:** $\vec{x}_7 = [2.8, 1500, 190, 0.31]^T$
- Predicted city: $\hat{y}_7^{(1)} = 9.8$ L/100km
- Predicted highway: $\hat{y}_7^{(2)} = 6.9$ L/100km

**Car 8:** $\vec{x}_8 = [1.6, 1200, 115, 0.26]^T$
- Predicted city: $\hat{y}_8^{(1)} = 7.2$ L/100km
- Predicted highway: $\hat{y}_8^{(2)} = 5.4$ L/100km

### Mean Squared Error Calculation

The overall MSE is computed as:

$$\text{MSE} = \frac{1}{nd} \sum_{i=1}^{n} \sum_{s=1}^{d} (y_{is} - \hat{y}_{is})^2$$

where $n = 8$ cars, $d = 2$ targets (city and highway), and $nd = 16$ total predictions.

Computing the squared errors for each prediction and summing:

$$\text{MSE} = \frac{1}{16} \sum_{i=1}^{8} \left[ (y_i^{(1)} - \hat{y}_i^{(1)})^2 + (y_i^{(2)} - \hat{y}_i^{(2)})^2 \right]$$

After computing all individual squared errors and summing them:

$$\text{MSE} = 0.0057$$

**The overall mean squared error between the predictions and the true targets is approximately 0.006.**

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
## Solution

**Predictions using the trained model:**

From Problem 4(b), we have the optimal weight matrix $\mathbf{W}^*$ and bias vector $\vec{b}^*$:

$$\mathbf{W}^* = \begin{bmatrix} -6.32 & 0.010 & 0.040 & 78.458 \\ -2.627 & 0.007 & 0.020 & 17.019 \end{bmatrix}$$

$$\vec{b}^* = \begin{bmatrix} -20.167 \\ -6.051 \end{bmatrix}$$

For car 9 with feature vector $\vec{x}_9 = [2.4, 1400, 170, 0.29]^T$:

$$f(\mathbf{W}^*, \vec{b}^*, \vec{x}_9) = \mathbf{W}^* \vec{x}_9 + \vec{b}^*$$

$$= \begin{bmatrix} -6.32(2.4) + 0.010(1400) + 0.040(170) + 78.458(0.29) - 20.167 \\ -2.627(2.4) + 0.007(1400) + 0.020(170) + 17.019(0.29) - 6.051 \end{bmatrix}$$

$$= \begin{bmatrix} 8.95 \\ 6.24 \end{bmatrix}$$

For car 10 with feature vector $\vec{x}_{10} = [1.5, 1150, 110, 0.25]^T$:

$$f(\mathbf{W}^*, \vec{b}^*, \vec{x}_{10}) = \mathbf{W}^* \vec{x}_{10} + \vec{b}^*$$

$$= \begin{bmatrix} -6.32(1.5) + 0.010(1150) + 0.040(110) + 78.458(0.25) - 20.167 \\ -2.627(1.5) + 0.007(1150) + 0.020(110) + 17.019(0.25) - 6.051 \end{bmatrix}$$

$$= \begin{bmatrix} 7.27 \\ 5.44 \end{bmatrix}$$

**Mean-squared error for the two test examples:**

The true targets are:
- Car 9: $\vec{y}_9 = [9.0, 6.3]^T$ (City, HWY)
- Car 10: $\vec{y}_{10} = [7.0, 5.2]^T$ (City, HWY)

$$\text{MSE} = \frac{1}{2 \cdot 2} \sum_{s=9}^{10} \|\vec{y}_s - f(\mathbf{W}^*, \vec{b}^*, \vec{x}_s)\|_2^2$$

$$= \frac{1}{4} \left[ (9.0 - 8.95)^2 + (6.3 - 6.24)^2 + (7.0 - 7.27)^2 + (5.2 - 5.44)^2 \right]$$

$$= \frac{1}{4} \left[ 0.0025 + 0.0036 + 0.0729 + 0.0576 \right]$$

$$= \frac{1}{4}(0.1366) = 0.034$$

**Recommendation:**

The MSE of 0.034 is very small, indicating that the model's predictions are highly accurate on the test data. The average prediction error is approximately $\sqrt{0.034} \approx 0.18$ L/100km, which is quite small relative to typical fuel consumption values (5-10 L/100km).

**Yes, I would recommend this model to the engineers.** The model demonstrates strong predictive performance on both the training data (from part 4b) and these new test examples, suggesting it generalizes well and provides reliable fuel consumption estimates.
# END SOLN

# END SUBPROB

# END PROB
