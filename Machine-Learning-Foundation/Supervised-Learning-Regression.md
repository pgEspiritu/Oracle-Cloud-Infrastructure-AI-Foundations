# Lesson: Supervised Learning – Linear Regression

## 📘 What is Supervised Learning?
- A **machine learning model** that learns from **labeled data**.  
- Learns the **mapping between input and output**.  
- Similar to a teacher guiding a student: the model is trained with past outcomes and learns the relationships.  

### Typical Applications
- **House Price Prediction**  
  - Input: House size (sq. ft.)  
  - Output: Price of house  
- **Cancer Detection**  
  - Input: Patient’s medical details  
  - Output: Tumor is malignant / not malignant  
- **Sentiment Analysis**  
  - Input: Customer reviews  
  - Output: Positive / Negative / Neutral  
- **Stock Price Prediction**  
  - Input: Opening price, closing price, trading volume  
  - Output: Future stock price  

---

## 📊 Outputs in Supervised Learning
- **Continuous output** → Regression  
- **Categorical output** → Classification  

In this lesson, we focus on **Regression**.  

---

## 🏡 Example: House Price Prediction
We want to predict house prices based on a single input feature: **size of the house (sq. ft.)**.  

- **Input (Independent Feature):** House Size  
- **Output (Dependent Feature):** House Price  
- A **single input-output pair** = training example (tuple)  
- All examples together form the **training dataset**  

### Visualizing the Data
- Plotting house size vs. price on a scatter plot shows:  
  - Larger house size → Higher price  
- Fitting a straight line helps us predict prices for unseen house sizes.  

---

## 📐 The Linear Regression Model
The relationship between input and output can be represented as a **line**:

\[
f(x) = w \cdot x + b
\]

Where:  
- \(x\) = input (house size)  
- \(w\) = slope (rate of change of price per sq. ft.)  
- \(b\) = bias (y-intercept)  

- **Slope (w):** Determines tilt of line  
- **Bias (b):** Shifts the line up/down  

By adjusting slope and bias, we find the **best fitting line**.  

---

## ⚙️ How the Model Learns
1. Start with random slope \(w\) and bias \(b\)  
2. Predict output using the line  
3. Compare predicted vs actual value  
4. Calculate **Error**:  
   \[
   \text{Error} = \text{Predicted Value} - \text{Actual Value}
   \]  
5. Calculate **Loss (Penalty)**:  
   \[
   \text{Loss} = ( \text{Predicted} - \text{Actual} )^2
   \]  
6. Adjust slope & bias to **minimize loss**  
7. Repeat until optimal values are found  

---

## 🧮 Summary
- **Supervised Learning** = Learning from labeled input-output pairs  
- **Regression** = Predicting continuous values  
- **Linear Regression** fits a straight line:  
  \[
  f(x) = w \cdot x + b
  \]  
- Training involves minimizing loss by adjusting slope & bias  
- Once trained, the model can predict new house prices from size input  

