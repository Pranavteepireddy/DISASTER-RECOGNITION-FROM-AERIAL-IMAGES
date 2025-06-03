# DISASTER-RECOGNITION-FROM-AERIAL-IMAGES

This project focuses on classifying aerial images into disaster categories using deep learning. We built and evaluated multiple CNN architectures, ultimately fine-tuning MobileNetV2 to achieve high accuracy and real-time inference capabilities. The model is designed for deployment on UAVs to support disaster monitoring and emergency response.

---

## Project Overview

- **Goal**: Accurately classify aerial images into five categories:  
  `Fire`, `Flooded Areas`, `Collapsed Buildings`, `Traffic Incidents`, and `Normal`.
- **Dataset**: [AIDER Dataset](https://zenodo.org/records/3888300#.XvCPQUUzaUk) – an annotated dataset of disaster imagery taken from drones.
- **Best Model**: Fine-tuned MobileNetV2 with >94% test accuracy.

---

## Model Architectures Explored

| Model           | Test Accuracy | Macro F1-Score |
|----------------|---------------|----------------|
| Custom CNN     | 85.6%         | 0.79           |
| ResNet50       | 67.7%         | 0.59           |
| EfficientNetB0 | 67.9%         | 0.55           |
| **MobileNetV2**| **94.6%**     | **0.91**       |

---

## Key Features

- **Transfer Learning**: Used MobileNetV2 pretrained on ImageNet, fine-tuned for aerial disaster classification.
- **Data Augmentation**: Rotation, zoom, brightness jitter, and flipping to reduce overfitting.
- **Class Imbalance Handling**: Weighted loss functions to balance under-represented classes.
- **Training Strategy**:
  - Phase 1: Train top layers with frozen base
  - Phase 2: Unfreeze upper layers and fine-tune with lower learning rate
- **Evaluation**: Confusion matrix, classification report (Precision, Recall, F1), and per-class performance metrics.

---

## Results (MobileNetV2)

- **Test Accuracy**: 94.6%
- **Test Loss**: 0.1664
- **Macro F1-Score**: 0.91
- **Weighted F1-Score**: 0.95

---

