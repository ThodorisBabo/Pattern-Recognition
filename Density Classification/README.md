# Parzen & kNN Density Estimation

This project implements **non-parametric probability density estimation** and **classification** using:

- **Parzen Window (Gaussian kernel)**
- **k-Nearest Neighbours (kNN)**

The methods are applied to a **2-dimensional, 3-class dataset**, with extensive visualization of:
- Estimated probability density functions (PDFs)
- The effect of estimator parameters
- Decision boundaries for both classifiers

---

## 📌 Project Overview

The goal of this project is to study and compare non-parametric density-based classifiers by:

- Estimating class-conditional probability densities
- Visualizing PDFs in 3D
- Analyzing the effect of parameters (`h` for Parzen, `k` for kNN)
- Exploring the bias–variance tradeoff
- Visualizing decision boundaries in the feature space

This project emphasizes **understanding behavior and geometry**, not just classification accuracy.

---

## 🧠 Key Concepts Demonstrated

- Parzen window density estimation
- k-Nearest Neighbour density estimation
- Bayesian classification using class-conditional PDFs
- Bias–variance tradeoff
- Non-parametric learning
- Decision boundary visualization
- 3D probability density visualization

---

## 🧰 Technologies Used

- Python
- NumPy
- Pandas
- Matplotlib
- Google Colab

---

## 📊 Dataset

- Synthetic or file-based dataset
- 2 features: `x1`, `x2`
- 3 classes labeled as `{1, 2, 3}`
- Equal number of samples per class

The code supports both loading data from file and generating synthetic data when the original dataset is unavailable.

---

## 🏗️ Implemented Methods

### Parzen Window Density Estimation

- Uses an isotropic **Gaussian kernel**
- Bandwidth parameter: `h`
- Estimates class-conditional densities:
  
\[
p(x) = \frac{1}{N} \sum_{i=1}^{N} K_h(x - x_i)
\]

where \( K_h \) is a Gaussian kernel.

---

### k-Nearest Neighbour Density Estimation

- Density estimated using a hypersphere enclosing the `k` nearest samples
- Density formula:

\[
p(x) = \frac{k}{N \cdot V}
\]

where \( V \) is the area of the circle with radius equal to the distance to the k-th nearest neighbor.

---

## 🧪 Experiments Performed

### 1️⃣ Parzen PDF Visualization (Full Dataset)
- Evaluated for multiple bandwidths:
  - `h = 0.1, 0.3, 0.7`
- 3D surface plots of maximum class PDF

---

### 2️⃣ Parzen with Reduced Dataset
- Uses **75% less data**
- Bandwidth increased proportionally
- Demonstrates bias–variance tradeoff

---

### 3️⃣ kNN PDF Visualization
- Evaluated for:
  - `k = 3, 10, 30`
- Shows effect of neighborhood size on smoothness

---

### 4️⃣ Decision Boundary Visualization

#### Parzen Windows
- Parameters:
  - `h = 0.1, 0.3, 1.5`
- Color-coded decision regions

#### kNN Classifier
- Parameters:
  - `k = 3, 8, 30`
- Shows increasingly smoother boundaries with larger `k`

---

## 📈 Visualizations

- 3D probability density surfaces
- 2D decision boundary plots
- Overlay of training samples
- Color-coded class regions

---

## 📁 Code Structure 

- Imports and setup
- Density estimation functions
- Classifier definition
- Dataset loading / generation
- Feature grid creation
- PDF visualization (Parzen & kNN)
- Reduced data experiments
- Decision boundary visualization
  
---

## 🚀 Possible Extensions

- Use different kernel functions
- Compare with parametric classifiers
- Add classification accuracy evaluation
- Extend to higher-dimensional data
- Implement adaptive bandwidth selection

---
