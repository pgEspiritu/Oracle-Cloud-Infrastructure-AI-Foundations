# 🧠 Overview of OCI AI Services

---

## 🏗️ Oracle AI Architecture

Business applications consume **AI and ML services**, and the foundation of these services is **data**.  
**AI services** contain prebuilt models for specific use cases. Some are **pretrained**, while others can be **additionally trained** by customers with their own data.

AI services can be accessed by calling the **API** for the service—passing in data to be processed—and the service returns a result.  
There’s **no infrastructure to manage** when using AI services.

---

## 💻 Accessing OCI AI Services

OCI AI Services provide multiple methods for access:

### 1. **OCI Console**
- Browser-based interface.  
- Enables access to notebook sessions, data science features, and AI services.

### 2. **REST API**
- Provides programmatic access to service functionality.  
- Requires programming expertise.  
- An API reference is available in the product documentation.

### 3. **Language SDKs**
- Available for **Java, Python, TypeScript/JavaScript, .NET, Go, and Ruby**.  
- Useful for developers integrating AI directly into applications.

### 4. **Command Line Interface (CLI)**
- Provides both quick access and full functionality.  
- Ideal for automation without scripting overhead.

---

## 🤖 OCI AI Service Categories

OCI AI Services are a collection of prebuilt **machine learning models** that simplify the creation of intelligent business applications.  
Models can also be **custom-trained** for higher accuracy in domain-specific use cases.

### Available Services:
- 🗣️ **Digital Assistant**
- 💬 **Language**
- 👁️ **Vision**
- 🎧 **Speech**
- 📄 **Document Understanding**

---

## 🗣️ OCI Language Service

OCI **Language** allows sophisticated **text analysis at scale**.  
Using **pretrained** and **custom models**, you can process unstructured text and extract insights **without data science expertise**.

### 🔹 Pretrained Models
- Language Detection  
- Sentiment Analysis  
- Key Phrase Extraction  
- Text Classification  
- Named Entity Recognition (NER)  
- Personally Identifiable Information (PII) Detection  

### 🔹 Custom Models
- Train for **Named Entity Recognition (NER)** and **Text Classification** using domain-specific datasets.

### 🔹 Text Translation
- Uses **Neural Machine Translation** to translate text across multiple languages.

---

## 👁️ OCI Vision Service

The **Vision Service** enables image upload, detection, and classification of objects.

### 🔹 Pretrained Models
- Object Detection  
- Image Classification  
- Optical Character Recognition (OCR)

### 🔹 Custom Models
- **Custom Object Detection**: Identify specific objects and return bounding boxes.  
- **Custom Image Classification**: Recognize objects and scene-based features in images.

---

## 🎧 OCI Speech Service

The **Speech Service** converts media files into readable text in **JSON** and **SRT** formats.  
It easily transforms spoken content into **highly accurate transcriptions**.

Use cases include:
- Meeting transcription  
- Call analysis  
- Accessibility enhancements  

---

## 📄 OCI Document Understanding

The **Document Understanding Service** detects and classifies text and objects in uploaded documents.  
It supports both **single file** and **batch processing**.

### 🔹 OCR & Text Extraction
- Detects and recognizes text in documents.  
- Provides **word-level** and **line-level** text.  
- Returns **bounding box coordinates**.

### 🔹 Key-Value Extraction
- Extracts structured information from:
  - Receipts  
  - Invoices  
  - Passports  
  - Driver’s licenses  

### 🔹 Table Extraction
- Extracts content in **tabular format**, preserving **row and column** relationships.

### 🔹 Document Classification
- Categorizes documents into specific types automatically.

---

## 🤖 Oracle Digital Assistant

**Oracle Digital Assistant (ODA)** is a platform to create and deploy **AI-driven conversational interfaces**.

### ✨ Key Features
- Engages users with **natural language conversations**.  
- Routes user inputs to the appropriate **skills**.  
- Greets users, lists capabilities, and provides **entry points** into skills.  
- Handles **interruptions**, **disambiguation**, and **exit requests** gracefully.

### 🧩 Typical Flow
1. User interacts with the Digital Assistant.  
2. The system interprets intent and context.  
3. Routes the conversation to the appropriate skill.  
4. Provides intelligent, context-aware responses.

---

## 🏁 Summary

OCI AI Services simplify building intelligent business applications with **prebuilt**, **customizable**, and **scalable AI models**.  
From **language understanding** to **vision**, **speech**, and **document analysis**, OCI offers enterprise-ready tools with no infrastructure overhead.


