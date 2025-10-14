# 🗣️ Oracle Cloud Infrastructure (OCI) Speech

## 🎯 Introduction

**OCI Speech** is a powerful AI service that **converts spoken words into written text** with exceptional accuracy.  
It uses Oracle’s **time-tested acoustic and language models** to transcribe audio or video content automatically, across multiple languages — all without requiring any data science expertise.

---

## 🧩 What OCI Speech Does

OCI Speech unlocks the value in **audio data** by converting it into readable, searchable, and structured text.  
It uses **advanced deep learning** techniques to produce **timestamped, grammatically accurate transcriptions** directly from your audio or video files.

### ⚙️ Key Highlights
- 🎧 **Speech-to-Text Conversion** for audio and video files  
- 🤖 **No Data Science Required** — ready to use with simple API calls  
- ☁️ **Processes Data in Object Storage** — no local infrastructure needed  
- 🕒 **Timestamped, Accurate Transcriptions** for each segment  
- ✍️ **Readable, Normalized Output** that resembles human writing  

---

## 🌐 Language Support

OCI Speech currently supports:
- 🇺🇸 **English**
- 🇪🇸 **Spanish**
- 🇧🇷 **Portuguese**

> 🌍 More languages will be supported in the future.

---

## 🚀 Performance and Efficiency

- ⚡ **Batch Processing:** Submit **multiple files** in a single API call.  
- ⏱️ **Fast Transcription:** Transcribes **hours of audio in under 10 minutes**.  
- 🧩 **Parallel Processing:** Breaks large audio files into smaller **chunks**, transcribes them individually, and then merges them seamlessly into one result.

---

## 📈 Accuracy and Quality

### 🔢 Confidence Scoring
- Each **word** and **entire transcription** includes a **confidence score**, helping developers assess transcription reliability.

### 🧮 Punctuation and Grammar
- OCI Speech **automatically punctuates** text, producing results that are easy to read and ready for downstream processing.

---

## 🎬 SRT File Support (Closed Captions)

OCI Speech supports **SRT**, the most common **subtitle format** for video platforms.  
With SRT output, users can:
- Add **closed captions** to videos  
- Improve **accessibility** and **searchability**  
- Synchronize audio and text with timestamps  

---

## 🧠 Text Normalization

Normalization ensures transcribed text **looks natural**, just like human writing.  
It automatically converts:
- Numbers → digits (e.g., “one hundred” → “100”)  
- Times → standard format (e.g., “five o’clock” → “5:00”)  
- URLs, addresses, and other formats → readable text

Example:

| Raw Transcription | Normalized Text |
|--------------------|----------------|
| “one two three Main Street” | “123 Main St.” |
| “five thirty PM” | “5:30 PM” |

---

## 🚫 Profanity Filtering

OCI Speech includes **profanity control** to manage sensitive content with three modes:

| Mode | Description | Example |
|------|--------------|----------|
| **Remove** | Replaces the entire word with asterisks | `****` |
| **Mask** | Keeps the first letter and masks the rest | `s****` |
| **Tag** | Leaves the word intact but adds a tag in metadata | `slur_word (tagged)` |

This feature ensures output text is suitable for business or public use.

---

## ✅ Summary

**OCI Speech** simplifies and accelerates audio-to-text transcription by combining accuracy, speed, and flexibility.  

| Feature | Description |
|----------|--------------|
| 🗣️ Speech-to-Text | Converts speech from audio/video to text |
| 🌍 Multi-Language | Supports English, Spanish, and Portuguese |
| ⚡ Batch Processing | Submit multiple files at once |
| 🕒 Fast Performance | Transcribes hours in minutes |
| 📈 Confidence Scores | Measures reliability of output |
| 🧠 Normalization | Produces human-readable text |
| 🚫 Profanity Filter | Removes or masks sensitive words |
| 🎬 SRT Support | Enables subtitles and captions |

OCI Speech empowers developers to build **accessible, AI-driven applications** with **accurate transcriptions**, ready for analytics, search, and media processing.
