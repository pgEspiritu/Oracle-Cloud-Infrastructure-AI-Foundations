# 🧾 OCI Vision – Document AI in Action

## 🔍 Exploring Document AI in the OCI Console

Let’s walk through how **OCI Vision’s Document AI** works directly within the **Oracle Cloud Console**.

---

### 🧾 Example 1: Receipt Analysis

When you open **Document AI**, the **default image** is a **receipt**.

#### 🧠 Step 1: Language and Text Extraction
- The document is **detected as English**.
- **All text elements** from the receipt are automatically extracted.
- The **highlighted areas** on the image indicate the text captured by the model.
- The extracted content is available in two formats:
  - 📄 **Line Format:** Full lines of text  
  - 🔤 **Word Format:** Each word individually separated

This provides both granular and structured extraction views for better data handling.

---

#### 🧩 Step 2: Key-Value Pair Detection
Document AI automatically identifies **key fields** that are common in receipts and matches them with detected values.

| Key Field | Extracted Value |
|------------|----------------|
| 🏪 **Merchant Name** | Example Café |
| 📍 **Merchant Address** | [Detected address] |
| ☎️ **Merchant Phone Number** | [Extracted phone number] |
| ⏰ **Transaction Time** | [Time value] |
| 📅 **Transaction Date** | [Date value] |

These extracted details are **highly useful for expense processing** and downstream accounting workflows.

---

#### 📋 Step 3: Tabular and Line Item Data
- The model identifies **line items** from the receipt, such as purchased products or services.
- Example of extracted items:

| Item | Quantity | Unit Price | Total |
|------|-----------|-------------|--------|
| ☕ **Americano** | 1 | — | — |
| 💧 **Water** | 1 | — | — |

This structured data can easily be integrated into ERP, expense, or finance systems.

---

### 📄 Example 2: Invoice Analysis

Now let’s upload a **different document** — an **invoice image**.

#### 🧠 Step 1: Text Extraction
- The model extracts **all visible text** from the invoice.  
- Everything highlighted represents extracted content — printed, handwritten, or stamped.

#### 🧾 Step 2: Handwritten and Stamped Text Handling
This invoice includes:
- A **stamp** applied after processing by an accounts payable clerk.
- Some **handwritten** notes.
- A partially visible, **faded stamp**, yet the model still extracts legible elements.

✅ Despite these imperfections, **Document AI successfully captures** both printed and handwritten text from the image.

---

#### 📊 Step 3: Table Extraction
Since this document is an **invoice**, the model focuses on **tabular data** such as quantities, descriptions, and totals.

| Quantity | Description | Unit Price | Total |
|-----------|--------------|-------------|--------|
| 2 | Product A | $50 | $100 |
| 1 | Product B | $25 | $25 |

Interestingly, some of the **stamp text** was extracted and placed into the description column —  
showing how the model handles overlapping printed and stamped data without losing accuracy.

---

### ✅ Key Takeaways

| Feature | Description | Example Output |
|----------|-------------|----------------|
| 🔠 **Text Extraction (OCR)** | Captures all visible text, including handwritten or stamped | Extracts full receipt text |
| 🧩 **Key-Value Extraction** | Identifies key fields from receipts | Merchant name, date, amount |
| 📊 **Table Extraction** | Reads tabular data and line items | Invoices and itemized receipts |
| 🧾 **Multi-Format Handling** | Works on receipts, invoices, forms, and PDFs | Handles rotated or shaded scans |
| 🧠 **Language Detection** | Detects document language visually | English (with confidence score) |

---

**OCI Vision Document AI** accurately processes complex documents —  
extracting structured data, key values, and tables, even from handwritten or stamped text —  
enabling automated workflows for **expense management, billing, and record processing**.
