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
