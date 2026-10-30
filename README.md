# GDDA709 – ERA5 Weather Analytics

## Project Overview

This project applies Big Data technologies and machine learning techniques to analyse ERA5 atmospheric reanalysis data for Auckland, New Zealand.

The project explores atmospheric conditions across different pressure levels and time periods, using distributed data processing and predictive modelling.

## Dataset

- **Source:** Copernicus Climate Data Store – ERA5
- **Location:** Auckland, New Zealand
- **Records:** Approximately 507,989
- **Time coverage:** 2000–2026
- **Key variables:** Temperature, relative humidity, geopotential, pressure level, and valid time.

## Technologies Used

- Python
- Apache Spark / PySpark
- Databricks
- Delta Lake
- Spark MLlib

## Project Workflow

1. **Data Preprocessing:** Data ingestion, cleaning, transformation, and storage in Delta Lake.
2. **MapReduce Analysis:** Grouping and aggregating atmospheric statistics by pressure level and analysing temporal patterns.
3. **Decision Tree Regression:** Predicting atmospheric temperature 24 hours ahead.
4. **Random Forest Classification:** Classifying future temperature into Low, Medium, and High categories.
5. **Model Evaluation:** Evaluating model performance through regression and classification metrics.

## Repository Structure

```text
GDDA709-ERA5-Weather-Analytics/
│
├── notebooks/
│   ├── 01_Data_Preprocessing.ipynb
│   ├── 02_MapReduce_Analysis.ipynb
│   ├── 03_DecisionTree_Regression.ipynb
│   ├── 04_RandomForest_Classification.ipynb
│   └── 709.ipynb
│
├── README.md
└── .gitignore
```

## Model Evaluation

**Decision Tree Regressor**

- MAE: Approximately 1.95°C
- RMSE: Approximately 2.60°C
- R²: Approximately 0.9914

**Random Forest Classifier**

- Accuracy: 67.31%
- Weighted Precision: 66.74%
- Weighted F1-score: 66.75%

## How to Use

1. Access the notebooks in the `notebooks/` directory.
2. Import the notebooks into a Databricks environment.
3. Configure access to the ERA5 dataset and the required Delta tables.
4. Execute the notebooks in the documented workflow order.

**Note:** The notebooks were developed in Databricks. A compatible Spark environment and access to the required dataset are necessary to reproduce the results.

## Project Purpose

This repository documents the data processing workflow, analytical methods, machine learning implementation, and evaluation results developed for the GDDA709 project.
