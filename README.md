# VJTechnologies
# 🔍 COCO Subset Segmentation: Dataset Prep & U-Net Training

This repository contains a full pipeline for semantic segmentation on a COCO 2017 subset, covering:

- **Task 1** – Dataset preparation & multi-class mask generation  
- **Task 2** – Training a U-Net model using PyTorch

---

## 📦 Contents

- `VJT.ipynb`  
  - Downloads & extracts COCO 2017 images and annotations  
  - Creates a class-balanced subset for person, bicycle, and car  
  - Generates multi-class RGBA masks with fixed color codes  
  - Trains a U-Net model using masked focal loss  
  - Evaluates segmentation performance (IoU, F1, accuracy)  
  - Visualizes predictions vs. ground truth

---

## Requirements

- Python 3.8.10



