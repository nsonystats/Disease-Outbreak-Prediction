
Project Overview:

This project presents a comprehensive early-warning framework to forecast infectious disease outbreaks in India by blending:

Classical Time Series Forecasting (SARIMA, Prophet) Supervised Machine Learning (Random Forest) Geospatial Analytics (District-wise spread & lag modeling)

The models are trained on real-world epidemiological data from the Government of India, capturing both seasonal (Dengue, Malaria) and non-seasonal (Chickenpox, Food Poisoning)diseases, helping predict future outbreaks and optimize public health interventions.

Objectives:

Predict disease outbreaks with high sensitivity and precision
Compare forecasting performance of SARIMA and Prophet
Develop a Random Forest-based early warning classifier
Identify spatial-temporal disease transmission across districts
Provide insights for targeted resource allocation and policy-making
Dataset Overview:

Source: IDSP, Ministry of Health and Family Welfare, Govt. of India

Time Frame: Jan 2022 – Feb 2025

Diseases Modeled: Dengue, Malaria, Chickenpox, Food Poisoning

Volume: 6,200+ records | 17 districts

Key Features:

State, District, Disease Name
Number of Cases, Deaths
Outbreak & Reporting Dates
Status, Action Taken
Technical Stack:

Category	Tools & Libraries
Time Series Forecasting	SARIMA, SARIMAX, Prophet, ADF, Seasonal Decomposition
ML Classification	Random Forest, SMOTE, Scikit-learn
Geo-Visualization	Plotly, GeoPandas, Folium, Plotly Express
Data Engineering	Pandas, NumPy
Evaluation	ADF Test, Confusion Matrix, F1 Score, ROC-AUC
Methodology:

Time Series Modeling:

Models: SARIMA (for seasonal), Prophet (for both)

Steps:

Stationarity check via ADF test
Lag feature engineering: Lag_1, Lag_2, Rolling Mean_3
Trend, seasonality & residual decomposition
Outcome:

Forecasts until 2025
Detection of seasonality (e.g., Dengue peaks in Sept)
Increasing trend observed in Chickenpox, Food Poisoning
ML Early Warning System:

Target: Binary classification — Outbreak if ≥ 10 cases *Issue: Class Imbalance (16 outbreaks vs 3711 non-outbreaks) *Solution: Applied SMOTE + Stratified K-Fold CV *Model: Random Forest Classifier *Performance:

Accuracy: 99.87%
ROC-AUC: 0.9996
F1 Score: 0.8571 @ threshold = 0.30
All true outbreaks detected (Recall = 1.00)
Geo-Spatial Analysis:

Plotted district-wise disease intensity from 2022–2025
Applied Pearson correlation & cross-correlation
Identified lead-lag effects(e.g., Kozhikode leads Malappuram by 9 months)
Created interactive maps to visualize hotspot evolution
Key Results:

Category	Result/Insight
SARIMA Forecasting	Accurately captured seasonal disease peaks (esp. Dengue, Malaria)
Prophet Model	Strong trend tracking, especially for non-seasonal diseases
ML Classification	High accuracy and recall for detecting rare outbreaks
Feature Importance	Rolling mean over 3 periods was most predictive (~80% importance)
Geo-Spatial Lag Analysis	Showed inter-district transmission delay patterns (cross-correlation peaks)
Public Health Insights	Provided actionable insights for intervention scheduling and hotspot control
Visual Outputs Included :

Time Series Trend, Forecast & Seasonality (SARIMA, Prophet)
Random Forest Confusion Matrix & Feature Importance
Interactive Geo Maps for 2022–2025 outbreaks
Cross-district Lag Plots and Correlation Heatmaps
Monthly and Yearly Forecast Highlights per Disease
The full dataset used in this project is sourced from the Government of India’s [IDSP Portal] (https://idsp.nic.in) and may not be redistributed publicly.
