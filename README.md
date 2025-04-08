#  Integrated Wildfire Risk Prediction and Monitoring System

A comprehensive wildfire prediction and monitoring framework built using multi-source data and advanced machine learning techniques. The system integrates real-time fire data, meteorological parameters, satellite imagery, and human activity data to assess fire risk and predict wildfire occurrences in regions like Queensland, Australia.

![Python](https://img.shields.io/badge/python-3.8%2B-blue)

##  Table of Contents

- [Project Overview](#project-overview)
- [Key Features](#key-features)
- [Data Sources](#data-sources)
- [Methodology](#methodology)
- [Model Performance](#model-performance)
- [Getting Started](#getting-started)
- [Results](#results)
- [Team Contributions](#team-contributions)
- [Future Work](#future-work)

## Project Overview

Wildfires have devastating ecological and economic impacts. This project aims to:

- Predict wildfire risk using diverse data sources.
- Build interpretable and robust machine learning models.
- Provide real-time alerts and long-term risk assessments.
- Create a scalable early warning system for wildfire-prone regions.

## Key Features

-  Real-time data collection from APIs (NASA FIRMS, Open Meteo)
-  Feature-rich dataset combining meteorology, vegetation indices, soil parameters, and human activity
-  ML Models: XGBoost, Random Forest, LSTM, SVM, KNN, Decision Tree, Logistic Regression
-  Geospatial & Temporal visualizations
-  Model evaluation with AUROC, AUPRC, F1, MAE, RMSE, and more

## Data Sources

| Source              | Data Collected                              |
| ------------------- | ------------------------------------------- |
| NASA FIRMS          | Fire location, brightness, confidence       |
| Open Meteo API      | Weather (temperature, humidity, etc.)       |
| USGS Earth Explorer | Satellite imagery, DEM, vegetation indices  |
| OpenStreetMap       | Roads, buildings, elevation, human activity |

## 🛠️ Methodology

1. **Data Integration**
2. **EDA & Preprocessing**
3. **Modeling**
4. **Feature Engineering**

##  Model Performance

| Model               | Accuracy | Precision | Recall | AUC-ROC |
| ------------------- | -------- | --------- | ------ | ------- |
| LSTM                | 0.82     | 0.77      | 0.90   | 0.90    |
| XGBoost             | 0.80     | 0.81      | 0.80   | 0.88    |
| Random Forest       | 0.79     | 0.80      | 0.79   | 0.87    |
| K-Nearest Neighbors | 0.76     | 0.77      | 0.76   | 0.83    |
| SVM                 | 0.69     | 0.72      | 0.70   | 0.75    |
| Decision Tree       | 0.74     | 0.75      | 0.74   | 0.79    |
| Logistic Regression | 0.64     | 0.64      | 0.64   | 0.70    |

##  Getting Started

```bash
# Clone the repository
git clone https://github.com/<your-username>/wildfire-risk-prediction.git
cd wildfire-risk-prediction

# Install dependencies
pip install -r requirements.txt

# Run training script
python train_model.py

# Evaluate model
python evaluate.py
```

> Configure API keys for NASA FIRMS and Open Meteo before running scripts.

##  Results

- LSTM achieved best recall (0.90), ideal for early warning systems.
- XGBoost and Random Forest had consistent performance across all metrics.
- Most important features: Evapotranspiration, soil temperature, humidity.

##  Team Contributions

- **Girish Jeswani** – Data Collection, LSTM, Random Forest
- **Siddhant Kodolkar** – EDA (FIRMS), XGBoost
- **Nishchal Shetty** – EDA (Weather), SVM
- **Darshan Vijayaraghavan** – Decision Tree, KNN, Logistic Regression

##  Future Work

- Extend to convolutional LSTM and CNNs
- Model explainability with SHAP/LIME
- Real-time web dashboard (Streamlit or Flask)
- Broader application across global fire-prone regions
