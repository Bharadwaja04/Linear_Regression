# Simple Linear Regression from Scratch (Gradient Descent)

This repository contains a simple implementation of **Linear Regression using Gradient Descent** written in Python, without using scikit-learn.  

It demonstrates how a regression line is fitted on a dataset by minimizing the Mean Squared Error (MSE) loss function.

---

## 📌 Features
- Implemented **from scratch** (no `sklearn`).
- Gradient Descent optimization for slope (`m`) and intercept (`b`).
- Loss visualization across epochs.
- Line fit visualization against training data.
- Custom `predict` method for new inputs.

---

## 📂 Files
- `linear_regression.ipynb` → Jupyter Notebook containing implementation and experiments.
- `linear_regression.py` (optional) → Python script if you want a standalone class.
- `README.md` → Documentation.

---

## 📖 Theory (Quick Recap)
We aim to fit the line:

\[
y = mx + b
\]

The loss function (Mean Squared Error):

\[
J(m, b) = \frac{1}{n} \sum_{i=1}^n (y_i - (mx_i + b))^2
\]

Gradients:
\[
\frac{\partial J}{\partial m} = -\frac{2}{n} \sum x_i (y_i - (mx_i + b))
\]
\[
\frac{\partial J}{\partial b} = -\frac{2}{n} \sum (y_i - (mx_i + b))
\]

Update rules:
\[
m := m - \eta \cdot \frac{\partial J}{\partial m}
\]
\[
b := b - \eta \cdot \frac{\partial J}{\partial b}
\]

Where:
- \( m \) → slope
- \( b \) → intercept
- \( \eta \) → learning rate

---

## 🚀 Usage

### 1. Clone the repository
```bash
git clone https://github.com/your-username/simple-linear-regression-scratch.git
cd simple-linear-regression-scratch
