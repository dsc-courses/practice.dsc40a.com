# BEGIN PROB

<i>Source: DSC 40A Midterm Take-Home Exam, August 1, 2025, Exercise 2</i>

Consider training data $\{(\vec{x}_i, y_i)\}_{i=1}^n$, with $\vec{x}_i\in \mathbb{R}^d$ and $y_i \in \mathbb{R}$. Let $\mathbf{Z}$ be the design matrix, $\vec{y} = [y_1 \dots y_n]^T$, and model $f(\vec{w},b;\vec{x}) = \vec{w}^\top \vec{x} + b$.

# BEGIN SUBPROB

(a) Suppose $\vec{x}_i^{(1)} = \lambda \vec{x}_i^{(2)}$ for some $\lambda \neq 0$. Prove that a minimizer $\theta^\ast = [b^\ast\;\vec{w}^\ast]^T$ for the mean squared error is not unique.

# BEGIN SOLUTION

<!-- Solution here -->

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

(b) Let $R_1$ be optimal MSE with all features. Delete the first feature to get new MSE $R_2$. Is $R_2 > R_1$? Explain.

# BEGIN SOLUTION

<!-- Solution here -->

# END SOLUTION

# END SUBPROB

# BEGIN SUBPROB

(c) Modify design matrix by adding interaction terms $\vec{x}^{(3)}\vec{x}^{(4)}, \vec{x}^{(1)}\vec{x}^{(2)}$, polynomial terms $(\vec{x}^{(1)})^2, (\vec{x}^{(3)})^2$, and removing $\vec{x}^{(1)}, \vec{x}^{(5)}$. Is $\widetilde{\mathbf{Z}}^\top \widetilde{\mathbf{Z}}$ invertible?

# BEGIN SOLUTION

<!-- Solution here -->

# END SOLUTION

# END SUBPROB

# END PROB
