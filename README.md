# 🛡️ Actuarial Risk Engine — Modeling Environmental Shifters of Health Insurance Costs

## 📖 Project Overview
Traditional health insurance underwriting often relies on static demographic buckets (Age, Gender). This project modernizes the risk assessment process by integrating **climatological centroids** with a **228,711-record health insurance portfolio** (2017–2019). 

The goal is to quantify how regional weather patterns—such as **UV Index, Wind, and Temperature**—influence human medical claim severity and frequency.

## 🚀 Key Technical Features
* **Actuarial Distribution:** Implemented a **Tweedie Regressor** (Compound Poisson-Gamma) to handle zero-inflated, long-tailed claim data.
* **Feature Engineering:** Developed custom retention metrics (`is_active`) and socio-economic feature mappings from raw insurance codes.
* **Climate Integration:** Merged policyholder data with regional weather centroids across 6 distinct geographic clusters.

* **Machine Learning Pipeline:** Built a robust pipeline utilizing `StandardScaler` and `GridSearchCV` for hyperparameter optimization.
* **Statistical Validation:** Utilized **Mutual Information Regression** to rank features by their "Information Gain" and prevent data leakage from post-event variables.

## 📊 Results & Insights
* **Primary Driver:** Age remains the strongest predictor (Standardized Weight: **0.480**).
* **Environmental Shifters:** Identified an inverse correlation between **Temperature/UV Index** and claim costs, while **Wind Speed** was revealed as a positive risk driver.

* **Optimization:** Achieved an optimal **Tweedie Power of 1.9**, indicating a severity-heavy distribution rather than a frequency-heavy one.

## 🛠️ Tech Stack
* **Languages:** Python 3.12
* **Libraries:** `scikit-learn`, `pandas`, `numpy`, `seaborn`, `matplotlib`, `joblib`
* **Techniques:** Generalized Linear Models (GLM), Hyperparameter Tuning, Cross-Validation, Z-score Normalization.
