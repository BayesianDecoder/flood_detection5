# 🌊 Flood Detection from Satellite Images

## 🛰️ Overview
This project leverages **deep learning** techniques to **detect flood-prone areas from satellite imagery**.  
Using the **VGG16 Convolutional Neural Network (CNN)** pre-trained on ImageNet, the model has been **fine-tuned** to identify water-covered regions with high accuracy.  
It aims to support disaster management systems by automating early flood detection through remote sensing data.

---

## ✨ Features
- **Pre-trained VGG16 CNN** – Utilizes VGG16 layers for rich feature extraction from satellite images.  
- **Fine-Tuning** – Refines deeper layers of the model for flood-specific feature learning.  
- **Global Average Pooling** – Reduces dimensionality while retaining key spatial information.  
- **Binary Classification** – Predicts whether a given satellite image segment contains flooded regions or not.  

---

## 🧩 Model Architecture
| Component | Description |
|------------|-------------|
| **Base Model (VGG16)** | Used without the top (fully connected) layers to act as a deep feature extractor. |
| **Global Average Pooling** | Condenses feature maps to a 512-length vector per image. |
| **Dense Output Layer** | Single neuron with sigmoid activation for binary flood classification. |

---

## ⚙️ Fine-Tuning Details
1. **Initial Training** – The top layers are trained with a base learning rate of **0.0001**.  
2. **Unfreezing Layers** – Layers from the **15th onwards** are unfrozen to allow deeper feature adaptation.  
3. **Reduced Learning Rate** – During fine-tuning, the learning rate is reduced by **75×** to prevent overfitting and make controlled weight updates.

---

## 📊 Results
| Metric | Score |
|---------|--------|
| **Validation Accuracy** | 🟢 **98.06%** |
| **Test Accuracy** | 🟢 **97.29%** |

These results demonstrate strong generalization and reliability in identifying flood-affected areas from unseen satellite images.

---

## 🧰 Tech Stack
| Category | Tool / Library |
|-----------|----------------|
| Framework | TensorFlow / Keras |
| Model | VGG16 (pre-trained on ImageNet) |
| Language | Python |
| Data Type | Satellite Imagery |
| Evaluation | Accuracy, Validation & Test Metrics |

---

