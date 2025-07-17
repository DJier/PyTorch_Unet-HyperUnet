# HyperUnet
# 🧠 Liver Segmentation with U-Net 🩺 using TensorFlow & Medical Imaging

![TensorFlow](https://img.shields.io/badge/Framework-TensorFlow-orange?logo=tensorflow)
![Dataset](https://img.shields.io/badge/Dataset-LiTS-blue)
![Model](https://img.shields.io/badge/Model-U--Net-green)
![Status](https://img.shields.io/badge/Status-Training%20Complete-success)

---

## 📝 Overview

This project implements a **U-Net-based deep learning model** for **semantic segmentation of liver tissues** from medical CT scan slices. Using the **LiTS (Liver Tumor Segmentation)** dataset, we preprocess, visualize, and train the model to distinguish liver structures using grayscale mask annotations.

---

## 🧪 Tech Stack

| Category         | Tech Used |
|------------------|-----------|
| Language         | Python 3.x |
| Deep Learning    | TensorFlow, Keras |
| Image Processing | OpenCV, scikit-image |
| Visualization    | Matplotlib, Seaborn |
| Dataset Handling | Pandas, NumPy |
| Dataset Source   | [LiTS 256x256 (KaggleHub)](https://www.kaggle.com/datasets/harshwardhanbhangale/lits-dataset-256x256-imgs) |

---

## 📊 Dataset Summary

- ✅ Total images: 49,842
- 🖤 Black masks (empty): ~34,097
- 🩻 Masks with liver annotations: ~15,745
- 🔄 Selected annotated masks: 15,000
- 🔀 Dataset split:  
  - **Training**: 12,000  
  - **Validation**: 1,500  
  - **Testing**: 1,500  

---

## 🧠 Model Architecture

This project uses a **custom U-Net** architecture with:
- 4-level encoder-decoder
- Batch normalization
- ReLU activations
- Skip connections for better gradient flow
- Sigmoid output for binary segmentation

---

## 🧮 Evaluation Metrics

- 🎯 **Dice Coefficient**
- 📐 **Jaccard Index (IoU)**
- 🧪 **Precision / Sensitivity**
- ⚠️ **HD95 (Hausdorff Distance)**

---

## 🔍 Key Features

- ⚙️ Grayscale mask filtering and analysis
- 📊 Mask type distribution plots
- 🧼 Clean mask loading with augmentation-ready generators
- 🔍 Image-mask matching & integrity checking
- 🧠 Custom loss functions including Dice Loss & Jaccard Loss
- 🖼️ Real-time visualization of the masks

---

## 🧰 How to Run

```bash
# Clone the repository
git clone https://github.com/DJier/LiverSegmentation-U-Net-TensorFlow.git
cd LiverSegmentation-U-Net-TensorFlow

# Install dependencies
pip install -r requirements.txt

# Train the model
python train.py
