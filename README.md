# Student Performance Prediction

## 📌 Overview
This project implements a **machine learning pipeline** to predict student pass/fail outcomes and identify at-risk learners based on demographic, assessment, and online engagement data. It leverages **Dask** for distributed data processing and **XGBoost** for high-performance classification.

## 🎯 Objectives
- Aggregate large-scale clickstream activity data using **Dask**.  
- Merge demographic, assessment, and engagement metrics into a unified dataset.  
- Engineer features and encode categorical variables for model training.  
- Train and evaluate an **XGBoost binary classifier** to predict student outcomes.  
- Provide insights for early academic intervention.

## 🛠 Technologies Used
- **Python**
- **Pandas** – Data manipulation
- **Dask** – Distributed/parallel data processing
- **Scikit-learn** – Data preprocessing & metrics
- **XGBoost** – Machine learning classification
- **Google Colab** – Development environment

## 📂 Dataset
The project uses three CSV datasets:
- `studentInfo.csv` – Demographic and academic history  
- `studentAssessment.csv` – Assessment scores  
- `studentVle.csv` – Virtual Learning Environment (VLE) clickstream activity  

> **Note:** These datasets must be stored in Google Drive for this notebook to run as-is.

## 📊 Workflow
1. **Install Dependencies** and mount Google Drive.  
2. **Load Data** – Use Pandas for smaller datasets and Dask for large VLE clickstream data.  
3. **Aggregate Click Data** – Calculate total clicks per student using distributed processing.  
4. **Merge Datasets** – Combine demographic, assessment, and clickstream data.  
5. **Feature Engineering** – Handle missing values, create pass/fail labels.  
6. **Encode Categorical Features** – Apply label encoding to non-numeric fields.  
7. **Model Training** – Train an XGBoost binary classifier.  
8. **Evaluation** – Generate a classification report (precision, recall, F1-score).

## 📈 Example Output
- Aggregated total clicks per student.  
- Merged dataset with demographic and performance metrics.  
- Model performance report showing prediction accuracy.

## 🏆 Results
The trained XGBoost model achieved strong predictive performance:  
- **High recall** for detecting at-risk students, ensuring minimal false negatives.  
- **Balanced precision and recall**, making it reliable for early academic intervention.  
- Generated actionable insights to identify students likely to fail or withdraw.  

These results indicate that the pipeline can be effectively used for **predictive learning analytics** in educational settings.

## 🚀 Getting Started

### Prerequisites
```bash
pip install dask[complete] scikit-learn xgboost pandas
