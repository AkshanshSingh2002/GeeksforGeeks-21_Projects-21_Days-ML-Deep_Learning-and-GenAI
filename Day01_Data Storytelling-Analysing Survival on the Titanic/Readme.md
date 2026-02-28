
# README.md for Day01 Project

## Project: Data Storytelling - Analysing Survival on the Titanic

### Overview
This project performs a comprehensive Exploratory Data Analysis (EDA) on the Titanic dataset to understand the key factors influencing passenger survival. Through systematic data cleaning, feature engineering, and visualization, we uncover patterns that reveal the social dynamics of the disaster.

### Contents

#### Notebooks
- **1_Data Storytelling_Analysing Survival on the Titanic.ipynb** - Complete EDA with theoretical explanations
- **L1_Assignment.ipynb** - Data cleaning and profiling assignment

#### Key Sections

1. **Data Loading & Inspection** - Initial dataset overview and structure analysis
2. **Data Cleaning** - Handling missing values in Age, Embarked, and Cabin columns
3. **Univariate Analysis** - Individual variable distributions for categorical and numerical features
4. **Bivariate Analysis** - Relationships between features and survival outcomes
5. **Feature Engineering** - Creating FamilySize, IsAlone, and Title features
6. **Multivariate Analysis** - Complex interactions between multiple variables
7. **Correlation Analysis** - Heatmap of numerical feature correlations
8. **Data Profiling** - ydata-profiling HTML report

### Key Findings

**Strongest Survival Predictors:**
- Gender (Female > Male)
- Passenger Class (1st > 2nd > 3rd)
- Age (Children had higher survival rates)
- Title (Mrs, Miss, Master)
- Family Size (Small families 2-4 members had best odds)

### Technologies Used
- Pandas, NumPy
- Matplotlib, Seaborn
- ydata-profiling

### Output
- `Titanic Dataset Profiling Report.html` - Comprehensive profiling report
