# 🏥 AI-Driven Clinical Triage System for Early Diabetes Detection
**Architect:** Afrizal | **Framework:** Nucleo Enterprise ML Framework (7-Phase Blueprint)

## 📌 Executive Summary
This project implements a high-precision **Smart Triage System** to address inefficiencies in large-scale diabetes screening. Leveraging the **BRFSS 2015** dataset (253,680 records), the system transforms raw clinical indicators into actionable risk scores, allowing healthcare providers to optimize laboratory resources and prioritize high-risk patients effectively.

## 📊 Business Impact & ROI (Return on Investment)
The system is calibrated to balance medical safety with operational cost-efficiency:
* **Clinical Goal:** Achieved a **Target Recall of 80%**, ensuring that 4 out of 5 diabetic patients are caught in the initial screening phase.
* **Cost Optimization:** Implementation of the **Nucleo AI Triage** reduces total estimated costs to **$5,146,250.00**.
* **Net Savings:** Provides a potential saving of **$6,327,500.00** compared to inefficient Universal Screening methods.
* **Risk Reduction:** Mitigates the $10.5M financial risk associated with untreated complications (No Screening scenario).

## ⚙️ Methodology: The Nucleo Framework
The project followed a rigorous 7-phase enterprise-grade pipeline:

1.  **Data Ingestion & Integrity**: Processed 253k+ records and removed **24,206 duplicates** (9.54%) to maintain data purity.
2.  **Exploratory Data Analysis (EDA)**: Analyzed clinical correlations, identifying that **General Health** and **High Blood Pressure** are primary risk drivers.
3.  **Statistical Validation**: Confirmed feature significance through **Mann-Whitney U** and **Chi-Square** tests ($p < 0.001$).
4.  **Advanced Feature Engineering**: Expanded the feature set from **21 to 26** by injecting domain knowledge (e.g., `Metabolic_Syndrome`, `CardioRisk`, `LifestyleScore`).
5.  **Tri-Force Ensemble Modeling**: Developed a robust soft-voting ensemble comprising **XGBoost**, **LightGBM**, and **CatBoost**.
6.  **Medical Calibration**: Achieved a **ROC-AUC of 0.8201** and a **PR-AUC of 0.4485**, ensuring strong separation power even in imbalanced classes (5.54:1 ratio).
7.  **Explainable AI (XAI)**: Utilized **SHAP** for global model transparency and **LIME** for localized, patient-specific diagnostic rationales.

## 🧠 Clinical Intelligence (XAI Insights)
The model's decision-making process is transparent and medically grounded:
* **Metabolic Syndrome**: Identified as the 2nd most powerful predictor, validating the re-engineering strategy.
* **Non-Linear Interactions**: SHAP analysis proves that obesity (High BMI) significantly worsens risk as patients age, a critical insight for geriatric care.

## 🧪 Real-World Validation Scenarios
The model was validated across complex mixed-scenario patient profiles:
* **Elite Senior (Age 75-79, Highly Fit)**: Predicted Risk: **14.98%** (Status: Healthy/Low Risk).
* **High-Stress Youth (Age 30-34, Poor Lifestyle)**: Predicted Risk: **33.19%** (Status: Healthy/Monitoring) .
* **Recovery Case (Post-Stroke, Obese)**: Predicted Risk: **82.60%** (Status: **DIABETES ALERT**) .

## 🛠️ Tech Stack
* **Languages:** Python
* **Models:** XGBoost, LightGBM, CatBoost
* **Tools:** Scikit-Learn, SHAP, LIME, Joblib 
* **Deployment:** Serialized artifacts (`.pkl`) ready for integration with AI Agents (CrewAI/LangGraph).

---
*Developed by Afrizal - Nucleo Techwise Indonesia*