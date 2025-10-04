# Lesson: Introduction to Anaconda & Jupyter Notebook

## 🐍 What is Anaconda?
Anaconda is an **open-source distribution of Python and R** for data science and machine learning.  
It simplifies **package management** and **deployment**, making it easy to get started with data projects.  

Think of it as a **toolbox preloaded with essential libraries and tools** for machine learning and data science.  

---

## 🔑 Why Use Anaconda?
1. **📦 Package Management**  
   - Quickly install and manage data science libraries and dependencies.  

2. **🧩 Isolated Environments**  
   - Work on multiple projects with different package versions, without conflicts.  

3. **🖥️ Anaconda Navigator**  
   - A GUI to manage environments, install packages, and launch Jupyter Notebooks **without command line**.  

4. **🌍 Cross-Platform**  
   - Available for **Windows, Mac, and Linux**.  

---

## 📓 Jupyter Notebook
One of the most powerful tools included with Anaconda is **Jupyter Notebook**.  

- An **Interactive Development Environment (IDE)**.  
- Allows creation and sharing of documents with:  
  - Live code  
  - Equations  
  - Visualizations  
  - Explanatory text  

This makes it **perfect for prototyping, data exploration, and interactive presentations**.  

---

## 🚀 Launching Jupyter Notebook
When you start Jupyter Notebook:  

- A local server runs on your machine.  
- Your browser opens a Jupyter tab with three main sections:  
  - **Files** → Shows all your folders and notebooks.  
  - **Running** → Shows active notebooks or terminals.  
  - **Clusters** → For parallel processing (not covered in this lesson).  

---

## 📂 Creating a Project Notebook
1. Create a new folder (e.g., `ML Demo`).  
2. Inside the folder, create a new **Python 3 Notebook**.  
3. Rename it to `ML Demo 1`.  

---

## 🐍 First Python Code in Jupyter

Inside the notebook, let’s try a simple program that **adds two numbers**.

```python
# This program adds two numbers

# Define variables
num1 = 1
num2 = 4

# Add 2 numbers
sum = num1 + num2
```

▶️ When executed (Shift + Enter), the output will be:

```python
The sum of 1 and 4 is 5
```

---

## 📝 Summary

- Anaconda = Distribution for data science (with package management & environments).
- Navigator = GUI for managing environments and packages.
- Jupyter Notebook = IDE for interactive coding, exploration, and presentations.
- You can start coding immediately by running Python cells in Jupyter.
# Display the result
print("The sum of {} and {} is {}".format(num1, num2, sum))
