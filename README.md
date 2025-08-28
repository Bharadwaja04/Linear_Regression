# Simple Linear Regression from Scratch

This repository contains a simple implementation of **Linear Regression** in Python, using two approaches:

1. **Normal Equation** (Analytical solution)  
2. **Gradient Descent** (Iterative optimization)  

No scikit-learn is used — everything is coded from scratch.

---

## 📖 Theory

We aim to fit the line:

$$
y = mx + b
$$

### 1️⃣ Normal Equation

Instead of iteratively updating parameters, the optimal solution can be computed directly:

$$
\theta = (X^T X)^{-1} X^T y
$$

Here:
- \( \theta = \begin{bmatrix} b \\ m \end{bmatrix} \)  
- \( X \) is the feature matrix with a bias column (ones for intercept)  
- \( y \) is the target vector  

This gives the **best fit line** in one step (if \( X^T X \) is invertible).  

---

### 2️⃣ Gradient Descent

We minimize the Mean Squared Error (MSE):

$$
J(m, b) = \frac{1}{n} \sum_{i=1}^n \big(y_i - (mx_i + b)\big)^2
$$

Gradients:

$$
\frac{\partial J}{\partial m} = -\frac{2}{n} \sum_{i=1}^n x_i \big(y_i - (mx_i + b)\big)
$$

$$
\frac{\partial J}{\partial b} = -\frac{2}{n} \sum_{i=1}^n \big(y_i - (mx_i + b)\big)
$$

Update rules:

$$
m := m - \eta \cdot \frac{\partial J}{\partial m}
$$

$$
b := b - \eta \cdot \frac{\partial J}{\partial b}
$$

Where:
- \( m \) → slope  
- \( b \) → intercept  
- \( \eta \) → learning rate  

---

## 📊 Visualizations

- Error vs. Epochs curve (to check convergence of Gradient Descent)  
- Regression line plotted against training data  

---

## 🚀 How to Run

```bash
git clone <your-repo-link>
cd <repo-folder>
python linear_regression.py
