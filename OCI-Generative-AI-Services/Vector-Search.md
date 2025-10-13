# AI Vector Search in Oracle Database 23ai

## Overview

**AI Vector Search** is built directly into **Oracle Database 23ai**.  
In this lesson, we’ll explore:
- The components available in the database  
- How AI Vector Search powers Gen AI pipelines  
- How it integrates with your data and applications  

In previous lessons, we discussed **Large Language Models (LLMs)**, **Generative AI**, and **OCI Gen AI Services**.  
Now, we’ll focus on how Oracle Database 23ai provides **native AI Vector Search** to enable powerful, semantic information retrieval.

---

## Converged Database Approach

While there are single-purpose vector databases, **Oracle Database 23ai** follows a *converged database* approach — supporting multiple data types for AI and data-driven workloads:

- **JSON**
- **XML**
- **Graph**
- **Spatial**
- **Text**
- **Relational**
- **Vectors**

AI Vector Search enhances **information retrieval** by enabling **semantic searches** across structured and unstructured data — a key capability for modern Gen AI systems.

---

## Built-in Vector Search Capabilities

Oracle Database 23ai includes:

- **SQL support** for native vector generation  
- **VECTOR datatype** for storing vector embeddings  
- **SQL syntax and functions** for similarity search  
- **Approximate search index** for high performance and quality  

---

## Using Models in Oracle Database 23ai

You can use models with API calls or **load an ONNX model** into the database.  

For example:
- Load a model such as `resnet_50` into the database.  
- Use the **VECTOR_EMBEDDING** function with the model and a query image.  

```sql
SELECT VECTOR_EMBEDDING(resnet_50 USING image_data) FROM images;
```

This function returns a vector embedding that can be stored in the database.
AI Vector Search can then compare this embedding to others in the table to find similar images.

---

## VECTOR Datatype

The VECTOR datatype allows you to create tables with vector columns, alongside relational data.

Example:
```sql
CREATE TABLE image_vectors (
    id NUMBER,
    image_name VARCHAR2(100),
    embedding VECTOR(512)
);
```
You can also use a simple VECTOR declaration without specifying dimensions.
This design is future-proof — as models evolve, your schema remains compatible with new embedding formats.

----

## Performing Similarity Searches

To compare vectors, Oracle provides the VECTOR_DISTANCE function.

Example:
```sql
SELECT VECTOR_DISTANCE(a.embedding, b.embedding) AS distance
FROM image_vectors a, image_vectors b
WHERE a.id = 1;
```
- The smaller the distance, the more similar the entities.
- The distance metric (e.g., cosine, euclidean) can be specified based on your embedding model.

---

## AI Vector Search in SQL Queries

You can use vector search directly in SQL to find the closest matches.

Example query:
```sql
SELECT job_id, title, city
FROM job_listings
WHERE city IN (SELECT preferred_city FROM applicants WHERE applicant_id = :id)
ORDER BY VECTOR_DISTANCE(resume_embedding, job_embedding)
FETCH FIRST 10 ROWS ONLY;
```

This example combines:
- Applicant data
- Job data
- AI Vector Search
  — all in five lines of SQL.

✅ Single integrated solution
✅ Fully consistent data
✅ Simple to implement

---

## Vector Indexes

Vector indexes enhance performance and control accuracy.

Example:
```sql
CREATE VECTOR INDEX job_vector_idx
ON job_listings(job_embedding)
ORGANIZATION INMEMORY NEIGHBOR GRAPH
DISTANCE COSINE
TARGET ACCURACY 80;
```

Key Options
- ORGANIZATION:
  - INMEMORY NEIGHBOR GRAPH (for in-memory)
  - NEIGHBOR PARTITIONS (for disk-based)
- DISTANCE: Default is COSINE, can be changed per model.
- TARGET ACCURACY: Defines default accuracy for similarity searches.

You can also override accuracy at query time using APPROXIMATE in the FETCH clause.
example:
```sql
SELECT customer_id, name
FROM customers
ORDER BY VECTOR_DISTANCE(query_embedding, customer_embedding)
FETCH APPROXIMATE FIRST 5 ROWS ONLY;
```
If target accuracy = 80%, the approximate results will have ~4 out of 5 correct matches.
If no vector index is available, Oracle may fall back to an exact search.

---

## Similarity Search Over Joins

One major differentiator of Oracle Database 23ai is similarity search over joins — crucial for enterprise data that’s often normalized.

Example query joining three tables (Author, Books, Pages):
```sql
SELECT b.book_title, a.author_name
FROM authors a
JOIN books b ON a.author_id = b.author_id
JOIN pages p ON b.book_id = p.book_id
WHERE VECTOR_DISTANCE(p.page_embedding, :qVec) < 0.2
  AND b.genre = 'Fiction'
  AND a.country = 'India'
FETCH FIRST 5 ROWS ONLY;
```
- Each page has its own embedding.
- The query retrieves the top 5 books with text semantically similar to the query input.

The cost-based optimizer automatically chooses the best join strategy and vector index for performance.

---

## Powering Generative AI Pipelines

AI Vector Search is a core component of modern Gen AI pipelines.

Typical Workflow:
1. Data Sources: Database, CSV, documents, social media, etc.
2. Document Loader: Imports data into the pipeline.
3. Transformation: Summarize, split, or process documents.
4. Embedding Generation: Convert text/images into vectors.
5. Vector Database Storage: Store embeddings in Oracle Database.
6. Similarity Search / RAG: Retrieve relevant data to augment LLM responses.

Oracle Database 23ai enables this entire process natively.

---

## Integration with Third-Party Frameworks
Oracle provides tight integration with frameworks like:
- LangChain
- LlamaIndex

These tools help developers build RAG (Retrieval-Augmented Generation) applications more efficiently.

---

## Benefits of AI Vector Search in Oracle Database 23ai
- Enterprise-grade performance & reliability
- Converged SQL processing for seamless AI-powered queries
- Combines multiple data types: relational, document, spatial, graph, machine learning, and vector
- Efficient orchestration of Gen AI pipelines directly within the database
- Supports both native and external AI frameworks

---

## Conclusion

AI Vector Search in Oracle Database 23ai delivers a powerful, unified platform for building and scaling AI-driven applications.
It allows enterprises to:
- Perform semantic similarity searches
- Integrate structured and unstructured data
- Power Gen AI pipelines natively within the database
