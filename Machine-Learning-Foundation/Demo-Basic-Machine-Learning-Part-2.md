# Machine Learning Demo 2 – Extended Workflow

In this demo, we will duplicate our previous notebook and extend it with additional libraries and steps, including preprocessing, model evaluation, and predictions on new data.

---

## Notebook Setup

1. Duplicate the existing notebook and rename it as **MLDemo2**.  
2. Close the old notebook tab and shut it down.  
3. Open **MLDemo2**.  
4. Restart and clear the kernel outputs before proceeding.  

---

## Step 1: Import Additional Libraries

```python
import numpy as np
from sklearn.model_selection import train_test_split
from sklearn.preprocessing import StandardScaler
from sklearn.metrics import accuracy_score
```

## Explanation of Libraries:

- NumPy (np) → Provides numerical computations, arrays, and mathematical functions.
- train_test_split → Splits the dataset into training and testing sets.
- StandardScaler → Standardizes features by scaling them to mean = 0 and standard deviation = 1.
- accuracy_score → Calculates the accuracy of model predictions.

---

## Why Standardization?

Standardization ensures features are on the same scale. Without it, large-valued features (e.g., square footage in house prices) may dominate smaller-valued features (e.g., number of bedrooms).
This helps the model treat all features equally and prevents biased learning.

---

## Why Train/Test Split?
- Divides dataset into training and testing sets.
- Model is trained on training set and evaluated on testing set.
- random_state parameter ensures reproducibility of splits (e.g., random_state=42).

---

## Why Accuracy Score?

- Accuracy = (Correct Predictions) ÷ (Total Predictions).
- Used to evaluate performance on unseen data.
- Helps detect overfitting (when a model only works on training data but fails on new data).

Example: A spam email classifier achieving 95% accuracy means it correctly labels 95 out of 100 emails as spam/not spam.

--

## Step 2: Load Dataset and Split Features/Labels
```python
X = iris_data.drop(["ID", "Species"], axis=1)
y = iris_data["Species"]
```

---

## Step 3: Train/Test Split
```python
X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, random_state=42
)
```
- 80% of data used for training, 20% for testing.
- random_state=42 ensures reproducible results.

---

## Step 4: Standardize Features
```python
scaler = StandardScaler()
X_train_scaled = scaler.fit_transform(X_train)
X_test_scaled = scaler.transform(X_test)
```
- `fit_transform` → Fits scaler on training data and scales it.
- `transform` → Applies same scaling to test data.

---

## Step 5: Train Logistic Regression Model

```python
from sklearn.linear_model import LogisticRegression

model = LogisticRegression()
model.fit(X_train_scaled, y_train)
```

---

## Step 6: Evaluate Model

```python
y_pred = model.predict(X_test_scaled)
accuracy = accuracy_score(y_test, y_pred)
print("Model Accuracy:", accuracy)
```

Example Output:
```yaml
Model Accuracy: 1.0
```
➡️ The model achieved 100% accuracy on the test set.

---

## Step 7: Predict on New Data

```python
new_data = np.array([
    [5.1, 3.5, 1.4, 0.2],   # Example 1
    [6.5, 3.0, 5.2, 2.0],   # Example 2
    [4.9, 3.0, 1.4, 0.2]    # Example 3
])

new_data_scaled = scaler.transform(new_data)
predictions = model.predict(new_data_scaled)

print("Predicted Species:", predictions)
```

Example Output:
```yaml
Predicted Species: ['Iris-setosa' 'Iris-virginica' 'Iris-setosa']
```

---

Summary

In this extended demo, we covered:

- Importing additional libraries
- Data preprocessing with train/test split and standardization
- Training a logistic regression model
- Evaluating model accuracy
- Making predictions on new, unseen data

This reflects a more comprehensive machine learning workflow that ensures models generalize well and avoid overfitting.
