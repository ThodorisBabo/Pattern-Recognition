# MNIST Autoencoder with 3D Latent Space Visualization

This project implements a **fully connected autoencoder** trained on the MNIST handwritten digits dataset using **PyTorch**.  
The model compresses 28×28 digit images into a **3-dimensional latent space**, enabling direct visualization and exploration of learned representations.

---

## 📌 Project Overview

The goal of this project is to:
- Learn a compact representation of handwritten digits
- Visualize how digits cluster in a low-dimensional latent space
- Generate new digit-like images by sampling from the latent space

Unlike classification tasks, this project focuses on **unsupervised learning** and representation discovery.

---

## 🧠 Key Concepts Demonstrated

- Autoencoders
- Latent space representations
- Dimensionality reduction
- Unsupervised learning
- Generative sampling
- 3D data visualization

---

## 🧰 Technologies Used

- Python
- PyTorch
- Torchvision
- NumPy
- Matplotlib
- MNIST Dataset

---

## 🏗️ Model Architecture

### Encoder
- Input: 784 (28×28 flattened image)
- Hidden layers: 128 → 32
- Latent dimension: **3**
- Activation: ReLU

### Decoder
- Input: 3-dimensional latent vector
- Hidden layers: 32 → 128
- Output: 784
- Activation: ReLU (hidden), Sigmoid (output)

The Sigmoid output ensures reconstructed pixel values remain in the range \([0, 1]\).

---

## ⚙️ Training Details

- Loss function: Mean Squared Error (MSE)
- Optimizer: Adam
- Batch size: 64
- Epochs: 20
- Device: CPU or GPU (automatically selected)

---

## 📊 Latent Space Visualization

After training:
- All MNIST images are encoded into 3-D vectors
- Separate 3D scatter plots are created for:
  - Training set
  - Test set
- Points are color-coded by digit label

This visualization reveals how the autoencoder organizes digits into clusters in latent space, even without using labels during training.

---

## 🎲 Generating New Images

Random points are sampled from the 3-D latent space and passed through the decoder to generate new images.

This demonstrates the **generative capability** of the autoencoder and shows how different regions of the latent space correspond to different digit-like structures.
