# Customer Churn Prediction and Retention Strategy Analysis

## Overview
This project predicts customer churn for a telecommunications company using the Telco Customer Churn dataset (7,043 rows, 21 columns). It demonstrates the following skills:
- **Data Management**: SQL queries, schema/ER diagram comprehension.
- **Machine Learning**: Logistic regression, propensity modeling (AUC 0.84).
- **Big Data**: PySpark for distributed processing.
- **Visualization**: Trend analysis with Seaborn.
- **Business Insights**: Proactive retention strategies (e.g., ~14% churn reduction, ~$131,500 savings).

The project is implemented in a Google Colab notebook (`churn_prediction.ipynb`) and uses `WA_Fn-UseC_-Telco-Customer-Churn.csv` from Kaggle. Last updated: September 10, 2025.

## Dataset
- **Source**: [Kaggle Telco Customer Churn](https://www.kaggle.com/datasets/blastchar/telco-customer-churn) (`archive.zip` containing `WA_Fn-UseC_-Telco-Customer-Churn.csv`).
- **Columns**: `customerID`, `gender`, `tenure`, `MonthlyCharges`, `Churn`, etc.
- **Size**: 7,043 rows, 21 columns.
- **Notes**: `TotalCharges` contains ~11 blanks (handled as 0); high-risk segments include short-tenure (<14 months), fiber optic, and electronic check users.

## Requirements
- Google Colab environment (free tier).
- Libraries: `pandas`, `pandasql`, `pyspark`, `scikit-learn`, `matplotlib`, `seaborn`.
- Upload `archive.zip` (contains `WA_Fn-UseC_-Telco-Customer-Churn.csv`) when prompted.
- Google Drive for cloud-like storage (e.g., saving outputs).

## How to Run
1. Open `churn_prediction.ipynb` in Google Colab (https://colab.research.google.com).
2. Run the first cell to install dependencies (`pandasql`, `pyspark`).
3. Upload `archive.zip` when prompted (contains the dataset CSV).
4. Run all cells sequentially to:
   - Extract and load the dataset.
   - Perform SQL queries for exploration.
   - Clean data and engineer features.
   - Build logistic regression and PySpark models.
   - Visualize trends (saved to Drive).
   - Generate business recommendations.
5. Outputs (data, plots) are saved to `/content/drive/MyDrive/`.

## Project Structure
- `churn_prediction.ipynb`: Main notebook with code and documentation.
- `README.md`: Project overview and instructions.
- `archive.zip`: Dataset (not included in repo; download from [Kaggle](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)).

## Results
- **Model Performance**: Logistic regression achieves ROC AUC 0.84.
- **Insights**: High churn in short-tenure (<14 months, ~45% churn rate), fiber optic users (~41% churn rate), and electronic check users (dominant in 994 month-to-month churns).
- **Business Impact**: Proposed retention campaign targeting 420 high-risk customers (propensity > 0.7) could retain ~263 customers, reducing churn by ~14% and saving ~$131,500 ($500/customer acquisition cost).

## License
MIT License.

## Author
[Sebastian Zappulla] - Data Science Portfolio Project
