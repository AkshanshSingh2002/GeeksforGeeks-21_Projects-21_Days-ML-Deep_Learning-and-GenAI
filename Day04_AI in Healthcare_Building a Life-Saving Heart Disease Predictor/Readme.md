
# Heart Disease Prediction - README

## Project Overview
This project builds machine learning classification models to predict heart disease based on patient medical attributes. It demonstrates a complete end-to-end workflow from data exploration to model evaluation.

## Objective
Develop an accurate predictive model to classify whether a patient has heart disease using medical features like age, cholesterol, chest pain type, and maximum heart rate.

## Dataset
- **Source**: UCI Heart Disease Dataset
- **Records**: 920 patient samples
- **Target**: Binary classification (0: No Disease, 1: Has Disease)
- **Features**: 13 medical attributes

## Key Steps

### 1. Exploratory Data Analysis (EDA)
- Analyzed feature distributions and relationships
- Identified key predictors: `ca`, `thalch`, `oldpeak`, `cp`
- Examined correlations and class balance

### 2. Data Preprocessing
- Handled missing values (mean for numerical, mode for categorical)
- One-hot encoding for categorical variables
- Feature scaling using StandardScaler

### 3. Model Training
Implemented four classification models:
- **Logistic Regression** (Baseline)
- **Random Forest Classifier** (Ensemble)
- **Support Vector Machine (SVM)**
- **K-Nearest Neighbors (KNN)**

### 4. Model Evaluation
Used metrics: Accuracy, Precision, Recall, F1-Score, and Confusion Matrix

## Results
**Random Forest** achieved the best performance:
- Accuracy: ~99%
- Precision & Recall: 99-100%
- Minimal false negatives (critical for medical diagnosis)

## Technologies
Python, Scikit-Learn, Pandas, NumPy, Matplotlib, Seaborn

## Files
- `4_AI_in_Healthcare_Building_a_Life_Saving_Heart_Disease_Predictor.ipynb` - Complete analysis with pipelines
- `L4_Assignment.ipynb` - Manual preprocessing approach (without pipelines)
