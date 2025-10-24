# 🛂 Visa Approval Prediction (Stacking Ensemble ML & F1 Score Optimization)

[cite_start]This project develops a predictive classification model for EasyVisa to streamline the visa approval process[cite: 32]. [cite_start]The goal was to build a robust model to predict visa outcomes by analyzing attributes of both the employee and employer, with a focus on mitigating critical errors[cite: 34, 30].

---

## 🚀 Key Results & Impact

[cite_start]The project prioritized the **F1 Score** to ensure a balance between minimizing False Negatives (denying a deserving applicant) and False Positives (certifying an undeserving applicant)[cite: 606].

| Final Model | Base Estimators | Testing Accuracy | Testing F1 Score | Key Finding |
| :--- | :--- | :--- | :--- | :--- |
| **Stacking Classifier** | AdaBoost, Gradient Boosting, Random Forest | [cite_start]**74.80%** [cite: 540] | [cite_start]**82.06%** [cite: 540] | [cite_start]The ensemble approach provides a boost in predictive performance[cite: 1219]. |
| **Tuned XGBoost** | N/A | [cite_start]74.52% [cite: 540] | [cite_start]82.17% [cite: 540] | [cite_start]The strongest individual performer, showing robust performance after tuning[cite: 557]. |

### 💡 Key Insights for Decision-Making:
* [cite_start]**High-Impact Features:** The most influential factors include the employee's **education level**, **job experience**, and the **type of wage unit**[cite: 16].
* [cite_start]**Education:** Higher education levels (Bachelor's and Master's) showed a higher proportion of case certifications[cite: 98].
* [cite_start]**Wages:** Higher prevailing wages increase the likelihood of visa certification[cite: 408].
* [cite_start]**Imbalance:** The raw data showed a class imbalance, with "Certified" cases more than double the number of "Denied" cases (17,018 vs. 8,462)[cite: 221, 222].

---

## 🛠️ Technical Details & Methodology

* [cite_start]**Objective Metric:** **F1 Score** was the evaluation criterion, aiming to minimize False Negatives and False Positives[cite: 606].
* [cite_start]**Approach:** Rigorous model comparison, optimization (using hyperparameter tuning), and evaluation across various ensemble algorithms[cite: 13].
* [cite_start]**Stacking Architecture:** The final **Stacking Classifier** combines multiple base estimators (AdaBoost, Gradient Boosting, and Random Forest) with the highly-tuned **XGBoost Classifier** serving as the final estimator[cite: 1164, 1165].
* [cite_start]**Preprocessing:** Included handling missing values, encoding categorical variables, and scaling numerical features[cite: 37, 38].

***

## 📁 Project Assets

* **Executive Report (PDF):** [View Full Report](EasyVisa_Ensemble_Report_EK.pdf)
* **Code Notebook (iPython):** [View Code](EasyVisa_Ensemble_Code_EK.ipynb)

***

## ✅ Recommendations

* [cite_start]**Resource Allocation:** Allocate resources to factors contributing most significantly to the model's predictions, such as focusing on high-impact features like education and job experience[cite: 20].
* [cite_start]**Model Deployment:** Deploy the robust Stacking Classifier and implement continuous monitoring to quickly adapt to changes in the model's predictive power[cite: 22].
