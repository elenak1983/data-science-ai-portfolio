# ⚡ Predictive Maintenance for Wind Turbines (XGBoost Optimization)

This project develops an advanced **Machine Learning (ML)** solution for ReneWind to predict component failures in wind turbines *before* they occur. This predictive maintenance approach is vital for minimizing costly downtime and maximizing renewable energy output.

## 🎯 Executive Summary & Impact

The core business objective was to ensure the model catches the maximum number of true failures, meaning the project prioritized maximizing the **Recall** metric to minimize false negatives.

| Model | Class Balancing | Test Accuracy | Test Recall |
| :--- | :--- | :--- | :--- |
| **XGBoost Classifier (Final)** | SMOTE Oversampled | **97.9%** | **85.5%** |

### Key Achievements:
* **Optimal Model:** **XGBoost** was selected as the final model as it consistently achieved the highest Recall scores during cross-validation and validation sets.
* **Imbalance Resolution:** Used the **SMOTE** (Synthetic Minority Over-sampling Technique) to successfully balance the highly skewed dataset, which initially had only 5.6% failure instances.
* **Production Readiness:** The final XGBoost model was encapsulated in a Scikit-learn **Pipeline** for production deployment and consistent application on new sensor data.

***

## ⚙️ Technical Details & Methodology

### Data Handling
* The project optimized for the **Recall** score, which aligns with the business objective of reducing false negatives (missed failures).
* The raw dataset had a high imbalance, with a vast majority of observations categorized as '0' (non-failure).
* Missing values in features V1 and V2 were imputed using the median with `SimpleImputer`.
* The training data was split into train (75%) and validation (25%) sets.

### Model Tuning
* Model comparison and hyperparameter tuning were performed using **Randomized SearchCV** across ensemble methods, including Random Forest, Gradient Boosting, AdaBoost, and XGBoost.
* The final XGBoost model achieved a training accuracy of 99.9% and near-perfect recall and precision on the oversampled training data.

### Feature Insights
* The feature importance analysis showed that **V36** was the **most important factor** used by the model for prediction, while V8 was the least important.

***

## 📁 Project Assets

* **Executive Presentation (PDF):** [View Full Report](ReneWind_model_tuning.pdf)
* **Code Notebook (iPython):** [View Code](ReneWind_Code.ipynb) *(Adjust the code file name/extension as necessary)*

***

## ✅ Actionable Insights & Recommendations

* **Feature Focus:** Utilize the feature importances to prioritize continuous monitoring of the most influential factor, **V36**.
* **Strategy Refinement:** Continuously monitor the effectiveness of the SMOTE oversampling strategy and consider experimenting with different oversampling techniques.
* **Model Maintenance:** Regularly monitor the model's performance and retrain it as needed with new data to ensure its effectiveness over time.
