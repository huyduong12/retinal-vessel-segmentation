# Retinal Vessel Segmentation with Dual-Decoder Attention 👁️💉

An advanced Computer Vision pipeline for the precise segmentation of retinal vessels from fundus imagery. This project implements a **Dual-Decoder Attention** model to capture both fine vessel structures and global vascular morphology.

## 🌟 Overview
Vessel segmentation is a prerequisite for diagnosing diabetic retinopathy and other systemic diseases. This model uses specialized attention mechanisms to focus on low-contrast capillary networks that traditional U-Nets often miss.

## 🚀 Key Features
- **Dual-Decoder Architecture:** Separately optimizes for fine-grained vessel edges and major vascular trunks.
- **Attention Gates:** Dynamically weights spatial features to suppress background noise.
- **DICE Loss Optimization:** Handles extreme class imbalance between vessel and non-vessel pixels.
- **Support for DRIVE/STARE Datasets:** Standardized evaluation scripts for academic benchmarking.

## 🏗️ Architecture
- **Encoder:** Modified ResNet-34.
- **Decoders:** Parallel branches with feature fusion.
- **Loss:** Weighted Cross-Entropy + Soft DICE.

## 🛠️ Usage
```bash
pip install -r requirements.txt
python segment.py --input eye_fundus.jpg --output mask.png
```