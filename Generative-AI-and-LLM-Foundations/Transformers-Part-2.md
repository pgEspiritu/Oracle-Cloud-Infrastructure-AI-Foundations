# Transformer Architecture (Part 2)

As we saw earlier, transformer architectures and models have two main parts:  
- The **Encoder** and  
- The **Decoder**  

The **Encoder** reads the input text and encodes it into **embeddings** that capture its meaning.  
The **Decoder** then uses these embeddings to generate the output text.  

At a high level, this is how the encoder-decoder system works — but let’s look at the details.

---

## Tokens and Tokenization

Before diving deeper into the encoder-decoder architecture, let’s first understand **tokens** and **tokenization** — a core concept in large language models (LLMs).

### What are Tokens?

LLMs don’t directly understand words. They understand **tokens**, which can represent:
- An entire word (e.g., “apple”)  
- Part of a word (e.g., “friend” and “ship” from “friendship”)  
- A punctuation symbol (e.g., “,” or “.”)

The number of tokens per word depends on text complexity:
- **Simple text:** ~1 token per word  
- **Complex text:** ~2–3 tokens per word  

For example, a sentence might map to **15 tokens**, with:
- Common words like *many*, *words*, and *map* as single tokens  
- Rare words like *indivisible* split into two tokens  
- Punctuation symbols like commas and periods each having their own token  

Tokenization allows models to process language efficiently and uniformly.

---

## Embeddings

**Embeddings** are **numerical representations** of text.  
They allow machines to understand **semantic relationships** between words or phrases.

An embedding can represent:
- A **word**
- A **phrase**
- A **sentence**
- A **paragraph** — or even multiple paragraphs.

### Example

If we take the phrase:  
> *They sent me a*

The process is as follows:
1. Convert the words into tokens (`They`, `sent`, `me`, `a`).
2. Feed these tokens into the **encoder model**.
3. The encoder outputs **vector representations (embeddings)** for each token.
4. The model also produces an additional embedding representing the **entire sentence**.

These embeddings are vectors — numerical arrays that capture semantic meaning.  
They are fundamental in many modern AI applications.

---

## Use of Embeddings

Embeddings are used extensively in **vector databases** and **semantic search**.  
These techniques allow retrieval of relevant information based on meaning, not just exact keywords.

### Example: Semantic Search with Embeddings

1. Encode each document in a corpus using an encoder model.  
2. Store the resulting embeddings in a **vector database**.  
3. When a user submits a query:
   - Encode the query into an embedding.
   - Compare it to stored document embeddings.
   - Retrieve the most semantically similar document.  

The retrieved content can then be provided to an **LLM** to generate an answer.  
The LLM combines the retrieved context with its general knowledge to produce a meaningful response.

This technique is known as **Retrieval-Augmented Generation (RAG)**.

> **RAG = Retrieval + Generation**  
> Embeddings play a critical role in achieving good retrieval quality.

---

## Decoder Models

**Decoder models** take a sequence of tokens and generate the next token — one at a time.  

### Example
Input: *They sent me a*  
Output (next token): *lion*

The decoder:
1. Computes probabilities across its vocabulary.
2. Chooses the token with the highest probability.
3. Emits that single token.

To generate a complete sequence, the decoder is repeatedly invoked —  
each time producing one token and feeding it back into the model until the sequence ends.

---

## Encoder-Decoder Architecture

The **encoder-decoder architecture** combines both components for **sequence-to-sequence** tasks such as translation.

### How It Works
1. Input text (e.g., English sentence) is **tokenized**.
2. Tokens are fed to the **encoder**, which generates **embeddings**.
3. These embeddings are passed to the **decoder**.
4. The **decoder** generates output tokens **one at a time**, forming the translated sequence.

During generation, each new token is looped back into the decoder along with previous context —  
this self-referential loop continues until the entire output is produced.

---

## Types of Transformer Architectures

Modern transformer-based models can be categorized into three main types:

### 1. Encoder-Only Models
- Focus solely on **understanding input data**.  
- Output embeddings or vector representations.  
- Used in:
  - **Semantic Search**
  - **Vector Databases**
  - **RAG systems**

### 2. Decoder-Only Models
- Focus on **generating sequences** such as text, code, or stories.  
- Produce one token at a time.  
- Used in:
  - **Text generation**
  - **Chatbots**
  - **Creative AI writing**

### 3. Encoder-Decoder Models
- Combine both understanding and generation.  
- Ideal for **sequence-to-sequence** tasks like:
  - **Machine Translation**
  - **Summarization**
  - **Question Answering**

---

## Summary

- **Tokens** are the building blocks of text that models process.  
- **Embeddings** are vectorized meanings of text, enabling semantic understanding.  
- **Encoder models** convert text into embeddings.  
- **Decoder models** generate tokens sequentially.  
- **Encoder-Decoder models** handle both input understanding and output generation.  
- **RAG (Retrieval-Augmented Generation)** leverages embeddings to improve LLM accuracy.
