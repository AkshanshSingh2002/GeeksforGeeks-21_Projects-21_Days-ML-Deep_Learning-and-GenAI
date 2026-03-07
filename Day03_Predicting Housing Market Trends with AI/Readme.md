# Project 3: House Price Prediction (Regression) 🏠


## Project Objective

To develop a robust regression model that accurately predicts the sale price of houses in Ames, Iowa, using 80 different property features. The project showcases best practices in data science, from understanding the target variable to deploying a production-ready prediction model.

---

## Dataset 📊

- **Source:** Kaggle - House Prices: Advanced Regression Techniques
- **Training Samples:** 1,460 houses
- **Test Samples:** 1,459 houses
- **Total Features:** 81 (including the target variable)
- **Target Variable:** `SalePrice` - The property's sale price in dollars

### Key Features Include:

- **Quality & Condition:** OverallQual, OverallCond, Exterior1st, Exterior2nd
- **Area Features:** LotArea, GrLivArea (Above grade living area), TotalBsmtSF
- **Building Features:** BldgType, HouseStyle, RoofStyle, Foundation
- **Garage Features:** GarageType, GarageArea, GarageCars, GarageYrBlt
- **Basement Features:** BsmtQual, BsmtCond, BsmtFinSF1, BsmtFinSF2
- **Location:** Neighborhood, Condition1, Condition2, LotConfig
- **Year Information:** YearBuilt, YearRemodAdd, MoSold, YrSold

---

## Core Concepts Covered 📚

1. **Regression vs. Classification:** Understanding continuous value prediction
2. **Target Variable Analysis:** Distribution analysis with skewness detection and log transformation
3. **Advanced Data Preprocessing:** 
   - Handling missing values strategically
   - Imputation by neighborhood for spatial features
   - Mode-based imputation for categorical features
4. **Feature Engineering:** Creating derived features (TotalSF, TotalBath, Age)
5. **Categorical Encoding:**
   - Label Encoding for ordinal features
   - One-Hot Encoding for nominal features
6. **Feature Scaling:** StandardScaler for linear models
7. **Model Training:** Baseline vs. advanced models
8. **Model Evaluation:** RMSE, MAE, R-squared metrics

---

## Project Workflow 🔄

### Step 1: Setup & Data Loading ✅

- Import necessary libraries (pandas, scikit-learn, XGBoost)
- Load training and test datasets
- Display basic dataset statistics

### Step 2: Exploratory Data Analysis (EDA) 📈

- Analyze SalePrice distribution
- Detect positive skewness
- Identify top correlated features
- Visualization with seaborn and matplotlib

### Step 3: Data Preprocessing ⚙️

- **Handle Missing Values:**
  - Numerical features: Fill with 0 (logical for area/count features)
  - LotFrontage: Impute with neighborhood median
  - Categorical features: Fill with 'None' or mode
  
- **Feature Engineering:**
  - `TotalSF` = TotalBsmtSF + 1stFlrSF + 2ndFlrSF
  - `TotalBath` = FullBath + 0.5×HalfBath + BsmtFullBath + 0.5×BsmtHalfBath
  - `Age` = YrSold - YearBuilt

- **Categorical Encoding:**
  - One-hot encoding for all remaining categorical features

### Step 4: Feature Transformation 🔄

- Apply log transformation to target variable: `log(SalePrice)`
- Standardize features using StandardScaler
- Reduce skewness from +1.88 to near 0

### Step 5: Model Development & Training 🤖

**Model 1: Linear Regression (Baseline)**

- Simple, interpretable model
- Assumes linear relationships
- Serves as performance baseline

**Model 2: XGBoost (Advanced)**

- Gradient boosting algorithm
- Parameters:
  - n_estimators: 1000
  - learning_rate: 0.05
  - max_depth: 3
  - subsample: 0.8
  - colsample_bytree: 0.8

### Step 6: Model Evaluation 📊

| Metric | XGBoost Performance |
|--------|-------------------|
| RMSE | Lower error rate |
| MAE | Better average prediction accuracy |
| R-squared | High variance explanation |

*XGBoost significantly outperforms Linear Regression, capturing non-linear relationships in the data.*

### Step 7: Predictions & Submission 🎯

- Generate predictions on test set using best model
- Reverse log transformation to original price scale
- Create submission.csv with Id and SalePrice columns

---

## Results & Insights 💡

### Key Findings:

1. **Most Influential Features:**
   - OverallQual (Overall Quality)
   - GrLivArea (Above ground living area)
   - GarageCars & GarageArea

2. **Model Performance:**
   - XGBoost demonstrates superior predictive power
   - Handles non-linear relationships effectively
   - Outperforms linear baseline across all metrics

3. **Data Distribution:**
   - Original SalePrice: Positively skewed (right-tailed)
   - After log transformation: Near-normal distribution
   - Improves model assumptions and performance

---

## How to Use 🚀

### Prerequisites:

```bash
pip install pandas numpy scikit-learn xgboost matplotlib seaborn scipy
```

### Running the Notebook:

1. Download the notebook: `3_Predicting_Housing_Market_Trends_with_AI.ipynb`
2. Set up Kaggle API (if using automatic dataset download)
3. Run cells sequentially or the entire notebook
4. View outputs and generated `submission.csv`

### Kaggle API Setup (Optional):

1. Visit [https://www.kaggle.com/account](https://www.kaggle.com/account)
2. Click 'Create New Token' in API section
3. Upload `kaggle.json` when prompted in the notebook

---

## Files in This Directory 📁

- `3_Predicting_Housing_Market_Trends_with_AI (1).ipynb` - Main project notebook
- `Readme.md` - This file
- `data/train.csv` - Training dataset (1,460 samples)
- `data/test.csv` - Test dataset (1,459 samples)
- `data/data_description.txt` - Feature descriptions
- `submission.csv` - Final predictions for submission

---

## Next Steps & Improvements 🔮

1. **Hyperparameter Tuning:**
   - Use GridSearchCV or RandomizedSearchCV
   - Optimize XGBoost parameters further
   - Cross-validation for better generalization

2. **Advanced Feature Engineering:**
   - Interaction terms between key features
   - Polynomial features
   - Domain-specific derived features

3. **Ensemble Methods:**
   - Combine predictions from multiple models
   - Stacking or blending techniques
   - Weighted averaging of models

4. **Outlier Detection:**
   - Identify and handle extreme property prices
   - Investigate high-residual predictions

5. **Model Interpretation:**
   - SHAP values for feature importance
   - Permutation importance analysis
   - Individual prediction explanations

---

## Learning Outcomes 🎓

By completing this project, you will understand:

- ✅ Complete regression pipeline from raw data to predictions
- ✅ Professional data preprocessing and cleaning strategies
- ✅ Feature engineering techniques for structured data
- ✅ Categorical encoding methods (ordinal vs. nominal)
- ✅ Tree-based models vs. linear models
- ✅ Model evaluation metrics for regression problems
- ✅ Handling skewed distributions with transformations
- ✅ Production-ready prediction workflows

---

## Technologies Used 🛠️

- **Python 3.x**
- **pandas** - Data manipulation
- **numpy** - Numerical computing
- **scikit-learn** - ML algorithms and preprocessing
- **XGBoost** - Advanced gradient boosting
- **matplotlib & seaborn** - Data visualization
- **scipy** - Statistical analysis

---

## Acknowledgments 🙏

- Kaggle: House Prices competition dataset
- GeeksforGeeks: 21 Days ML Deep Learning & GenAI Program

---

**Author:** Akshansh Singh | **Date:** 2026 | **Difficulty Level:** Intermediate
