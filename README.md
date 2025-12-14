# 🚲 Bike Rental Demand Prediction

## Project Overview
This project focuses on **predicting bike rental demand** using historical data collected from a bike-sharing system. The objective is to understand how **temporal, seasonal, and weather-related factors** influence bike usage and to build reliable machine learning models that can accurately forecast demand at both **daily** and **hourly** levels.

The project follows the **complete Data Science life cycle** — from data understanding and exploratory data analysis (EDA) to feature engineering, model building, evaluation, and final conclusions.

---

## Business Problem
Accurate demand prediction is critical for bike-sharing companies to:
- Optimize bike availability and distribution
- Reduce operational costs
- Improve customer satisfaction
- Plan maintenance and resource allocation

This project aims to answer:
> *“Given weather and time-based features, how many bikes will be rented?”*

---

## Datasets Used
Two datasets are analyzed **independently** due to different granularities:

### 1. Day-Level Dataset
- Captures **daily trends and seasonality**
- Suitable for long-term planning and forecasting

### 2. Hourly-Level Dataset
- Captures **hourly demand patterns**
- Useful for understanding peak hours, commuting behavior, and short-term fluctuations

The datasets are **not merged** to preserve their individual analytical value.

---

## Exploratory Data Analysis (EDA)
- Distribution analysis of bike rentals
- Impact of weather conditions, working days, and seasons
- Comparison of demand patterns across time
- Outlier detection and variability analysis

Each visualization is supported with **clear insights and observations**.

---

## Feature Engineering
- Date-time feature extraction (hour, day, month, weekday)
- Encoding of categorical variables
- Removal of leakage-prone features (`casual`, `registered`)
- Consistent preprocessing pipeline for fair model comparison

---

## Modeling Approach

### Models Used

#### Day Dataset
- **Linear Regression** (baseline)
- **Random Forest Regressor** (primary model)

#### Hourly Dataset
- **Linear Regression** (baseline)
- **Random Forest Regressor**
- **XGBoost Regressor**

Model selection was driven by:
- Dataset size
- Feature complexity
- Bias–variance tradeoff

---

## Evaluation Metrics
All models are evaluated using:
- **R² Score** – Variance explained by the model
- **MAE (Mean Absolute Error)** – Average prediction error
- **RMSE (Root Mean Squared Error)** – Penalizes large errors

Hyperparameter tuning was applied only where meaningful.

---

## Results Summary
- **Day Data:** Random Forest Regressor performed best
- **Hourly Data:** Hyper-tuned XGBoost achieved the highest performance
- Tree-based models significantly outperformed linear models due to non-linear patterns in the data

---

## Key Challenges
- Managing two datasets with different granularities
- Preventing data leakage
- Handling large trained model files in version control
- Selecting models appropriate to dataset size

---

## Key Learnings
- Ensemble models excel in real-world tabular data
- Dataset granularity heavily influences model choice
- R² is not accuracy; MAE and RMSE provide business-relevant insights
- Proper EDA is critical before modeling
- Model artifacts should not be stored directly in GitHub repositories

---

## Notes
- Trained model (`.pkl`) files are intentionally excluded due to GitHub size limitations.
- Models can be regenerated using the provided notebooks.

---

## Conclusion
This project demonstrates an **end-to-end machine learning workflow** with strong emphasis on **EDA, justified model selection, and professional evaluation practices**. The approach reflects real-world data science problem-solving rather than tutorial-based experimentation.

---

## Author
**Mohamed Afreed K**  
B.Tech – Information Technology  
Aspiring Data Scientist
