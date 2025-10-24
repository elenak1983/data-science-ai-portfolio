# 🛂 Visa Approval Prediction (Stacking Ensemble ML & F1 Score Optimization)

This project develops a predictive classification model for EasyVisa to streamline the visa approval process. The goal was to build a robust model to predict visa outcomes by analyzing attributes of both the employee and employer, with a focus on mitigating critical errors.

---

## 🚀 Key Results & Impact

The project prioritized the **F1 Score** to ensure a balance between minimizing False Negatives (denying a deserving applicant) and False Positives (certifying an undeserving applicant).

| Final Model | Base Estimators | Testing Accuracy | Testing F1 Score | Key Finding |
| :--- | :--- | :--- | :--- | :--- |
| **Stacking Classifier** | AdaBoost, Gradient Boosting, Random Forest | **74.80%** | **82.06%** | The ensemble approach provides a boost in predictive performance. |
| **Tuned XGBoost** | N/A | 74.52% | 82.17% | The strongest individual performer, showing robust performance after tuning. |

### 💡 Key Insights for Decision-Making:
* **High-Impact Features:** The most influential factors include the employee's **education level**, **job experience**, and the **type of wage unit**.
* **Education:** Higher education levels (Bachelor's and Master's) showed a higher proportion of case certifications.
* **Wages:** Higher prevailing wages increase the likelihood of visa certification.
* **Imbalance:** The raw data showed a class imbalance, with "Certified" cases more than double the number of "Denied" cases (17,018 vs. 8,462).

---

## 🛠️ Technical Details & Methodology

* **Objective Metric:** **F1 Score** was the evaluation criterion, aiming to minimize False Negatives and False Positives.
* **Approach:** Rigorous model comparison, optimization (using hyperparameter tuning), and evaluation across various ensemble algorithms.
* **Stacking Architecture:** The final **Stacking Classifier** combines multiple base estimators (AdaBoost, Gradient Boosting, and Random Forest) with the highly-tuned **XGBoost Classifier** serving as the final estimator.
* **Preprocessing:** Included handling missing values, encoding categorical variables, and scaling numerical features.

***

## 📁 Project Assets

* **Executive Report (PDF):** [View Full Report](EasyVisa_Ensemble_Report_EK.pdf)
* **Code Notebook (iPython):** [View Code](EasyVisa_Ensemble_Code_EK.ipynb)

***

## ✅ Recommendations

* **Resource Allocation:** Allocate resources to factors contributing most significantly to the model's predictions, such as focusing on high-impact features like education and job experience.
* **Model Deployment:** Deploy the robust Stacking Classifier and implement continuous monitoring to quickly adapt to changes in the model's predictive power.
