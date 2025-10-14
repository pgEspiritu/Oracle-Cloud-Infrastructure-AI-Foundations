# 📄 OCI Vision – Document AI Overview

## 🧠 What Is Document AI?

**OCI Vision** offers a powerful second capability known as **Document AI**, designed for understanding and processing **document images** and **PDFs**.  

This feature allows developers and businesses to extract, classify, and interpret information from:
- 🖼️ **Image files:** JPEG, PNG, TIFF  
- 📄 **Scanned documents:** PDFs  
- 📷 **Photographs containing text**

It leverages **machine learning** and **computer vision** to automate the reading and understanding of documents — even in challenging scenarios.

---

## 🧩 Key Features of Document AI

### 🔠 Text Recognition (OCR)
Also known as **Optical Character Recognition**, this feature:
- Extracts text from scanned or photographed documents  
- Handles **non-trivial cases** such as:
  - ✍️ Handwritten text  
  - 📐 Tilted, shaded, or rotated documents  
- Converts visual text into editable and searchable digital text  

✅ *Example:* Extracting handwritten notes from a photographed meeting agenda.

---

### 🗂️ Document Classification
Automatically **categorizes documents** into **10 distinct types** using:
- Visual appearance  
- High-level layout features  
- Extracted keywords  

Useful for workflows where actions depend on document type, such as:
- 🧾 **Invoice**  
- 🧍‍♂️ **Resume**  
- 🧾 **Receipt**  
- 🏢 **Contract**  

✅ *Example:* Automatically routing resumes to HR and invoices to accounting.

---

### 🌐 Language Detection
Unlike traditional text-based detection, OCI Vision analyzes **visual text features** to determine the **document’s language**.

- Works even when textual content is limited or partially obscured.  
- Supports multilingual environments and global document processing.  

✅ *Example:* Detecting French handwriting or Japanese printed text from scanned pages.

---

### 📊 Table Extraction
Identifies and extracts **tabular data** from documents.  
This feature:
- Recognizes **table structures**, even when formatting is irregular  
- Converts table content into **structured, machine-readable form**  

✅ *Example:* Extracting product lists or pricing tables from invoices.

---

### 🔑 Key-Value Extraction
Automatically detects and pairs **common business fields** with their corresponding **values**, such as:
- 🏪 Merchant Name  
- 📅 Transaction Date  
- 💵 Total Amount  
- 🧾 Line Items  

There are **13 predefined field types** supported, enabling accurate extraction of critical information from receipts and transactional documents.

✅ *Example:* Extracting totals and merchant details from a photographed restaurant receipt.

---

## ✅ Summary

| Feature | Description | Example Use Case |
|----------|-------------|------------------|
| 🔠 **Text Recognition (OCR)** | Extracts text, including handwritten or rotated documents | Digitize scanned forms |
| 🗂️ **Document Classification** | Categorizes docs into 10 types | Route invoices or resumes automatically |
| 🌐 **Language Detection** | Determines the language visually | Process multilingual documents |
| 📊 **Table Extraction** | Reads tables and converts to structured data | Extract pricing from invoices |
| 🔑 **Key-Value Extraction** | Identifies common receipt fields | Extract totals and transaction info |

---

**OCI Vision Document AI** brings intelligence and automation to your document workflows — turning static images into actionable, structured data.

