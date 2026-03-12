# Day 5: Smart Segmentation - Unlocking Customer Personas with AI

## Project Overview

This project focuses on customer segmentation using unsupervised machine learning techniques, specifically clustering algorithms like K-Means and Hierarchical Clustering. The goal is to identify distinct groups of customers based on their demographic and behavioral data to enable targeted marketing strategies.

## Objectives

- Understand the fundamentals of unsupervised learning and clustering.
- Perform exploratory data analysis (EDA) on customer data.
- Apply K-Means clustering to segment customers based on income and spending score.
- Use the Elbow Method to determine the optimal number of clusters.
- Visualize and interpret the resulting customer segments.
- Explore alternative clustering approaches like Hierarchical Clustering.

## Dataset

The dataset used is `Mall_Customers.csv`, which contains information about mall customers including:

- CustomerID: Unique identifier for each customer
- Gender: Male or Female
- Age: Age of the customer
- Annual Income (k$): Annual income in thousands of dollars
- Spending Score (1-100): Score assigned by the mall based on customer behavior and spending nature

## Methodology

1. **Data Preprocessing**: Load and clean the dataset, handle missing values if any.
2. **Exploratory Data Analysis**: Analyze distributions, relationships between features using histograms, pair plots, and 3D visualizations.
3. **Feature Selection**: Identify key features for clustering (e.g., Annual Income and Spending Score).
4. **Clustering with K-Means**:
   - Standardize the features.
   - Use the Elbow Method to find optimal k.
   - Apply K-Means clustering.
5. **Visualization and Interpretation**: Plot the clusters and analyze the characteristics of each segment.
6. **Alternative Methods**: Explore Hierarchical Clustering for comparison.

## Results

The analysis reveals distinct customer segments such as:

- High-income, high-spending customers (premium targets)
- Low-income, high-spending customers (enthusiasts)
- High-income, low-spending customers (careful buyers)
- Average customers
- Budget shoppers

## Files

- `5_Smart_Segmentation_Unlocking_Customer_Personas_with_AI (1).ipynb`: Main project notebook with detailed analysis.
- `L5_Assignment.ipynb`: Assignment notebook for submission.
- `data/Mall_Customers.csv`: Dataset file.
- `Readme.md`: This file.

## How to Run

1. Ensure you have Python and required libraries installed (pandas, numpy, matplotlib, seaborn, plotly, scikit-learn).
2. Open the Jupyter notebook `5_Smart_Segmentation_Unlocking_Customer_Personas_with_AI (1).ipynb`.
3. Run the cells sequentially to reproduce the analysis.

## Dependencies

- pandas
- numpy
- matplotlib
- seaborn
- plotly
- scikit-learn

Install via pip: `pip install pandas numpy matplotlib seaborn plotly scikit-learn`

This is part of the GeeksforGeeks 21 Projects in 21 Days: ML, Deep Learning & GenAI series.