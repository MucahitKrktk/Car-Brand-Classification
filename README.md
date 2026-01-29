# 🚗 Car Brand Classification with Computer Vision

![Python](https://img.shields.io/badge/Python-3.x-blue?style=flat&logo=python)
![TensorFlow](https://img.shields.io/badge/Framework-TensorFlow%20%2F%20Keras-orange?style=flat&logo=tensorflow)
![Status](https://img.shields.io/badge/Status-Completed-success)

## 📖 Project Overview
This project focuses on classifying different car brands using advanced **Deep Learning** techniques. Developed as a comprehensive **Computer Vision** term project, it implements and compares two distinct approaches:

1.  **Custom CNN:** A lightweight Convolutional Neural Network designed from scratch.
2.  **VGG16 Transfer Learning:** A high-performance model pre-trained on ImageNet and fine-tuned for this specific task.

The goal is to analyze vehicle images and correctly identify the brand (e.g., Audi, BMW, Mercedes) with high accuracy using a dataset of varying angles and lighting conditions.

---

## 📊 Experimental Results & Analysis

### 1. Training Performance (Accuracy & Loss)
The model was trained over multiple epochs. As seen in the graph below, the **VGG16 model** achieved faster convergence and higher validation accuracy compared to the custom CNN architecture.

![Training Graph](assets/training_graph.png)
*Figure 1: Training vs. Validation Accuracy/Loss metrics over epochs.*

### 2. Confusion Matrix
To understand the misclassifications, a Confusion Matrix was generated. It highlights which car brands were most frequently confused with each other (e.g., distinguishing between similar luxury sedans).

![Confusion Matrix](assets/confusion_matrix.png)
*Figure 2: Confusion Matrix showing true positives and class-wise performance.*

### 3. Real-world Prediction Example
The model was tested on unseen data to evaluate its generalization capability. Below is an example of the model correctly identifying a vehicle brand with high confidence:

![Prediction Result](assets/prediction_result.png)
*Figure 3: Model prediction output on a test image.*

---

## 🛠️ Technical Architecture

### Data Processing
* **Augmentation:** Utilized `ImageDataGenerator` for rescaling, rotation, shear, and zoom to prevent overfitting and improve robustness.
* **Normalization:** Pixel values normalized to the [0, 1] range for optimal neural network performance.
* **Dataset Split:** Data rigorously divided into Training, Validation, and Test sets.

### Model Comparison
| Feature | Custom CNN | VGG16 (Transfer Learning) |
| :--- | :--- | :--- |
| **Architecture** | 3 Convolutional Blocks + MaxPool | 16 Deep Layers (Fixed Feature Extractor) |
| **Trainable Params** | Low (~1M parameters) | Medium (Only Dense Layers trained) |
| **Performance** | Good for simple features | **Superior** for complex patterns |

---

## 📂 Repository Structure
```text
├── assets/                 # Screenshots, graphs, and visual results
├── reports/                # Project Documentation and Final PDF Report
├── CPproject.ipynb         # Main Jupyter Notebook (Training, Evaluation, Plots)
└── README.md               # Project documentation
