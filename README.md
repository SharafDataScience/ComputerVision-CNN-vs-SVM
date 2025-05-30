# Image Recognition Using CNN and SVM

## Project Overview

This project compares **Convolutional Neural Networks (CNNs)** and **Support Vector Machines (SVMs)** for image classification using a subset of the **CIFAR-10 dataset**. The goal is to evaluate the performance and strengths of each method in classifying images across 10 categories.

## Dataset

- **CIFAR-10 (subset)**
  - **Training Images:** 5,000
  - **Test Images:** 1,000
  - **Classes:** 10 (e.g., airplane, automobile, bird, cat, deer, dog, frog, horse, ship, truck)

## Methodologies

### 1. CNN Model

- **Architecture:**
  - Two convolutional layers: 32 and 64 filters, kernel size (3, 3)
  - ReLU activation after each conv layer
  - MaxPooling (2, 2) to reduce spatial size
  - Dropout (0.25) to prevent overfitting
  - Flatten layer to vectorize output
  - Two dense layers with 512 neurons (ReLU)
  - Output layer: 10 neurons with Softmax activation

- **Training Parameters:**
  - Optimizer: Adam
  - Learning Rate: 0.001
  - Loss Function: Categorical Cross-Entropy
  - Epochs: 12

### 2. SVM Model

- **Preprocessing:**
  - Convert RGB images to grayscale
  - Normalize pixel values
  - Extract Histogram of Oriented Gradients (HOG) features
  - Apply StandardScaler for standardization
  - Dimensionality reduction using PCA

- **SVM Configuration:**
  - Kernel: RBF
  - Regularization parameter C = 10

## Results

| Model | Test Accuracy |
|-------|---------------|
| CNN   | 78.4%         |
| SVM   | 54.0%         |

- **CNN Pros:** Learns features automatically, better performance
- **SVM Pros:** Faster training, interpretable features using HOG

## Key Insights

- CNN outperforms SVM in this setup but is more computationally intensive.
- SVMs are simpler and still reasonably accurate with the right feature engineering.
- Model performance depends heavily on dataset size, complexity, and compute power.

## Future Work

- Develop hybrid CNN+SVM model
- Improve CNN with transfer learning
- Handle class imbalance
- Explore larger and diverse datasets
- Improve CNN interpretability using explainability tools


---

> Created by **Abdullah Sharaf (2139533)**
