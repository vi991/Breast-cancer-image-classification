# Breast Cancer Classification Using MobileNetV2

## Project Overview

This project presents a deep learning approach for breast cancer classification from histopathological images using transfer learning. A pre-trained MobileNetV2 convolutional neural network was employed to distinguish between benign and malignant breast tissue samples.

The study investigates the impact of several regularization and generalization techniques, including Batch Normalization, Dropout, and Data Augmentation, on model performance.

---

## Objectives

* Develop an automated breast cancer image classification system.
* Apply transfer learning using MobileNetV2.
* Compare different model configurations.
* Evaluate the influence of regularization techniques on classification accuracy.
* Visualize and analyze model performance.

---

## Dataset

The dataset contains histopathological breast cancer images divided into two categories:

* **Benign**
* **Malignant**

Images were organized into training and testing subsets and resized to **224×224 pixels** before model training.

---

## Data Exploration

The following exploratory analysis was performed:

* Visualization of sample images from each class.
* Analysis of class distribution.
* Inspection of dataset balance.

Example outputs include:

* Sample image visualization
* Class distribution plots

---

## Data Preprocessing

Images were preprocessed using the MobileNetV2 preprocessing pipeline.

### Standard Preprocessing

* Image resizing (224×224)
* Pixel normalization using MobileNetV2 preprocessing

### Data Augmentation

To improve generalization, the following augmentation techniques were applied:

* Random rotations
* Width and height shifts
* Shearing
* Zooming
* Horizontal flipping

---

## Model Architecture

### Feature Extractor

* MobileNetV2 (pre-trained on ImageNet)
* Frozen convolutional base

### Classification Head

* GlobalAveragePooling2D
* Dense layer (128 neurons, ReLU activation)
* Optional Batch Normalization
* Optional Dropout (0.5)
* Output layer (Sigmoid activation)

---

## Experimental Setup

Four experiments were conducted:

| Model Configuration        | BatchNorm | Dropout | Augmentation |
| -------------------------- | --------- | ------- | ------------ |
| Baseline MobileNetV2       | No        | No      | No           |
| MobileNetV2 + BatchNorm    | Yes       | No      | No           |
| MobileNetV2 + Dropout      | No        | Yes     | No           |
| MobileNetV2 + Augmentation | No        | No      | Yes          |

Training settings:

* Optimizer: Adam
* Learning Rate: 0.0001
* Loss Function: Binary Cross-Entropy
* Early Stopping
* Maximum Epochs: 10

---

## Evaluation Metrics

Model performance was assessed using:

* Accuracy
* Precision
* Recall
* F1-Score
* Confusion Matrix

Training and validation curves were also analyzed to monitor convergence and overfitting.

---

## Results

The experiments demonstrate how different regularization techniques affect classification performance and model generalization.

Performance visualization includes:

* Accuracy curves
* Loss curves
* Confusion matrices
* Classification reports

---


## Future Improvements

* Fine-tuning MobileNetV2 layers
* Comparison with EfficientNet and ResNet architectures
* Cross-validation experiments
* Grad-CAM explainability analysis
* Hyperparameter optimization

---

## Author

Viktoriia Perevoznyk
