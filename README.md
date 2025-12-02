# 🌸 Iris Clustering Project – Google Colab Notebook  
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1OI5oIj84kS_bllJEhfvYzYuTsp4fy0SO?usp=sharing)

![Python](https://img.shields.io/badge/Python-3.10-blue.svg)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-1.4-orange.svg)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen.svg)

---

## 📌 Project Overview  
This project demonstrates **unsupervised machine learning** using two clustering algorithms applied to the classic **Iris dataset**:

- **KMeans Clustering**
- **Agglomerative (Hierarchical) Clustering**

The entire workflow is performed in **Google Colab**, making it easy to reproduce and explore.  
The aim is to uncover natural groupings within the data and compare how well these clusters align with the true Iris species labels.

---

## 🔗 Access the Notebook  
👉 **Open in Colab:**  
https://colab.research.google.com/drive/1OI5oIj84kS_bllJEhfvYzYuTsp4fy0SO?usp=sharing

---

## 🧠 Learning Objectives

- Understand the Iris dataset  
- Apply KMeans and hierarchical clustering  
- Visualize clusters  
- Compute evaluation metrics (Silhouette Score, ARI, etc.)  
- Interpret clustering quality and dataset structure  

---

## 🗂 Dataset  

The Iris dataset contains **150 samples** of iris flowers with four numeric features:

- Sepal Length  
- Sepal Width  
- Petal Length  
- Petal Width  

Species (used only for evaluation):

- Setosa  
- Versicolor  
- Virginica  

---

## 🧰 Workflow Summary

### **1. Data Loading & Preprocessing**
- Load Iris dataset from scikit-learn  
- Extract feature matrix `X`  
- Apply **StandardScaler** for normalization

### **2. KMeans Clustering**
- Fit KMeans model with `k = 3`  
- Plot clusters  
- Compare predicted clusters to true labels using ARI  

### **3. Hierarchical Clustering (Agglomerative)**
- Fit agglomerative clustering with 3 clusters  
- Visualize cluster assignments  
- Evaluate similarity with true species labels

### **4. Evaluation Metrics**
- **Silhouette Score** – measures cluster separation  
- **Adjusted Rand Index (ARI)** – measures similarity to actual labels  
- **Cluster counts** – helps understand balance  
- Optional: Map clusters → species to compute accuracy

---

# 📊 **Results & Metrics**

## 🔷 **KMeans Clustering Results**

- **Cluster Counts:**
  - Cluster 0 → **53 samples**  
  - Cluster 1 → **50 samples**  
  - Cluster 2 → **47 samples**

- **Silhouette Score:** **`0.4599`**  
  Indicates **moderate separation** between clusters.

- **Adjusted Rand Index (ARI):** **`0.6201`**  
  Shows ~62% agreement with the true species labels.

### **Interpretation**
- Clusters are well-balanced in size.  
- Silhouette score indicates reasonable cluster structure.  
- ARI confirms KMeans captures natural species groupings fairly well.

---

## 🟩 **Agglomerative (Hierarchical) Clustering Results**

- **Cluster Counts:**
  - Cluster 0 → **71 samples**  
  - Cluster 1 → **49 samples**  
  - Cluster 2 → **30 samples**

- **Silhouette Score:** **`0.4467`**  
  Slightly lower than KMeans, but still shows acceptable separation.

- **Adjusted Rand Index (ARI):** **`0.6153`**  
  Very close to KMeans performance (~61.5% alignment).

### **Interpretation**
- Cluster 0 is significantly larger (71 samples), showing cluster imbalance.  
- Slightly lower silhouette score suggests more overlap.  
- Hierarchical clustering still performs well for this dataset.

---

## 📌 **Overall Comparison**

|** Metric**                       | KMeans          | Agglomerative |
|------------------------ -------- |-----------------|---------------|
| **Silhouette Score**             | 0.4599          |     0.4467    |
| **Adjusted Rand Index (ARI)**    | 0.6201          |     0.6153    |
| **Cluster Balance**              | Good            | Less balanced |
| **Performance Summary**          | Slightly better | Very similar but less balanced |

### **Conclusion**
- **KMeans shows marginally better overall performance** on Iris.  
- **Agglomerative clustering is competitive** and reveals similar structure.  
- Both algorithms effectively uncover natural groupings in the data.

---

