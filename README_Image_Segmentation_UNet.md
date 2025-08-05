# 🧠 Image Segmentation Using U-Net with Transfer Learning

This project applies deep learning for semantic image segmentation using a U-Net architecture enhanced by **transfer learning**. The objective is to classify each pixel of an image and generate a segmentation map identifying target regions.

> 🔧 Built using PyTorch  
> 🎯 Trained on a dataset with paired images and binary masks  
> 📉 Final Validation IoU Score: ~0.54

---

## 📁 Project Structure

```
image-segmentation/
├── gunjan_priyanka29_gmail_com_31_UNET11.ipynb   # Main notebook
├── README.md
├── requirements.txt                              # Python dependencies
└── (data/, scripts/, etc. can be added as needed)
```

---

## 📌 Problem Statement

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

## ⚙️ Training Details

- **Loss Function**: Binary Cross Entropy with Logits (`BCEWithLogitsLoss`)
- **Optimizer**: Adam
- **Metric**: Intersection over Union (IoU)
- **Train/Val Split**: 80:20
- **Validation IoU Score**: ~0.54

---

## 📈 Results

Below are example outputs on the test set:

| Input Image | Ground Truth Mask | Predicted Mask |
|-------------|-------------------|----------------|
| ![sample1](link) | ![mask1](link) | ![pred1](link) |
| _(Add images if available, or remove this table)_ |

Visual inspection shows the model performs reasonably well in identifying the key regions.

---

## 📦 Requirements

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

---

## 🚀 Future Improvements

- Add Dice coefficient and pixel accuracy evaluation
- Use data augmentation to improve generalization
- Deploy with a Streamlit or Gradio app for interactive demos

---

## 👩‍💻 Author

- Priyanka Gunjan  
  [GitHub](https://github.com/priyanka1901)
