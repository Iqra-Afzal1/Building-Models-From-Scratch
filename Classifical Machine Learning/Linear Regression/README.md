# Linear Regression From Scratch

> A complete implementation of **Linear Regression** using **Gradient Descent** from scratch with **NumPy**.  
> No machine learning libraries are used for training the model (Later sklearn and PyTorch for comparison)

---

## Project Structure

```text
Linear Regression/
│
├── dataset/
│
├── notebook/
│   └── linear_regression.ipynb
│
├── visualizations/
│   ├── weights_plot.html
│   └── training_animation.html
│
└── README.md
```

## Project Structure
For derivation and explanation, see 'Exaplanation & Derivations' PDF


---

# Algorithm Workflow

```mermaid
flowchart TD

A[Load Dataset]
B[Data Cleaning]
C[Encode Categorical Features]
D[Feature Scaling]
E[Train Test Split]

F[Initialize Parameters]

G[Forward Pass]

H[Compute Predictions]

I[Calculate MSE Loss]

J[Compute Gradients]

K[Update Weights & Bias]

L{Maximum Iterations Reached?}

M[Model Trained]

N[Prediction]

A --> B
B --> C
C --> D
D --> E
E --> F
F --> G
G --> H
H --> I
I --> J
J --> K
K --> L
L -- No --> G
L -- Yes --> M
M --> N
```

---

# Future Improvements

- Mini-Batch Gradient Descent
- Stochastic Gradient Descent (SGD)
- Ridge Regression (L2 Regularization)
- Lasso Regression (L1 Regularization)
- Elastic Net
- Learning Rate Scheduling
- Early Stopping
