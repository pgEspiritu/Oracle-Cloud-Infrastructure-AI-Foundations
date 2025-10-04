# Machine Learning Process with Logistic Regression

Before we implement a machine learning use case, let's revisit a typical machine learning process, which involves:

1. Loading the data  
2. Preprocessing the data  
3. Training a model  
4. Evaluating the model  
5. Making predictions  

---

## Introduction

The code we will write demonstrates a simple machine learning workflow using **Logistic Regression**, which is a classifier.  

- A **classifier** is a type of algorithm used for classification tasks.  
- **Classification** is a supervised learning problem where the goal is to assign a category or label to an input based on its features.  
- The classifier learns patterns and relationships in training data to make predictions on unseen data.  

In this example, we will:  
- Load the dataset  
- Prepare it for training  
- Train a model  
- Make predictions  
- Print results  

This example provides a **foundational understanding** of how machine learning models are built and used for classification.

---

## Step 1: Import Necessary Libraries

```python
import pandas as pd
from sklearn.linear_model import LogisticRegression
```

- `pandas` is used for data manipulation and provides structures like DataFrames and Series.
- `LogisticRegression` from sklearn is used to build our classifier.

If these libraries are not part of your kernel, install them using:

```bash
conda install -c anaconda scikit-learn
```

---

## Step 2: Load the Dataset
```bash
iris_data = pd.read_csv("iris.csv")
iris_data.head()
```

- Loads the iris dataset into memory.
- Displays the first 5 rows for inspection.
- The dataset contains attributes (features) and species (labels).

---

## Step 3: Split Features and Labels
```bash
X = iris_data.drop(["ID", "Species"], axis=1)
y = iris_data["Species"]
```

- X → Features (attributes of the flowers)
- y → Labels (species of the flowers)
- The ID column is dropped since it’s not useful for classification.

---

## Step 4: Create and Train the Model
```bash
model = LogisticRegression()
model.fit(X, y)
```
- Initializes the Logistic Regression classifier.
- Uses .fit() to train the model on features (X) and labels (y).

---

## Step 5: Make Predictions
```bash
sample_data = [[5.1, 3.5, 1.4, 0.2]]  # Example input
prediction = model.predict(sample_data)
print("Predicted Species:", prediction)
```
- Makes predictions on unseen data.
- Example result:
  ```bash
  Predicted Species: ['Iris-setosa']
  ```

---

## Summary
In this demo, we:
- Loaded a dataset
- Split it into features and labels
- Created and trained a logistic regression model
- Made predictions on new data

This is a basic machine learning workflow that demonstrates how classifiers are used in supervised learning.
