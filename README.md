# Team A: Ames Housing Price Prediction & Market Analysis

Welcome to Team A's Capstone Project! This repository contains an end-to-end data science pipeline that analyzes the Ames Housing Dataset to predict residential property valuations and uncover the key structural and spatial factors driving real estate prices.

## 🎯 Problem Statement
In the real estate market, inaccurately predicting property values can lead to massive financial miscalculations for buyers, sellers, and investors. It is often difficult to quantify exactly how much value specific physical features (like square footage or overall condition) add to a property, and how non-linear factors like neighborhood or zoning impact the final valuation. This project builds a data-driven predictive pipeline to minimize these valuation errors.

## 👥 The Team & Roles
This capstone was a collaborative effort, divided across four distinct stages of the data lifecycle to leverage each team member's strengths:

*   **Latita Mvunelo** (Team Leader): Machine Learning & Predictive Modeling
*   **Trizah Nasumba**: SQL Data Extraction & Integrity
*   **Favour Chibaya**: Python Exploratory Data Analysis (EDA) & Feature Engineering
*   **Tanran Ethrudies Suhliy**: Business Intelligence & Power BI Dashboarding

## 🛠️ Methodology & Tech Stack

### 1. Data Extraction & Integrity (SQL)
*   **Lead:** Trizah Nasumba
*   **Tech:** SQLite / SQL
*   **Scope:** Audited the raw Ames database, mapped primary keys, and executed queries to filter out non-typical transactions. Calculated baseline market summaries (e.g., median sale prices, yearly sale volumes, and missing data identification) to feed into the Python environment.

### 2. Exploratory Data Analysis (Python)
*   **Lead:** Favour Chibaya
*   **Tech:** Python (Pandas, NumPy, Seaborn, Matplotlib)
*   **Scope:** Analyzed statistical distributions, computed skewness, and assessed temporal trends for `SalePrice`. Explored the impact of physical characteristics, detected extreme multivariate outliers, and handled missing data imputation. Applied one-hot and ordinal encoding to prepare the features for machine learning.

### 3. Machine Learning Pipeline
*   **Lead:** Latita Mvunelo
*   **Tech:** Python (Scikit-Learn)
*   **Scope:** Benchmarked baseline performance using Multiple Linear Regression. Tuned and deployed a Random Forest Regressor to capture non-linear feature interactions. Optimized models using RMSE (Root Mean Squared Error) to heavily penalize large, costly pricing mistakes, and extracted the top 10 most influential property features.

### 4. Interactive Dashboarding (Power BI)
*   **Lead:** Tanran Ethrudies Suhliy
*   **Tech:** Microsoft Power BI, DAX
*   **Scope:** Ingested the clean data and model predictions to build a multi-page interactive dashboard. Designed visuals for pricing trends across neighborhoods, dynamic slicers for physical attributes, and a scenario interface to inspect actual vs. predicted prices for model performance evaluation.

## 🚀 Key Findings & Results
*   **Model Performance:** The tuned Random Forest Regressor significantly outperformed the baseline Linear Regression model, successfully reducing the RMSE and explaining over 91% of the variance in the housing market ($R^2 = 0.916$).
*   **Key Drivers of Value:** Feature importance extraction confirmed that core structural variables—specifically Overall Quality, Above Ground Living Area (`GrLivArea`), and Neighborhood—are the dominant drivers of a property's final valuation in Ames.
*   **Dashboard Insights:** The Power BI deployment successfully allows stakeholders to dynamically filter neighborhoods and overall quality ratings, proving that predictive valuation errors drop significantly when analyzing homes with standard dimensions versus extreme outliers.

## 📁 Repository Structure

```text
├── /data/       # Contains the raw and cleaned Ames Housing CSV files
├── /sql/        # SQL scripts for data extraction and baseline aggregation
├── /notebooks/  # Jupyter/Colab notebooks containing the Python EDA and ML pipelines
└── /dashboard/  # The .pbix Power BI file and exported PDF reports
```

---
*This project was completed as part of our Data Science Capstone. Feel free to explore the code, interact with the dashboard, and reach out to any of the team members with questions!*