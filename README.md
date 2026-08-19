# 🌦️ ATMOS INTELLIGENCE

[![Python](https://img.shields.io/badge/Python-3.x-blue.svg)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)](https://jupyter.org/)
[![Machine Learning](https://img.shields.io/badge/Machine_Learning-Random_Forest-success.svg)](#)

## 📌 Project Overview
Accurate weather forecasting is crucial for various sectors, from agriculture and transportation to disaster preparedness and renewable energy. 

This project implements an end-to-end **Machine Learning Pipeline** to predict specific weather conditions (`condition_text`) by leveraging a rich, multi-dimensional dataset from the World Weather Repository. 

## 📊 Dataset & Features
The model integrates heterogeneous data sources to capture complex environmental patterns. Key feature categories include:

* **📍 Geographic Location:** `country`, `latitude`, `longitude`, `time_zone`
* **🌡️ Meteorological Metrics:** `temperature_fahrenheit`, `humidity`, `uv_index`
* **🌫️ Air Quality Indices (AQI):** `air_quality_Carbon_Monoxide`, `air_quality_us-epa-index`
* **🌔 Astronomical Data:** `sunrise`, `sunset`, `moon_phase`

**Target Variable:** `condition_text` (Categorical label representing the specific weather state, e.g., Sunny, Partly Cloudy, Rain).

## 🧠 Machine Learning Pipeline
The project follows a rigorous data science workflow:

1. **Data Preprocessing & Cleaning:** * Addressed missing values and standardized data formats.
   * Implemented **Outlier Detection** algorithms to remove anomalous readings and improve model robustness.
2. **Feature Engineering:**
   * Applied **Label Encoding** to transform text-based categorical labels (e.g., weather conditions) into machine-readable numerical values.
3. **Model Training (Random Forest):**
   * Selected the **RandomForestClassifier** for its resilience to overfitting and capability to handle non-linear relationships.
   * Configured the ensemble model with **100 decision trees** (`n_estimators=100`) to maximize predictive accuracy through aggregate voting.

## 🛠️ Tech Stack
* **Language:** Python 3
* **Data Manipulation:** Pandas, NumPy
* **Machine Learning:** Scikit-Learn
* **Environment:** Jupyter Notebook

## 🚀 Future Enhancements
* Incorporate Deep Learning architectures (e.g., Neural Networks) for time-series forecasting.
* Deploy the model via a REST API (Flask/FastAPI) for real-time weather prediction inference.

---
*Developed as a demonstration of applied machine learning in environmental data science.*
