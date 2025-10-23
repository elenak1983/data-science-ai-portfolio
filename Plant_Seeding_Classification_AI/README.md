# 🌿 AI-Powered Plant Seedling Classification (Deep Learning CNN)

This project develops and refines a *Convolutional Neural Network (CNN)* for the automated classification of plant seedlings into 12 distinct species categories. [cite_start]This solution addresses the need for reducing manual labor and improving crop management efficiency in the agriculture industry[cite: 38, 41, 42].

---

## 🚀 Executive Summary & Key Results

| Metric | [cite_start]Initial Model [cite: 387] | [cite_start]Final (Improved) Model [cite: 387, 416] | Improvement |
| :--- | :--- | :--- | :--- |
| *Test Accuracy* | [cite_start]59% [cite: 1414] [cite_start]/ 68% [cite: 266] | [cite_start]*76.84%* [cite: 363, 404] | [cite_start]*Significant* (approx. 9-18%) [cite: 387] |
| Macro Avg. F1-Score | [cite_start]0.57 [cite: 387] | [cite_start]*0.73* [cite: 374, 387] | Major improvement in class-level performance. |

### 🎯 Key Improvements Implemented:
[cite_start]The significant performance increase was achieved by refining the model architecture and training strategy[cite: 395]:
1.  [cite_start]*Improved Architecture:* Added *Batch Normalization* and *Dropout* layers (rate 0.3) for enhanced robustness and reduced overfitting[cite: 277, 278, 403, 425].
2.  [cite_start]*Data Augmentation:* Applied techniques (like rotation) to increase training data variability, which helps the model generalize better and manage class imbalance[cite: 271, 391, 402].
3.  [cite_start]*Dynamic Learning Rate:* Utilized *ReduceLROnPlateau* to decrease the learning rate if validation accuracy plateaued, improving convergence[cite: 23, 269, 390, 401].

---

## 📁 Project Contents

This folder contains the complete technical assets for this project.

* [cite_start]*Code Notebook (Colab):* `EK_CV_Project_Low_Code_Notebook.ipynb` (or PDF export: [cite: 441])
* [cite_start]*Executive Presentation (PDF):* `EK_Plans_Project.pdf` (or original PPTX [cite: 1777])

### 🔍 Technical Details

* [cite_start]*Data Source:* Images of 12 plant species provided by Aarhus University Signal Processing group[cite: 464, 465, 49].
* [cite_start]*Preprocessing:* Images were converted from BGR to RGB, resized from $128 \times 128$ to *$64 \times 64$* pixels, and normalized by dividing by 255.0[cite: 52, 104, 793, 881].
* [cite_start]*Model Architecture Summary:* The final CNN used 3 sets of Convolutional layers (filters: 64 and 32), MaxPooling, and Batch Normalization, followed by a Flatten layer and Dense layers with a Softmax output for 12 classes [cite: 407, 408, 409, 1448-1462].

### 📉 Handling Class Imbalance
[cite_start]Initial Exploratory Data Analysis (EDA) showed significant class imbalance, with 'Common Chickweed' and 'Loose Silky-bent' having the highest counts (over 600) and classes like 'Shepherds Purse', 'Common Wheat', and 'Maize' having the fewest (below 250)[cite: 90, 92, 776, 775, 781]. [cite_start]This was primarily managed by implementing *data augmentation* and was noted as requiring *further data collection* as a recommendation[cite: 97, 20, 33].

---

## 📈 Actionable Insights and Recommendations

[cite_start]The solution offers an effective, automatable tool for classification[cite: 440]. [cite_start]Recommendations for future work include[cite: 28, 29, 30, 31, 32]:

* [cite_start]*Data Enhancement:* Increase the size and diversity of the dataset, especially for underrepresented classes like 'Black-grass' and 'Cleavers'[cite: 19, 33].
* [cite_start]*Advanced Architectures:* Explore transfer learning models (e.g., ResNet, Inception) to potentially capture more intricate patterns and improve accuracy[cite: 35].
* [cite_start]*Deployment:* Deploy and integrate the model into a real-world agricultural setting to automate the seedling classification process[cite: 32].

**

[cite_start]*Note to Reviewer:* Please see the embedded presentation (PDF) for a high-level, business-focused overview, and the notebook file for the complete, reproducible Python code and step-by-step model development[cite: 7].
