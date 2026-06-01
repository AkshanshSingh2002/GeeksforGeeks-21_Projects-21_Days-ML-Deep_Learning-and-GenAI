# 21 Projects in 21 Days – Machine Learning, Deep Learning & GenAI

## 🧠 Overview

Welcome to the **21 Projects in 21 Days** challenge! This repository documents a comprehensive learning journey through Machine Learning, Deep Learning, and Generative AI. Each day features a hands-on project designed to build practical skills, from foundational data analysis to advanced neural networks and AI applications.

**Learning Goals:**

- Master data exploration, visualization, and storytelling
- Implement ML algorithms (classification, regression, clustering)
- Build deep learning models (CNNs, RNNs, Transformers)
- Explore generative AI and prompt engineering
- Develop end-to-end solutions for real-world problems

---

## 📂 Project List

| Day | Project | Focus Area |
|-----|---------|------------|

| 01 | Data Storytelling: Analysing Survival on the Titanic | EDA, Feature Engineering, Classification |\
| 02 | Cracking the Code: An Inside Look at Netflix's Content Strategy | Data Analysis, Content Strategy, Visualization |\
| 03 | House Price Prediction (Regression) | Model Training, Evaluation, Linear Regression, xgboost |\
| 04 | AI in Healthcare: Building a Life-Saving Heart Disease Predictor | Classification, Model Evaluation, Medical Data Analysis |\
| 05 | Smart Segmentation: Unlocking Customer Personas with AI | Clustering, Unsupervised Learning, Customer Segmentation |\
| 06 | Time Series Forecasting | ARIMA, SARIMA, Deep Forecasting |\
| 07 | Preventing Customer Churn with Feature Transformation | Feature Engineering, Classification, Churn Prediction |\
| 08 | Vision AI Fundamentals: Digit Recognizer | CNNs, ANN, Image Classification |\
| 09 | Advanced Vision AI: Transfer Learning | Transfer Learning, Fine-tuning, Pretrained Models |\
| 10 | The AI Swiss Army Knife: Hugging Face Pipelines | NLP & Vision pipelines, Quick demos |\
| 11 | Real-World Computer Vision: Object Detection | YOLO, Real-time Detection, OpenCV |\
| 12 | Next-Gen Forecasting: Time Series DL | Deep Learning for Forecasting, LSTMs, Transformers |\
| 13 | Build Your Own GPT: Text Generation Engine | Language Models, Prompting, Fine-tuning |\
| 14 | Data Analysis with AI Tools | EDA, Market Analysis, Automated Reporting |\
| 15 | Talk to Your Data: NL → SQL Generator | Natural Language Interfaces, SQL Generation |\
| 16 | Intelligent Document Automation: OCR Bot | OCR, Resume Parsing, Document Extraction |\
| 17 | Intelligent Image Search Engine | Embeddings, Vector DB, Image Retrieval |\
| 18 | Chat with Your Knowledge Base: RAG Chatbot | Retrieval-Augmented Generation, Vector Search |\
| 19 | Autonomous Market Analyst: AI Agents | Agent Design, Research Automation, Synthesis |\
| 20 | Background Verification & Diligence Agent | Automation for Due Diligence, Verification Workflows |\
| 21 | Building an AI-Powered Newsletter Pipeline on n8n | Automation, Content Summarization, Publishing |

---

## ⚙️ Tech Stack

- **Languages:** Python 3.13
- **Notebooks:** Jupyter Lab
- **Data Processing:** Pandas, NumPy, SciPy
- **ML Libraries:** Scikit-learn, Statsmodels
- **Visualization:** Matplotlib, Seaborn, Plotly
- **Deep Learning:** TensorFlow, PyTorch
- **Computer Vision:** OpenCV
- **Profiling & Analysis:** Ydata-profiling, Phik
- **Environment:** Conda

---

## 🚀 Installation & Setup

### Prerequisites

- Python 3.13+
- Git
- Conda (recommended)

### Steps

1. **Clone the repository:**

    ```bash
    git clone https://github.com/AkshanshSingh2002/GeeksforGeeks-21_Projects-21_Days-ML-Deep_Learning-and-GenAI.git
    cd GeeksforGeeks-21_Projects-21_Days-ML-Deep_Learning-and-GenAI
    ```

2. **Set up the environment:**

    ```bash
    conda env create -f environment.yml
    conda activate env
    ```

3. **Launch Jupyter Lab:**

    ```bash
    jupyter lab
    ```

4. **Navigate to desired project folder and open the notebook:**

    ```bash
    Open Day01_Data Storytelling-Analysing Survival on the Titanic/1_Data Storytelling_ Analysing Survival on the Titanic.ipynb
    ```

---

## 📊 Project Structure

```bash
    Day{NN}_ProjectName/
    ├── {N}_ProjectName.ipynb          # Main project notebook
    ├── L{N}_Assignment.ipynb          # Assignment notebook
    ├── Readme.md                      # Project-specific documentation
    ├── Profiling Report.html          # Dataset profiling report (Optional, not neccessarily available)
    └── data/
         └── Dataset-File.csv           # Raw data 
```

---

## 🧩 Project Highlights

### Project 01 – Data Storytelling: Titanic Survival Analysis

