# 🧠 Image Segmentation Using U-Net with Transfer Learning

This project applies deep learning for semantic image segmentation using a U-Net architecture enhanced by **transfer learning**. The objective is to classify each pixel of an image and generate a segmentation map identifying target regions.

> Built using PyTorch  
> Trained on a dataset with paired images and binary masks  
> Final Validation IoU Score: ~0.54


---

## Problem Statement

Given input images and corresponding binary masks, the goal is to segment the object of interest by classifying each pixel in the image.

---

## 📊 Dataset

- Each sample consists of an image and a corresponding binary segmentation mask.
- The dataset was split into:
  - **80%** training
  - **20%** testing
- Note: Due to file size, the dataset is not included in the repo.

---

## 🧠 Model Architecture

This project uses a **U-Net model with transfer learning**:
- The **encoder** is based on a **pretrained convolutional neural network** (e.g., VGG or ResNet).
- The **decoder** path is custom and trained from scratch to produce segmentation maps.
- This architecture benefits from feature richness of pretrained networks and is well-suited for tasks with limited labeled data.

---

## Training Details

- **Loss Function**: Combined Cross Entropy and Dice Loss (`cce_dice_loss`)
- **Optimizer**: Adam
- **Metric**: Intersection over Union (IoU)
- **Train/Val Split**: 80:20
- **Validation IoU Score**: ~0.54

---

## Requirements

Install Python dependencies:
```bash
pip install -r requirements.txt
```

Main libraries:
- `torch`
- `torchvision`
- `numpy`
- `matplotlib`
- `PIL`
- `segmentation_models` (Keras version)
- `tensorflow`

---

## Future Improvements

- Use data augmentation to improve generalization
- Deploy with a Streamlit or Gradio app for interactive demos

---
