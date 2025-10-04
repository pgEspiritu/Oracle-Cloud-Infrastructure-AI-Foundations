# Lesson: Supervised Learning – Classification

## 📘 Regression vs. Classification
In supervised machine learning, the output can be either:

- **Continuous Output → Regression**  
  Example: Predicting house prices (numeric values)  

- **Categorical Output → Classification**  
  Example: Predicting if an email is *spam* or *not spam*  

---

## 📊 What is Classification?
- A **supervised learning technique** that assigns data points to **predefined categories or labels**.  
- The model (classifier) is trained on a **labeled dataset**.  
- Goal: Learn the mapping between **input features** and **class labels**.  

### Examples
- **Binary Classification** → Spam vs. Not Spam  
- **Multi-class Classification** → Sentiment Analysis (Positive, Negative, Neutral)  

---

## ⚙️ Logistic Regression – A Simple Classifier
One common algorithm used for classification is **Logistic Regression**.  
Unlike its name, logistic regression is **not used for regression**, but for classification.  

### Example: Pass/Fail Prediction
- **Input Feature:** Hours of study (independent variable)  
- **Output (Label):** Pass / Fail (binary outcome)  

How it works:  
- More hours studied → Higher chance of passing  
- Fewer hours studied → Higher chance of failing  

---

## 📐 Sigmoid Function
Unlike linear regression (straight line), logistic regression uses an **S-shaped curve**:

\[
\sigma(x) = \frac{1}{1 + e^{-x}}
\]

- The sigmoid function **maps any real value** into a probability between **0 and 1**.  
- Output is interpreted as the **probability of belonging to a class**.  

### Example
- If **Probability > 0.5** → Classify as *Pass*  
- If **Probability < 0.5** → Classify as *Fail*  

📍 Cases:  
- Student studies **6 hours** → Probability = 0.8 → *Pass*  
- Student studies **4 hours** → Probability = 0.2 → *Fail*  

---

## 🌸 Multi-class Classification: Iris Dataset
For multiple categories, logistic regression can also be extended.  

- **Dataset:** Iris Flower Dataset (150 samples)  
- **Features (Inputs):**  
  - Sepal length  
  - Sepal width  
  - Petal length  
  - Petal width  
- **Labels (Outputs):**  
  - Iris-setosa  
  - Iris-versicolor  
  - Iris-virginica  

Since there are **3 classes**, this is a **multi-class classification problem**.  
Logistic regression will be used to classify flowers based on their features.  

---

## 🧮 Summary
- **Classification** = Predicting categorical outcomes (labels)  
- **Binary Classification** → 2 classes (e.g., spam/not spam)  
- **Multi-class Classification** → More than 2 classes (e.g., flower species)  
- **Logistic Regression**:  
  - Uses the **sigmoid function** to output probabilities  
  - Threshold (e.g., 0.5) decides the final class  
- Example: Hours studied → Predict *Pass* or *Fail*  
