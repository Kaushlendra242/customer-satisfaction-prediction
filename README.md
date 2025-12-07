**🎯 Customer Satisfaction Prediction System**

***Classification • NLP • Regression • Segmentation • Explainability (SHAP) • Deployment-Ready***

**🌟 Overview**

This project builds a complete **Machine Learning system for customer support analytics,** including:

***✅ Customer Satisfaction Prediction***
***✅ Resolution Time Regression***
***✅ Ticket Description NLP***
***✅ Customer Segmentation***
***✅ SHAP Explainability***
***✅ Streamlit + FastAPI Deployment- Pending***

A fully production-ready workflow for real customer support analytics.

**📦 Project Architecture**


📂 customer-satisfaction-project/
|                                
|── notebooks/                   
|   └── final_customer_satisfaction.ipynb
|                                        
├── model_artifacts/                     
│   ├── svm_model.joblib                 
│   ├── rf_regressor.joblib              
│   ├── tfidf.joblib                     
│   ├── scaler.joblib                              
│   └── encoders.joblib                            
│                                                  
|── requirements.txt                                
|─ README.md                                              |



**🚀 Final Model Performance**

**🟦 1️⃣ Classification Models**
| 🧠 Model                | 🎯 Accuracy | 🔵 Macro F1 | ⭐ Notes                  |
| ----------------------- | ----------- | ----------- | ------------------------ |
| RandomForest (weighted) | 0.7999      | 0.6123      | Good baseline            |
| XGBoost (default)       | 0.7946      | 0.5989      | Used for SHAP            |
| **SVM (balanced)**      | **0.8093**  | **0.6326**  | ⭐ **Best Overall Model** |


**✔ Why SVM is Best?**

- Strong performance on TF-IDF high-dimensional text

- Best Macro F1 (handles imbalanced classes well)

- Strong generalization

Strong generalization on sparse TF-IDF features

**🟩 2️⃣ Regression — Resolution Time (hrs)**

| Metric   | Score     |
| -------- | --------- |
| **MAE**  | **7.85**  |
| **MSE**  | **93.30** |
| **RMSE** | **9.66**  |

**✔ Notes**

- **📌 Model:** RandomForest Regressor
- **📌 Interpretation:** Typical prediction error ≈ 8–10 hours, good for SLA dashboards.

**🟨 3️⃣ Explainability —** SHAP (XGBoost Surrogate)

**Top Drivers of Satisfaction:**

- 🔥 Response Delay
- 🔥 Ticket Priority
- 🔥 Ticket Type
- 🔥 Description Length
- 🔥 Customer Age
- 🔥 Ticket Channel
- 🔥 TF-IDF keyword patterns

**Why XGBoost for SHAP?**

SVM doesn’t support SHAP → trained an XGBoost surrogate for transparent explanations.

**🟪 4️⃣ Customer Segmentation — KMeans (k=4)**

| Cluster                   | Interpretation                     |
| ------------------------- | ---------------------------------- |
| **0 – High Effort Cases** | Long resolution, long descriptions |
| **1 – Smooth Cases**      | High satisfaction, quick handling  |
| **2 – Priority Tickets**  | Escalated or urgent                |
| **3 – Low Complexity**    | Simple, short queries              |


---
**🧬 Data Features Used**
**🟦 Categorical**
- Customer Gender,
  
- Product Purchased,
  
- Ticket Type,
   
- Ticket Status,
  
- Ticket Priority,
   
- Ticket Channel,  

**🟩 Numeric**
- Customer Age,
  
- Customer Satisfaction Rating,
   
- Response Delay (hrs),
   
- Word Count,
   
- Description Length,  

**🟧 NLP**

* TF-IDF (top 5000 features)

* Ticket Description preprocessing

  ---

**🔧 Tech Stack**

| **Category**       |    	  **Tools**                    |
|--------------------|-------------------------------------|
| **ML Algorithms**  | 	SVM, RandomForest, XGBoost, KMeans |
| **NLP**            |	TF-IDF, text cleaning              |
| **Explainability** |	SHAP TreeExplainer                 |
|**Packaging**     	 |  Joblib models                      |
| **Visualization**  |  Matplotlib, Seaborn                |


**🖥 Run the Project Locally**

**1️⃣ Clone the Repository**
git clone https://github.com/yourusername/customer-satisfaction-prediction.git
cd customer-satisfaction-prediction

**2️⃣ Install Dependencies**
pip install -r requirements.txt

**3️⃣ Will Run the Streamlit Web App**
streamlit run app/streamlit_app.py



**📘 Deployment Ready**

The following artifacts are included and ready to deploy:

✔ svm_model.joblib – Final classification model

✔ xgb_shap_model.joblib – Explainability model

✔ rf_regressor.joblib – Regression model

✔ Preprocessing pipeline (scaler, tfidf)


**🧩 Future Enhancements**

🔹 Integrate BERT sentence embeddings

🔹 Advanced hyperparameter tuning (Optuna)

🔹 Add SLA Violations prediction

🔹 Full Docker + CI/CD pipeline

🔹 Model monitoring dashboard (Grafana + Prometheus)

**👨‍💻 Author & Maintainer**

**Kaushlendra Pratap Singh**
Email: Kaushlendra242@gmail.com

GitHub: https://github.com/Kaushlendra242
