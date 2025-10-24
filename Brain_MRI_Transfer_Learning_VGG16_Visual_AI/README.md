# 🧠 Brain MRI Tumor Classifier (Transfer Learning with VGG16)

This project develops an image classifier to distinguish between **Pituitary Tumors** and **No Tumor** MRI scans. The primary objective was to demonstrate and leverage **Transfer Learning** using the pre-trained **VGG16** architecture to achieve high classification accuracy efficiently.

---

## 🚀 Key Results & Impact

The model successfully reduced overfitting and significantly increased validation accuracy by implementing Transfer Learning.

| Model | Training Epochs | Training Accuracy | Validation Accuracy | Key Finding |
| :--- | :--- | :--- | :--- | :--- |
| **Custom CNN (Baseline)** | 10 epochs | ~95% | ~72% | **Overfit** (Poor generalization) |
| **VGG16 Transfer Learning (Final)** | 5 epochs | ~98% | **~91%** | **Converged Faster** and achieved superior generalization |

### Key Project Objectives Achieved:
* **Performance Improvement:** Achieved a substantial increase in validation accuracy (from $\sim 72\%$ to $\sim 91\%$).
* **Efficiency:** The Transfer Learning model converged faster than the custom CNN model, achieving high accuracy in only **5 epochs**.
* **Technique:** Successfully leveraged the pre-trained **VGG16** architecture by freezing its convolutional base and training only new fully-connected layers for binary classification.

---

## ⚙️ Technical Details & Methodology

* **Task:** Binary image classification (Pituitary Tumor vs. No Tumor).
* **Architecture:** VGG16 Convolutional Base + Custom Fully-Connected Layers.
* **Data Augmentation:** Used techniques including horizontal flip, rotation ($\le 20^\circ$), and height/width shifts on the training data to prevent overfitting.
* **Regularization:** The custom CNN used **Batch Normalization** and **Dropout** layers.

***

## 📁 Project Assets

* **Code Report (PDF):** [View Code Comments and Steps](Brain_MRI_VGG16_Code_Comments_EK.pdf)
