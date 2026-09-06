# Linear Regression with SGD Optimization and Bias Correction

This notebook implements **Linear Regression from scratch** using different variants of **Stochastic Gradient Descent (SGD)** on the Medical Insurance dataset.

## Workflow

1. **Load Dataset** – Loads `insurance.csv`.
2. **Data Quality** – Checks for missing values and duplicate records, then removes duplicates.
3. **Encoding** – Converts categorical features using ordinal encoding and one-hot encoding.
4. **Train-Test Split** – Splits the dataset into training and testing sets.
5. **Feature Scaling** – Standardizes both input features and target values.
6. **Vanilla SGD** – Implements linear regression using stochastic gradient descent.
7. **SGD with Momentum** – Adds momentum to smooth parameter updates and reduce loss fluctuations.
8. **Bias Correction** – Applies bias correction to the momentum estimates.
9. **Evaluation** – Compares model performance using Mean Squared Error (MSE) and visualizes training loss.

## Technologies

* Python
* NumPy
* Pandas
* Scikit-learn
* Matplotlib

## Dataset

The notebook uses the **Medical Cost Personal Dataset** (`insurance.csv`) containing features such as age, sex, BMI, number of children, smoking status, region, and medical charges.

## Key Observation

Vanilla SGD shows higher loss fluctuations, while **SGD with Momentum produces smoother weight updates and generally lower testing MSE**.
