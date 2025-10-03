# Lesson: OCI AI Services Overview

## 🔹 Vision AI Service

The **Vision AI Service** allows us to carry out several tasks:  
- 🖼️ Image Classification  
- 🎯 Object Detection  
- 🔡 Text Detection  
- 📄 Document AI  

---

### Image Classification
- Upload an image → AI analyzes it and assigns **labels with confidence scores**.  
- Example: For an image of vegetation, AI may return `Vegetation (99.23%)`.  
- Example: Zebra images return labels such as `zebra, vegetation, grassland, mammal`.

---

### Object Detection
- Detects **objects within an image** using **bounding boxes**.  
- Example: Traffic image → cars, taxis, and people detected with confidence scores.  
- Example: Basket of fruit → `orange, banana, apple, bowl`.

---

### Text Detection
- Extracts **text from images**, including license plates, numbers, or fonts.  
- Example: Bus image → extracts `M32HOD`, `45`, and other text blocks.  
- Example: Multiple fonts → AI recognizes text across different styles.

---

### Document AI
> **Note:** Document AI is now part of the **Document Understanding Service**, but features remain similar.

- Upload a document/receipt → AI extracts **raw text, key-value pairs, and tables**.  
- Example:  
  - Key Values: Transaction Date, Time, Subtotal, Tax, Total  
  - Tables: Itemized lists, card authorization codes, terminal IDs  

---

## 🔹 OCI AI Language Service

The **Language Service** provides:  
- 📝 Text Analysis  
- 🌐 Text Translation  

---

### Text Analysis
- Uses **pretrained models** for:  
  - 🌍 Language Detection  
  - 🏷️ Text Classification  
  - 😀 Sentiment Analysis (sentence & aspect-level)  
  - 🔑 Key Phrase Extraction  
  - 🆔 PII (Personally Identifiable Information) detection  

**Example:**  
- Language: English  
- Classification: Science & Technology  
- Entities: food, computers, instruments  
- Sentiment: Positive/Negative at sentence-level  

---

### Text Translation
- Supports **multiple source and target languages**.  
- Example: English → French / Japanese  
- Instant translation in just seconds.  
- Also allows **custom model training** with your own datasets.  

---

# ✅ Summary
- **Vision AI**: Image, object, text, and document analysis  
- **Language AI**: Text analysis, classification, sentiment, and translation  
- Both services provide **confidence scores, pretrained models, and custom training options**
