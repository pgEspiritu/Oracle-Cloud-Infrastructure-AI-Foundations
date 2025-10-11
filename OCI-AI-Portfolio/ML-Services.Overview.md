# 🧠 Machine Learning Services Overview

---

## 🏗️ Oracle AI and ML Services Architecture

At the top layer of the architecture are **applications** — referring to all the ways AI is consumed:  
- Business applications  
- Business processes  
- Analytics systems  

Between the **application layer** and the **data layer**, you’ll find two main groups:
- **AI Services** (top)
- **Machine Learning Services** (bottom)

We already discussed AI Services in the lesson *“AI Services Overview.”*  
In this lesson, we’ll focus on **OCI Data Science**, which is part of Oracle’s Machine Learning Services.

---

## 🔍 What is OCI Data Science?

**Oracle Cloud Infrastructure (OCI) Data Science** is a **cloud service** designed to serve data scientists throughout the **entire machine learning lifecycle**, with full support for **Python** and **open-source tools**.

OCI Data Science provides a comprehensive set of features, including:
- Model Catalog  
- Projects  
- JupyterLab Notebook  
- Model Training and Management  
- Model Deployment  
- Model Explanation  
- AutoML  
- Integration with open-source libraries  

---

## ⚙️ Core Principles of OCI Data Science

### 1. 🚀 Accelerated
- Designed to **boost the productivity** of individual data scientists.  
- Provides **open-source libraries** and **on-demand compute power** without infrastructure management.  
- Includes **Oracle’s Accelerated Data Science (ADS)** library to streamline workflows.

### 2. 🤝 Collaborative
- Enables teams to **work together efficiently**.  
- Supports **sharing assets**, **reducing duplicate work**, and ensuring **reproducibility** and **auditability** of models.  
- Enhances collaboration and risk management across teams.

### 3. 🏢 Enterprise-Grade
- Integrated with OCI’s **security** and **access control** mechanisms.  
- Underlying infrastructure is **fully managed** — including provisioning, patching, and upgrades.  
- Users can focus purely on solving **business problems** with data science.

---

## 🔬 OCI Data Science: Overview

| **Aspect** | **Description** |
|-------------|-----------------|
| **Purpose** | Rapidly build, train, deploy, and manage machine learning models. |
| **Users** | Data scientists and teams across the ML lifecycle. |
| **Interface** | JupyterLab Notebook with Python support. |
| **Usage** | Models are stored in a **Model Catalog** and deployed to **managed infrastructure**. |

---

## 🧩 Key Components and Terminology

### 📁 Projects
- **Containers** for organizing data science work.  
- Represent **collaborative workspaces** for organizing and documenting assets such as **notebooks** and **models**.  
- A tenancy can have **unlimited projects**.

---

### 📓 Notebook Sessions
- Interactive **JupyterLab environments** for building and training models.  
- Come with **preinstalled open-source libraries**, with the option to add more.  
- Run on **managed OCI infrastructure** — users can choose:
  - CPU or GPU shapes  
  - Compute capacity  
  - Storage allocation  

No manual provisioning is required.

---

### 🧱 Conda Environments
- **Open-source package management system** for Python.  
- Allows easy **installation, updates, and management** of dependencies.  
- Supports creating, saving, and switching between **environments** in notebook sessions.

---

### ⚡ Accelerated Data Science (ADS) SDK
- **Oracle’s ADS SDK** is a Python library included with OCI Data Science.  
- Simplifies and automates key steps of the **data science workflow**, including:
  - Connecting to data  
  - Exploring and visualizing data  
  - Training models (with **AutoML**)  
  - Evaluating and explaining models  

Also provides easy access to:
- **Model Catalog**
- **Object Storage**
- Other **OCI Services**

---

### 🧮 Models
- Mathematical representations of data and business processes.  
- Created within **notebooks** or **projects**.  
- Can be trained, evaluated, and deployed within OCI Data Science.

---

### 🗂️ Model Catalog
- **Centralized repository** to store, track, share, and manage ML models.  
- Stores **model artifacts** along with metadata:
  - **Git commit info**
  - **Notebook/script details**
  - **Provenance information**  

Models stored in the catalog can:
- Be **shared** across team members.  
- Be **reloaded** into new notebook sessions for continued work.

---

### 🌐 Model Deployments
- Deploy models from the **Model Catalog** as **HTTP endpoints** on **managed infrastructure**.  
- Enables **real-time inference** via **web applications** or **API requests**.  
- Common use: **serving predictions** to production systems.

---

### 🔁 Jobs
- Allow users to define and run **repeatable ML tasks** on **fully managed infrastructure**.  
- Ideal for automating:
  - Data preprocessing  
  - Model retraining  
  - Batch prediction pipelines  

---

## 🏁 Summary

OCI Data Science provides a **complete, managed environment** for the end-to-end machine learning lifecycle — from **data exploration** to **deployment**.

With its:
- **Accelerated workflows**
- **Collaborative environment**
- **Enterprise-grade infrastructure**

…it empowers data scientists to **focus on innovation** rather than infrastructure.
