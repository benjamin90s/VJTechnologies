# VJTechnologies
# COCO Subset Segmentation: Dataset Prep & U-Net Training

This repository contains a full pipeline for semantic segmentation on a COCO 2017 subset, covering:

- **Task 1** – Dataset preparation & multi-class mask generation  
- **Task 2** – Training a U-Net model using PyTorch

---

## Contents

- `VJT.ipynb`  
  - Downloads & extracts COCO 2017 images and annotations  
  - Creates a class-balanced subset for person, bicycle, and car  
  - Generates multi-class RGBA masks with fixed color codes  
  - Trains a U-Net model using masked focal loss  
  - Evaluates segmentation performance (IoU, F1, accuracy)  
  - Visualizes predictions vs. ground truth

---

## Training Metrics

Training and validation losses were monitored using TensorBoard.

- Screenshots of the TensorBoard scalar plots are provided.
- The raw scalar data exported from TensorBoard is also available as `train_loss.csv` & `val_loss.csv` file.


## Tested Environment

-Python: 3.8.10
-matplotlib: 3.7.5
-numpy: 1.24.3
-Pillow: 10.4.0
-requests: 2.32.3
-torch: 2.4.0+cu121
-torchvision: 0.19.1+cu121
-tqdm: 4.66.5
-pycocotools: 2.0

## Reproducibility (UV Setup)

Although the project was developed in an environment where required packages were pre-installed, the `pyproject.toml` is provided to comply with the assignment's `uv` dependency management requirement.

⚠️ Note on Reproducibility:
This project uses random sampling for dataset creation and visualization. While the overall behavior and performance will remain consistent, exact metrics (IoU, F1) and visual samples may vary slightly across runs unless a random seed is fixed.


