# 🧠 CIFAR-10 Image Classifier using CNN

This project implements an image classification pipeline using a Convolutional Neural Network (CNN) trained on the [CIFAR-10](https://www.cs.toronto.edu/~kriz/cifar.html) dataset. The model achieves ~75% validation accuracy and includes a clean interface to test predictions on custom images.

## 📁 Dataset Overview

The CIFAR-10 dataset contains 60,000 color images (32x32 pixels) labeled across 10 classes:

- `airplane`, `automobile`, `bird`, `cat`, `deer`, `dog`, `frog`, `horse`, `ship`, `truck`

It is automatically downloaded using `keras.datasets.cifar10`.

---

## 🏗️ Model Architecture

We use a deep CNN (Convolutional Neural Network) built with **Keras Sequential API**:

| Layer               | Description                                                                 |
|--------------------|-----------------------------------------------------------------------------|
| `Conv2D`           | Applies 2D filters to extract local features from the image (edges, textures) |
| `MaxPooling2D`     | Reduces spatial dimensions while retaining the most prominent features       |
| `Flatten`          | Converts 3D feature maps into a 1D vector for dense layers                   |
| `Dense`            | Fully connected layers to learn complex patterns and make predictions        |
| `Dropout` (optional) | Prevents overfitting by randomly turning off neurons during training      |
| `Softmax` output   | Produces class probabilities for the 10 categories                           |

### 📌 Achieved Performance

- **Validation Accuracy**: ~75%
- **Loss Function**: `categorical_crossentropy`
- **Optimizer**: `adam`

---


