# MonoDepthNet — Monocular Depth Estimation with UNet

[![Python](https://img.shields.io/badge/Python-3.9-blue.svg)]()
[![PyTorch](https://img.shields.io/badge/Framework-PyTorch-red.svg)]()
[![Dataset](https://img.shields.io/badge/Dataset-NYU%20Depth%20V2-green.svg)]()
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)]()

## 📖 Overview
**MonoDepthNet** is a deep learning project focused on **monocular depth estimation** — predicting a depth map from a single RGB image.  
Developed as part of *CPSC 8810: Deep Learning for Computational Photography*, this project implements a **UNet-based convolutional neural network** trained on the **NYU Depth V2** dataset to achieve high-precision pixel-wise depth prediction.

> **Author:** Shrayas Raju  
> **CUID:** C10067703  
> **Framework:** PyTorch (CUDA accelerated)

---

## 📂 Dataset
**NYU Depth V2 Dataset**  
📦 [Dataset Link](https://www.kaggle.com/datasets/soumikrakshit/nyu-depth-v2)

- Indoor RGB-D dataset containing thousands of paired RGB and depth images  
- Training set: **45,000 samples**  
- Validation set: **5,000 samples**  
- Input size: **240×320** pixels  
- Each RGB image has a matching 16-bit PNG depth map  

---

## 🧠 Model Architecture

The architecture is a **Deep UNet (4 levels)** designed for dense depth prediction:

- **Encoder:** Four DoubleConv blocks with max pooling  
- **Bottleneck:** 1024-channel representation  
- **Decoder:** Transposed convolutions with skip connections  
- **Output Layer:** 1-channel depth prediction  

**Loss Function:** Scale-Invariant Loss  
**Optimizer:** AdamW  
**Scheduler:** ReduceLROnPlateau  
**Early Stopping:** Patience of 7 epochs  

---

## ⚙️ Training Configuration

| Parameter | Value |
|------------|--------|
| Epochs | 25 |
| Batch Size | 16 |
| Learning Rate | 1e-4 |
| Weight Decay | 1e-5 |
| Train/Val Split | 90% / 10% |
| Device | CUDA (if available) |

---

## 📊 Results

The model shows strong convergence and low validation loss, reaching **~0.0049** final validation loss.

| Metric | Train Loss | Validation Loss |
|---------|-------------|----------------|
| Initial | 3.8678 | 1.6602 |
| Final | 0.0036 | 0.0049 |

📈 *Training and validation loss curve shows steady convergence throughout training.*

---



