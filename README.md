# Simple Linear Regression from Scratch (Gradient Descent)

This repository contains a simple implementation of **Linear Regression using Gradient Descent** written in Python, without using scikit-learn.  

It demonstrates how a regression line is fitted on a dataset by minimizing the Mean Squared Error (MSE) loss function.

---

## 📖 Theory (Quick Recap)

We aim to fit the line:

$$
y = mx + b
$$

The loss function (Mean Squared Error):

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
