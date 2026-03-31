# 🧠 BioGraphNet: Graph Attention Networks for Explainable Histopathology Classification

🚀 A hybrid CNN-GNN framework for accurate and interpretable cancer classification using histopathology images.

---

## 📌 Overview

Histopathological image analysis is critical for cancer diagnosis, but traditional CNN-based approaches fail to capture long-range spatial dependencies across tissue regions.

This project introduces **BioGraphNet**, a novel hybrid architecture that:
- Extracts local features using CNNs
- Models global spatial relationships using Graph Neural Networks (GNNs)
- Provides interpretability using GNNExplainer and LIME

📄 *This work is currently under peer review at Springer.*

---

## 🧩 Key Features

- 🔬 **Hybrid CNN + GNN Architecture**
- 🧠 **Dynamic Graph Learning (learned edge connections)**
- 📊 **Graph Attention Networks (GATv2)**
- 🧱 **SAGPooling for hierarchical graph representation**
- 🔍 **Explainability via GNNExplainer & LIME**
- 📈 **State-of-the-art performance on LC25000 dataset**

---

## 🏗️ Architecture

1. **Preprocessing**
   - Resize & normalize histopathology images
   - Extract overlapping patches (224×224)

2. **Feature Extraction**
   - CNN backbone (ResNet50 / Custom ResBlocks)
   - Generate patch-level embeddings

3. **Graph Construction**
   - Nodes = image patches
   - Edges = spatial relationships (k-NN + dynamic learning)

4. **Graph Learning**
   - GATv2 layers for attention-based aggregation
   - SAGPooling for graph coarsening

5. **Classification**
   - Global pooling (mean + max)
   - Fully connected classifier

6. **Explainability**
   - GNNExplainer
   - LIME superpixel visualization

---

## 📊 Results

| Model        | Accuracy | F1 Score | AUC  |
|-------------|--------|---------|------|
| **BioGraphNet (Ours)** | **99.79%** | **0.995** | **0.953** |
| ResNet50    | 94.1%  | 0.932   | 0.914 |
| ViT-Small   | 95.2%  | 0.948   | 0.931 |

---

## 📁 Dataset

- **LC25000 Dataset**
  - Lung and Colon Histopathological Images
  - 5 classes: colon_aca, colon_n, lung_aca, lung_n, lung_scc

⚠️ *Ensure proper train-test split to avoid data leakage.*

---

## ⚙️ Tech Stack

- Python 🐍
- PyTorch 🔥
- PyTorch Geometric 🌐
- Torchvision
- NumPy, Matplotlib

---

## 🚀 Installation

Just Run the Python notebook on Colab or your workspace