Complete EDA project analyzing Titanic passenger survival. Covers data cleaning, feature engineering, univariate/bivariate/  multivariate analysis, and correlation studies. Key insight: Gender, class, and age were primary survival factors. Includes ydata-profiling report.

### Project 02 – Cracking the Code: Netflix Content Strategy

This project conducts a comprehensive exploratory data analysis of Netflix's content library, revealing that 70% of content is movies with accelerated growth from 2016-2019, while the US leads in production followed by India and the UK. The analysis uncovers that TV-MA and TV-14 ratings dominate the platform, reflecting a mature audience focus, and that most TV shows are single-season productions. Advanced techniques including data cleaning, multi-value column handling, time-series analysis, and feature engineering are employed to extract insights on content themes, director rankings, and temporal trends.

### Project 03 – House Price Prediction (Regression)

An end-to-end machine learning project that builds and compares regression models to predict house sale prices based on various property features. This project demonstrates the complete ML workflow from exploratory data analysis (EDA) to advanced preprocessing, feature engineering, model training, and evaluation.

### Project 04 – Heart Disease Prediction (Classification)

Develop an accurate predictive model to classify whether a patient has heart disease using medical features like age, cholesterol, chest pain type, and maximum heart rate.

### Project 05 – Smart Segmentation - Unlocking Customer Personas with AI

This project focuses on customer segmentation using unsupervised machine learning techniques, specifically clustering algorithms like K-Means and Hierarchical Clustering. The goal is to identify distinct groups of customers based on their demographic and behavioral data to enable targeted marketing strategies.

### Project 06 - Time Series Forecasting

ARIMA/SARIMA models for predicting airline passenger trends, focusing on stationarity (p-value < 0.05) and seasonality.

### Project 07 – Preventing Customer Churn with Feature Transformation

Hands-on project using the Telco Customer Churn dataset to explore feature transformations, encoding strategies, and churn-prediction models. Focuses on improving model performance through careful preprocessing and feature engineering.

### Project 08 – Vision AI Fundamentals: Digit Recognizer

Building image classifiers from scratch using ANN/CNN architectures on small image datasets. Includes data preprocessing, model training, evaluation, and saved model weights for the best-performing runs.

### Project 09 – Advanced Vision AI: Transfer Learning

Demonstrates transfer learning workflows with pre-trained backbones (VGG16, ResNet50, MobileNetV2) for fast, accurate image classification and fine-tuning techniques for custom datasets.

### Project 10 – The AI Swiss Army Knife: One-Line Solutions with Hugging Face Pipelines

Short, practical demos showing how Hugging Face pipelines can be used to quickly solve common NLP and vision tasks with minimal code.

### Project 11 – Real-World Computer Vision: Object Detection

Implementing YOLO-based object detection for images and live video streams, with examples and a sample `yolov8n.pt` model for quick experimentation.

### Project 12 – Next-Gen Forecasting: Deep Learning for Time Series

Applies deep learning approaches (LSTMs, CNNs, and Transformer-based architectures) to forecasting problems, demonstrating end-to-end preprocessing, training, and evaluation.

### Project 13 – Build Your Own GPT: Creating a Custom Text Generation Engine

Guided notebook covering language model usage, prompt design, fine-tuning/adaptation, and assembly of a simple text-generation pipeline.

### Project 14 – Data Analysis with AI Tools

Market and insurance data analyses using AI-assisted tooling to accelerate exploratory analysis, visualization, and report generation.

### Project 15 – Talk to Your Data: Natural Language to SQL Generator

Demonstrates how to translate natural language questions into SQL queries for tabular datasets and run them to return answers—useful for quick data exploration.

### Project 16 – Intelligent Document Automation: Building a Smart OCR Bot

Automates document ingestion and structured data extraction (for example, resumes), producing cleaned CSV outputs and demonstrating practical OCR pipelines.

### Project 17 – Build Your Own Intelligent Image Search Engine

Creates an image search pipeline using embedding models and a vector database (Chroma) for fast similarity search and retrieval over an image corpus.

### Project 18 – Chat with Your Knowledge Base: Building a Powerful RAG Chatbot

Builds a retrieval-augmented generation (RAG) chatbot that indexes documents into a vector store and answers user queries with grounded responses.

### Project 19 – Autonomous Market Analyst: Building AI Agents for Deep Research

Designs AI agents that can autonomously gather, synthesize, and summarize market research data, enabling semi-automated analyst workflows.

### Project 20 – Background Verification & Diligence Agent

Demonstrates an agent-driven workflow for automating basic background checks and due diligence tasks, integrating data retrieval and synthesis steps.

### Project 21 – Building an AI-Powered Newsletter Pipeline on n8n

End-to-end automation example using n8n to collect content, summarize and enrich it with AI, and publish a recurring newsletter with minimal manual effort.

## 📫 Contact

- **GitHub:** [AkshanshSingh2002](https://github.com/AkshanshSingh2002)
- **LinkedIn:** [Akshansh Singh](www.linkedin.com/in/akshanshsingh2002)
- **Email:** <akshanshsingh2002@gmail.com>

Feel free to open issues, contribute, or reach out with questions!

If you'd like, I can also add direct links to each day's notebook from this README or commit the change for you.
