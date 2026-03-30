# Foundational CNN Architectures: AlexNet & VGG-16

This repository contains implementations and experimental logs for two of the most influential architectures in the history of Computer Vision: **AlexNet (2012)** and **VGG-16 (2014)**. 

The goal of this project is to explore the evolution of Convolutional Neural Networks (CNNs), moving from the irregular, pioneering design of AlexNet to the deep, uniform simplicity of VGGNet.

---

## 🏛️ Architecture Overviews

### 1. AlexNet (The Pioneer)
Introduced by Alex Krizhevsky et al. in 2012, this model won the ImageNet LSVRC-2012 competition by a massive margin, effectively starting the "Deep Learning Revolution."

**Key Innovations:**
* **ReLU Activation:** Replaced Sigmoid/Tanh, reducing training time by nearly $6\times$.
* **Dropout:** A regularization technique to prevent overfitting by randomly "dropping" neurons during training.
* **Overlapping Max Pooling:** Reduced the error rate by $0.4\%$ and $0.3\%$ respectively compared to non-overlapping pooling.
* **Large Filters:** Utilized large $11 \times 11$ and $5 \times 5$ convolutional kernels in the early layers.

### 2. VGG-16 (The Standard)
Developed by the Visual Geometry Group at Oxford in 2014, VGG-16 shifted the focus toward **network depth**. It proved that stacking multiple small filters is superior to using single large filters.

**Key Innovations:**
* **Uniformity:** Uses a consistent architecture of $3 \times 3$ convolutions with a stride of $1$ and $2 \times 2$ max-pooling with a stride of $2$.
* **Effective Receptive Field:** Proved that a stack of three $3 \times 3$ layers has the same effective receptive field as a single $7 \times 7$ layer, but with more non-linearity and fewer parameters.
* **Depth:** Demonstrated that increasing depth to 16–19 layers significantly improves feature extraction.

---

## 📊 Technical Comparison

| Feature | AlexNet (2012) | VGG-16 (2014) |
| :--- | :--- | :--- |
| **Total Layers** | 8 (5 Conv, 3 FC) | 16 (13 Conv, 3 FC) |
| **Filter Sizes** | $11 \times 11, 5 \times 5, 3 \times 3$ | Strictly $3 \times 3$ |
| **Parameters** | ~60 Million | ~138 Million |
| **Input Size** | $227 \times 227 \times 3$ | $224 \times 224 \times 3$ |
| **Normalization** | Local Response Normalization (LRN) | No LRN (Found to be ineffective) |

---
