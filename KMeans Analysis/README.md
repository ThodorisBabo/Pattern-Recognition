# KMeans Distances

This project implements **K-Means clustering from scratch** and studies how different  
**distance metrics** affect clustering performance.

The project focuses on **unsupervised learning**, internal validation using **silhouette analysis**,  
and external evaluation using the **Rand Index** with known class labels.

---

## 📌 Project Overview

The project explores K-Means clustering using the following distance measures:
- Euclidean Distance
- Squared Euclidean Distance
- Cosine Distance

A synthetic Seeds-like dataset is used to evaluate clustering behavior, visualize distance structures,  
and compare clustering quality across metrics.

---

## 🧠 Technologies Used
- Python
- NumPy
- Pandas
- Matplotlib
- Scikit-learn

---

## 🗂️ Code Structure

### 1️⃣ Data Preparation
- Generates a synthetic dataset with:
  - 7 numerical features
  - 3 underlying classes
- Separates features (`X`) and labels (`Y`)
- Normalizes data for cosine distance experiments

---

### 2️⃣ Distance and Similarity Analysis
- Computes:
  - Pairwise Euclidean distance matrix
  - Pairwise cosine similarity matrix
- Visualizes both matrices to gain intuition about data structure

---

### 3️⃣ Custom K-Means Implementation
- Implements K-Means from scratch without using `sklearn.cluster`
- Supports multiple distance metrics:
  - Euclidean
  - Squared Euclidean
  - Cosine
- Uses random centroid initialization and iterative refinement

---

### 4️⃣ Silhouette Analysis
- Evaluates clustering quality for:
  - `k = 2` to `k = 10`
- Generates silhouette plots for:
  - Squared Euclidean distance
  - Cosine distance
- Uses average silhouette score to estimate the optimal number of clusters

---

### 5️⃣ External Evaluation (Rand Index)
- Compares clustering results against ground-truth labels
- Runs multiple initializations to reduce randomness
- Reports mean Rand Index for:
  - Squared Euclidean K-Means
  - Cosine K-Means (with normalized data)

---

## 📊 Evaluation Metrics

### Internal Metrics
- **Silhouette Score**
  - Measures cluster cohesion and separation
  - Used to select the number of clusters

### External Metrics
- **Rand Index**
  - Compares predicted clusters to true class labels
  - Measures clustering agreement

---

## 🖼️ Visualizations Included
- Euclidean distance matrix
- Cosine similarity matrix
- Silhouette plots for multiple values of *k*
- Cluster-wise silhouette distributions

These visualizations help interpret how different distance metrics influence clustering behavior.

---

## 🎯 Learning Objectives
- Understand the K-Means clustering algorithm
- Implement distance-based clustering from scratch
- Compare distance metrics in unsupervised learning
- Use silhouette analysis for model selection
- Evaluate clustering using external labels
