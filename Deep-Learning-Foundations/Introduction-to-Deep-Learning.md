# Deep Learning

Deep learning is a **subset of machine learning** that focuses on training **artificial neural networks (ANNs)** to solve tasks, such as image classification.  
A very important quality of ANN is that it can process **raw data** (like image pixels) and automatically **extract patterns** (features) to predict outcomes.

---

## Example: Handwritten Digit Recognition

Suppose we have a set of handwritten images of digits (0–9). Since everyone writes digits differently, how can a machine recognize them?

- **Input:** ANN accepts image pixels  
- **Processing:** Extracts patterns like edges and curves  
- **Prediction:** Correlates patterns with outcomes (which digit is present)  

In short, ANN learns internal representations of raw data and predicts outcomes without requiring us to manually specify features.

---

## Why Deep Learning?

- In traditional ML, **features must be specified manually**.  
- With deep learning, **features are extracted automatically** from raw data.  
- Internal representations are built layer by layer to predict outcomes.  
- Deep learning supports **parallel computation** (using GPUs), enabling scalability and performance on large datasets.

---

## A Brief History of Deep Learning

- **1950s:** Concepts of artificial neurons, perceptron, and multi-layer perceptrons introduced.  
- **1980s:** Backpropagation developed for training neural networks.  
- **1990s:** Convolutional Neural Networks (CNNs) introduced for image analysis.  
- **2000s:** GPUs adopted for training neural networks.  
- **2010s:** Affordable GPUs fueled widespread adoption in computer vision, NLP, and speech recognition.  
- **2012:** Breakthrough models like **AlexNet** and **Deep-Q Network (DQN)** emerged.  
- **2016 onward:** Generative deep learning (GANs, transformers) became popular.  
- **Today:** Used in large language models, generative AI, and across industries.

---

## Applications of Deep Learning

### By Data Type
- **Images:** Image classification, object detection, facial recognition, segmentation  
- **Text:** Translation, summarization, sentiment analysis, question answering  
- **Audio:** Speech-to-text, music generation, voice recognition  
- **Video:** Activity recognition, video analytics  

### By Architectures
- **CNN (Convolutional Neural Networks):** Best for image-related tasks  
- **RNN / LSTM (Recurrent Neural Networks):** Good for sequential/text data  
- **Transformers:** State-of-the-art for text, NLP, and generative tasks  
- **GANs (Generative Adversarial Networks):** For image and media generation  
- **Diffusion Models:** For advanced text-to-image generation

---

## Artificial Neural Networks (ANN)

ANNs are **inspired by the human brain**, made up of interconnected nodes called **neurons**.

### Components of ANN
1. **Layers**  
   - Input layer  
   - Hidden layers (optional, often multiple)  
   - Output layer  

2. **Neurons**  
   - Computational units that process inputs and generate outputs  

3. **Weights**  
   - Strength of connections between neurons  

4. **Activation Functions**  
   - Apply transformations to weighted sums to introduce non-linearity  

5. **Bias**  
   - Provides flexibility to the model by shifting activation thresholds  

---

## Example: Training ANN on Handwritten Digits

- **Input layer:** 28×28 = 784 pixels  
- **Hidden layers:** Two hidden layers with 16 neurons each  
- **Output layer:** 10 neurons (representing digits 0–9)  

### Training Process
1. Feed an image (e.g., digit “2”) into the ANN.  
2. ANN produces an output (e.g., predicts digit “6”).  
3. Calculate error (expected: 2, predicted: 6).  
4. Use **backpropagation algorithm** to adjust weights.  
5. Repeat with thousands of images.  

Over time, the ANN **minimizes errors** and predicts correct digits.  
This iterative process of weight adjustment is called **model training**.

---

## Summary

- Deep learning is a powerful subset of ML that automatically learns features from raw data.  
- Fueled by GPUs and large datasets, it powers applications from **computer vision** to **NLP** and **generative AI**.  
- ANN, CNNs, RNNs, transformers, and GANs are key architectures for different tasks.  
- Training is performed using **backpropagation** and large amounts of data to achieve high accuracy.  

