# Smart Healthcare Prediction System
## Diabetes Risk Assessment Using Ensemble Machine Learning

### Overview
This project implements a **Smart Healthcare Prediction System** that applies **ensemble machine learning techniques** to classify patients into three risk categories:
- **Non-Diabetic**
- **Pre-Diabetic** 
- **Diabetic**

The system was developed using the **Diabetes 130-US Hospitals dataset (1999-2008)**, comprising approximately **100,000 patient records** across **50 clinical features**. 

Four ensemble models were implemented and compared: `Random Forest`, `Gradient Boosting`, `AdaBoost`, and a `Voting Classifier`.

### Key Features
- **Multi-class Classification**: Three clinically meaningful risk categories instead of just binary
- **SMOTE Balancing**: Synthetic Minority Over-sampling Technique for class imbalance correction
- **Ensemble Learning**: Combines multiple models for robust prediction
- **Web Application**: Flask-based real-time risk prediction with personalized health recommendations
- **Cross-Dataset Validation**: Innovation component using Pima Indians Diabetes Dataset

### Dataset

#### Primary Dataset — Diabetes 130-US Hospitals
- **Source**: UCI Machine Learning Repository / Kaggle
- **Size**: 101,766 patient encounter records
- **Features**: 50 clinical attributes
- **Target**: Readmission status `NO / >30 days / <30 days`

#### Innovation Dataset — Pima Indians Diabetes
- **Source**: UCI / Kaggle
- **Size**: 768 records, 8 features
- **Task**: Binary classification `Diabetic / Non-Diabetic`

### Models Implemented

| Model | Accuracy | Weighted F1 |
| --- | --- | --- |
| Random Forest (Tuned) | 57.5% | 0.541 |
| Gradient Boosting | 57.7% | 0.541 |
| AdaBoost | 50.1% | 0.508 |
| **Voting Classifier (Best)** | **57.9%** | **0.545** |

### Tech Stack
- **Python**: scikit-learn, pandas, numpy, matplotlib, seaborn
- **Web**: Flask, HTML5, CSS3
- **Utilities**: joblib, ngrok

### Project Structure
smart-healthcare-prediction/
├── ML_CCP_Report_Mahmoona_Khan.pdf   # Full project report
├── diabetes_prediction.ipynb         # Main Jupyter notebook
├── app.py                            # Flask web application
├── requirements.txt                  # Python dependencies
├── model/                            # Saved model files
│   └── voting_classifier.pkl
├── static/                           # CSS and assets
├── templates/                        # HTML templates
│   └── index.html
└── README.md

### How to Run

1. Notebook (Training & Evaluation)
Open diabetes_prediction.ipynb in Google Colab or Jupyter Notebook and run all cells.

### 2. Web Application
  bash
  pip install -r requirements.txt
  python app.py

### Results Summary
- Best Model: Voting Classifier (Soft)
- Primary Dataset F1: 0.545 (3-class)
- Pima Indians F1: 0.73-0.76 (binary) — validates model soundness
- SMOTE Effect: Successfully balanced all three classes to 10,666 samples each

### Key Insights
  Clinical complexity indicators (lab procedures, medications, time in hospital) are the strongest predictors
  The 20+ point F1 gap between datasets confirms lower primary accuracy is due to dataset complexity, not model deficiency
  Class 0 (Non-Diabetic) remains the hardest to classify correctly even after SMOTE


### Author
Mahmoona Khan
BSCS
Lahore Garrison University
Course: CSE6505 — Machine Learning
Instructor: Khuram Tehseen
Submission Date: May 11, 2026
