# 🧼 Image Denoising using Convolutional Autoencoder (MNIST)

A Deep Learning project that demonstrates image denoising on the MNIST handwritten digit dataset using a **Convolutional Autoencoder** implemented in TensorFlow/Keras.

---

## 📌 Project Overview

Image denoising is the process of removing unwanted noise from a degraded image while preserving important visual details and structures. In this project, a synthetic Gaussian noise factor is added to the clean MNIST images, and an Autoencoder network is trained to reconstruct the original, clean images from the noisy inputs.

### 🏗️ Architecture Summary

1. **Encoder:**
   - Input Layer: `(28, 28, 1)`
   - `Conv2D` (32 filters, 3x3 kernel, ReLU, strides=2) $\rightarrow$ Output: `(14, 14, 32)`
   - `Conv2D` (16 filters, 3x3 kernel, ReLU, strides=2) $\rightarrow$ Output: `(7, 7, 16)` *(Bottleneck)*
2. **Decoder:**
   - `Conv2DTranspose` (16 filters, 3x3 kernel, ReLU, strides=2) $\rightarrow$ Output: `(14, 14, 16)`
   - `Conv2DTranspose` (32 filters, 3x3 kernel, ReLU, strides=2) $\rightarrow$ Output: `(28, 28, 32)`
   - `Conv2D` (1 filter, 3x3 kernel, Sigmoid) $\rightarrow$ Final Output: `(28, 28, 1)`

---

## 🛠️ Requirements & Tech Stack

* **Python 3.x**
* **TensorFlow / Keras**
* **NumPy**
* **Matplotlib**

To install all required packages:
```bash
pip install tensorflow numpy matplotlib
