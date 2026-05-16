# neural-network
# Handwritten Digit Recognition using Neural Networks (MNIST)

A deep learning project for handwritten digit classification using the MNIST dataset and PyTorch.

---

# Project Overview

This project implements a Multi-Layer Perceptron (MLP) neural network to recognize handwritten digits from the MNIST dataset.

The model is trained and evaluated using two different experiments with different:

- Activation Functions
- Hidden Layer Sizes
- Learning Rates

The project also includes:

- Training & Validation
- Model Evaluation
- Accuracy/Loss Visualization
- Sample Predictions

---

# Technologies Used

- Python
- PyTorch
- Torchvision
- NumPy
- Matplotlib

---

# Dataset

Dataset used:

- MNIST Handwritten Digits Dataset

Dataset contains:

- 60,000 Training Images
- 10,000 Test Images
- 10 Classes (Digits 0–9)

Image size:

```text
28 × 28 grayscale images
```

---

# Data Preprocessing

The following preprocessing steps were applied:

- Convert images to tensors
- Normalize pixel values

```python
transform = transforms.Compose([
    transforms.ToTensor(),
    transforms.Normalize((0.5,), (0.5,))
])
```

---

# Model Architecture

The implemented model is a Multi-Layer Perceptron (MLP).

Architecture:

```text
Input Layer (784)
        ↓
Hidden Layer 1
        ↓
ReLU / Tanh
        ↓
Dropout (0.2)
        ↓
Hidden Layer 2
        ↓
ReLU / Tanh
        ↓
Output Layer (10 Classes)
```

---

# Experiments

## Experiment 1

| Parameter | Value |
|---|---|
| Activation Function | ReLU |
| Hidden Size | 128 |
| Learning Rate | 0.001 |
| Optimizer | Adam |

---

## Experiment 2

| Parameter | Value |
|---|---|
| Activation Function | Tanh |
| Hidden Size | 256 |
| Learning Rate | 0.0005 |
| Optimizer | Adam |

---

# Training Details

- Loss Function: CrossEntropyLoss
- Optimizer: Adam
- Batch Size: 64
- Epochs: 10

---

# Evaluation Metrics

The model performance was evaluated using:

- Accuracy
- Loss

---
# Results

The model achieves high accuracy on the MNIST dataset using simple MLP architecture.

Example output:

```text
Experiment 1 Test Accuracy: ~97%
Experiment 2 Test Accuracy: ~98%
```

(Results may vary slightly depending on initialization and hardware.)

---

# Visualization

The project visualizes:

- Training Loss
- Validation Loss
- Training Accuracy
- Validation Accuracy

using Matplotlib.

---

# Sample Predictions

The model predicts handwritten digits from the test dataset and displays sample outputs.

---
# Project Structure
# How to Run

## 1. Clone the repository

```bash
git clone https://github.com/habeba-abubakrmohamed12/neural-network
```

---

## 2. Install dependencies

```bash
pip install torch torchvision matplotlib numpy
```

---

## 3. Run the project

```bash
python main.py
```
