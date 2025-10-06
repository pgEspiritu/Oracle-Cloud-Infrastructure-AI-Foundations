# 📘 Deep Learning for Sequential Data

## 🔹 What Are Sequence Models?  
Sequence models are used to solve problems where the input data is in the form of **sequences**.  
- A sequence is an **ordered list** of data points or events.  
- The goal is to **find patterns and dependencies** within the data and make predictions, classifications, or even generate new sequences.  

---

## 🔹 Applications of Sequence Models  
Some common applications include:  
- **Natural Language Processing (NLP):** machine translation, sentiment analysis, text generation  
- **Speech Recognition:** converting recorded audio into text  
- **Music Generation:** creating original compositions  
- **Gesture Recognition:** interpreting sequences of hand gestures (e.g., sign language recognition)  
- **Time Series Prediction:** forecasting in finance or weather  

---

## 🔹 Recurrent Neural Networks (RNN)  
**Recurrent Neural Networks (RNNs)** are a class of neural networks designed for sequential data.  

### Key Features:  
- Unlike feedforward neural networks, **RNNs have a feedback loop** that allows information to persist across different time steps.  
- Maintain an **internal state (hidden state / memory)** updated as each element of the input sequence is processed.  
- Capture dependencies and patterns that occur across time.  

---

## 🔹 Types of RNN Architectures  
- **One-to-One** → Like feedforward NN, not suited for sequential data.  
- **One-to-Many** → One input → multiple outputs (e.g., music or sequence generation).  
- **Many-to-One** → Multiple inputs → one output (e.g., sentiment analysis from a review).  
- **Many-to-Many** → Multiple inputs → multiple outputs (e.g., machine translation, named entity recognition).  

⚠️ Limitation: RNNs struggle with **long-term dependencies** due to the **vanishing gradient problem**.  

---

## 🔹 Long Short-Term Memory (LSTM)  
To overcome the limitations of RNNs, we use **Long Short-Term Memory (LSTM)** networks.  

### How LSTM Works:  
- Uses **specialized memory cells** and **gating mechanisms** to capture long-term dependencies.  
- Maintains relevant information across long sequences.  
- Helps solve the vanishing gradient problem.  

### LSTM Gates:  
1. **Input Gate** → Decides what new information to add to the memory.  
2. **Forget Gate** → Decides what information to discard/forget.  
3. **Output Gate** → Decides how much of the memory should be exposed as output.  

---

## 🔹 Step-by-Step LSTM Process  
At each time step:  
1. Takes the **current input vector**.  
2. Receives the **previous hidden state** and **cell state**.  
3. Applies the **input, forget, and output gates** to regulate information flow.  
4. Updates the **cell state** accordingly.  
5. Produces the **hidden state output** for the next time step.  

---

✅ With these mechanisms, LSTMs can effectively handle **long-term dependencies** in sequential data, making them powerful for NLP, speech recognition, and time series prediction.  

---
