# 🧠 Pneumonia Chest X-Ray Classification (Multiclass - CNN)

This project is focused on building a custom **Convolutional Neural Network (CNN)** to classify chest X-ray images into three categories:

- **Normal**
- **Bacterial Pneumonia**
- **Viral Pneumonia**

---

## Dataset

The dataset consists of chest X-ray images organized into three classes. It has been split into three subsets:

- **Training**
- **Validation**
- **Testing**

Each subset contains three folders: `NORMAL`, `BACTERIAL`, `VIRAL`.

> Note: For privacy and size constraints, the dataset is not included in this repository. You may refer to the original source or upload your own dataset with the same folder structure.

---

## Project Structure

├── notebook/
│ └── Pneumonia_Classification_CNN.ipynb
├── models/
│ └── cnn_model_pneumonia.h5
├── results/
│ ├── accuracy_loss_plot.png
│ └── confusion_matrix.png
├── README.md
└── requirements.txt

---

## Methodology

### Preprocessing

- Resize all images to **224x224** pixels
- Normalize pixel values to **[0, 1]**
- Apply data augmentation:
  - Rotation
  - Zoom
  - Horizontal flip
- One-hot encode labels

### CNN Architecture

- 3 × Conv2D + MaxPooling
- Flatten → Dense (ReLU) → Dropout
- Output layer with 3 units and softmax activation

### Evaluation Metrics

- Accuracy
- Precision, Recall, F1-Score
- Confusion Matrix
