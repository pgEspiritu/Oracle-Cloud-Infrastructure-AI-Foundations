# Unsupervised Machine Learning


Unsupervised machine learning is a type of machine learning where there are **no labeled outputs**.  
The algorithm learns the **patterns and relationships** in the data and groups similar items.

---

## Key Idea

In unsupervised machine learning, patterns in the data are explored without being told what to look for.  

- **Example 1 (LEGO analogy):**  
  If you give a child a set of LEGO pieces, they may group them by **color**, **size**, or **type**, even without explicit instructions.  

- **Example 2 (Fruits analogy):**  
  With a basket of apples, bananas, and oranges, you might group:  
  - Round, red fruits → one cluster (apples).  
  - Elongated, yellow fruits → another cluster (bananas).  

This grouping is an **unsupervised learning task**.

---

## Clustering

Clustering is the method of grouping data items based on **similarities**.  

- **Within a cluster** → items are more similar.  
- **Outside the cluster** → items are less similar.  
- **Outliers** → items that don’t fit into any cluster.  

🔹 Example: Grapes have a very different shape and size compared to apples, pears, or strawberries, so they could be considered an **outlier**.

---

## Use Cases of Unsupervised Machine Learning

1. **Market Segmentation**  
   - Input: Purchasing details from an online shop.  
   - Output: Clusters of customers based on buying behavior.  
   - Example: Customers in a certain age group buying protein products could be targeted with sports product ads.  

2. **Outlier Analysis**  
   - Input: Credit card transactions.  
   - Output: Detection of fraudulent transactions as **outliers**.  
   - Example: Very high or unusual recurring payments signal possible fraud.  

3. **Recommendation Systems**  
   - Input: User viewing history (e.g., movies, music).  
   - Output: Clusters of users based on preferences.  
   - Example: Netflix groups users based on movie ratings and genres to recommend new content.  

---

## The Concept of Similarity

**Similarity** measures how close two data points are, with a value between **0 and 1**.  

- The closer the similarity value is to **1**, the more similar the objects.  
- Example: Apple and cherry (both red, round fruits) → high similarity (close to 1).  

Common similarity metrics:  
- Euclidean distance  
- Manhattan distance  
- Cosine similarity  
- Jaccard similarity  

---

## Workflow of Unsupervised Learning

Unsupervised learning follows a process similar to supervised learning, but without labels:

1. **Prepare the Data**  
   - Handle missing values  
   - Normalize or scale features  

2. **Create Similarity Matrix**  
   - Choose appropriate similarity metric (Euclidean, Manhattan, Cosine, Jaccard).  

3. **Run Clustering Algorithm**  
   - Types of clustering algorithms:  
     - Partition-based  
     - Hierarchical-based  
     - Density-based  
     - Distribution-based  

4. **Interpret Results & Adjust**  
   - Evaluate clusters at both cluster and item level.  
   - Iteratively refine preprocessing, similarity measures, and algorithms.  
   - No "ground truth" exists, so evaluation is exploratory.  

---

## Summary

Unsupervised learning helps discover hidden patterns and structures in unlabeled data.  
Through **clustering**, we can group similar items, detect anomalies, and provide recommendations.  
Its applications are seen in market segmentation, fraud detection, and recommendation engines.  

---

© 2025 Oracle University  
Privacy / Do Not Sell My Info · Contact Us · Terms of Use · Cookie Preferences · Ad Choices
