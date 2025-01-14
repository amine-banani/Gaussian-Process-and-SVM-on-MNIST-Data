# Gaussian Process and SVM on MNIST Data

This project consists of two main parts: implementing **Gaussian Process Regression** for a 2D dataset and using **Support Vector Machines (SVM)** for classification on the MNIST dataset.

---

## Part I: Gaussian Process Regression

### Overview
Gaussian Process Regression is applied to predict the distribution of a function \( f(x) \) based on noisy observations.

### Tasks
1. **Apply Gaussian Process Regression**:
   - Train a model using a **Rational Quadratic Kernel**.
   - Visualize the predictions, including:
     - Training data points.
     - The mean of \( f(x) \) in the range \([-60, 60]\).
     - The 95% confidence interval using visualization tools like `matplotlib`.

2. **Optimize Kernel Parameters**:
   - Use **negative marginal log-likelihood minimization** to optimize kernel parameters.
   - Re-visualize the results with the optimized kernel.

### Input
- **Training Data**: `input.data` (34x2 matrix). Each row corresponds to a 2D point \((X_i, Y_i)\).

### Output
- Visualization of predictions:
  - Mean of \( f(x) \) over the input range.
  - 95% confidence intervals for \( f(x) \).

---

## Part II: SVM on MNIST Dataset

### Overview
SVM models are used to classify digits (0–4) from the MNIST dataset with comparisons across different kernels and parameter tuning.

### Tasks
1. **Kernel Comparison**:
   - Train SVM models using **Linear**, **Polynomial**, and **RBF kernels**.
   - Compare their classification performance.

2. **Hyperparameter Tuning**:
   - Use **C-SVC** (soft-margin SVM) with **grid search** to tune parameters:
     - \( C \): Regularization parameter.
     - \( \gamma \): RBF kernel parameter.

3. **Custom Kernel**:
   - Combine a **Linear Kernel** and an **RBF Kernel** into a single custom kernel.
   - Evaluate its performance compared to standard kernels.

### Input
- **Training Data**: `X_train.csv` (5000x784 matrix) and `Y_train.csv` (5000x1 matrix).
- **Testing Data**: `X_test.csv` (2500x784 matrix) and `Y_test.csv` (2500x1 matrix).

### Output
- Classification results:
  - Accuracy for each kernel type.
  - Confusion matrix for the best-performing model.

---

