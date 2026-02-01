# MNIST Classification and Autoencoder with PyTorch

This project explores the MNIST handwritten digits dataset using **PyTorch**, covering both **supervised learning (classification)** and **unsupervised learning (autoencoders)**.  
It is designed as a learning-oriented project that demonstrates model training, evaluation, and visualization of learned representations.

---

## 📌 Project Overview

The project is split into two main parts:

1. **Feedforward Neural Network Classifier**
   - Classifies handwritten digits (0–9)
   - Trained using labeled MNIST data
   - Includes visualization of learned first-layer weights

2. **Autoencoder**
   - Learns a compact latent representation of MNIST images
   - Reconstructs images from a lower-dimensional embedding
   - Visualizes original, encoded, and reconstructed images

---

## 🧠 Technologies Used

- Python
- PyTorch
- Torchvision
- Matplotlib
- MNIST Dataset

---

## 🗂️ Code Structure

### Part 1 — MNIST Classifier
- Loads and visualizes MNIST samples
- Defines a fully connected neural network
- Trains the model using Cross Entropy Loss
- Evaluates performance on test data
- Visualizes first-layer weight filters to inspect learned features

### Part 2 — Autoencoder
- Implements a fully connected autoencoder
- Compresses 28×28 images into a latent vector
- Reconstructs images from the latent space
- Uses Mean Squared Error loss
- Displays original, encoded, and reconstructed images

---

## 📊 Model Details

### Classifier Architecture
- Input: 784 (28×28 flattened image)
- Hidden layers: 32 → 64
- Output: 10 classes
- Activation: ReLU
- Optimizer: SGD
- Loss: CrossEntropyLoss

### Autoencoder Architecture
- Encoder: 784 → 128 → 32
- Decoder: 32 → 128 → 784
- Activation: ReLU (hidden), Sigmoid (output)
- Optimizer: Adam
- Loss: MSELoss

---

## 🖼️ Visualizations Included

- Random MNIST sample images
- Learned first-layer weights of the classifier
- Autoencoder reconstructions
- Latent space visualizations

These visualizations help interpret what the models are learning internally.
