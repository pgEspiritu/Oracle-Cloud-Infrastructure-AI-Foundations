# 🗣️ OCI Speech – Console Walkthrough

## 🧭 Accessing the OCI Speech Console

To explore **OCI Speech**, navigate through the Oracle Cloud Console:

1. From the **main menu**, go to **Analytics & AI**.  
2. Under **AI Services**, select **Speech**.  
3. This opens the **OCI Speech Console page**, where you can manage and create transcription jobs.

---

## 🗂️ Preparing for a Transcription Job

Before you can start using OCI Speech, make sure you have:

- 🎵 **Audio data uploaded** to **Object Storage**  
- 📁 The **correct compartment** selected that contains your bucket  
- 🪣 An **Object Storage bucket** with supported file formats (e.g., `.wav`, `.mp3`)

OCI Speech works directly with **Object Storage**, so the transcription process reads from and writes results to your configured bucket.

---

## ⚙️ Creating a Transcription Job

Follow these steps to create your first transcription job:

1. Click **Create Transcription Job**.
2. Enter a **Job Name** — e.g., `Training`.
3. Confirm or select the **Compartment** where your data resides.
4. Choose the **Object Storage Bucket** containing your audio file.
5. Select the desired **audio file** (for example, `headphones_issue.wav`).
6. Click **Run Job** to start the transcription process.

> 🕒 The job runs quickly — typically within a few seconds, depending on the file size.

---

## 📊 Viewing Job Results

Once the transcription job completes:

1. The **status** changes to ✅ *Succeeded*.  
2. Click the job name to view the **output details**.  
3. Select the **transcribed file** to open the text result.

Example transcription output:

> “I’m having an issue with my wireless headphones.  
> I think my Bluetooth connectivity to the TV is not working.  
> I have high-quality headphones; I know the issue is not with them.  
>  
> Hi, thanks for contacting support.  
> I’m sorry to hear about your Bluetooth issue.”

---

## 🧠 Key Observations

### ✍️ Automatic Punctuation  
OCI Speech intelligently inserts punctuation, making text more natural and readable.

### 🔢 Normalization  
The service converts words like “one hundred percent” into symbolic form (`100%`), enhancing readability and making it ready for analytics or further processing.

### ⚡ Speed & Accuracy  
The job completes in seconds and provides highly accurate results, leveraging Oracle’s deep learning–powered models.

---

## ✅ Summary

| Step | Action | Result |
|------|---------|--------|
| 1️⃣ | Access **Analytics & AI → Speech** | Opens Speech Console |
| 2️⃣ | Select Compartment & Bucket | Prepares input data |
| 3️⃣ | Create Transcription Job | Starts speech-to-text conversion |
| 4️⃣ | Wait for Job Completion | Returns transcription result |
| 5️⃣ | Review Output | View clean, punctuated, normalized text |

OCI Speech in the Console offers an **easy, guided interface** for generating high-quality transcriptions — ready for downstream use in analytics, subtitles, or accessibility solutions.
