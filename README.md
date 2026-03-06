# AI-Driven Freshwater Sustainability Risk Forecasting System

[![Python](https://img.shields.io/badge/python-3.12-blue)](https://www.python.org/)
[![License](https://img.shields.io/badge/license-All%20Rights%20Reserved-red)]()

---

## 🌍 Overview

This project develops a **machine learning framework to predict freshwater stress** globally using environmental and socioeconomic indicators across 25 years (2001–2025).  

The study integrates **feature engineering, dynamic lag modeling, explainable AI (SHAP), scenario analysis, uncertainty quantification, and geospatial visualization** to identify the drivers of freshwater depletion and rank countries by risk.

---

## 🔬 Research Questions

- Can AI accurately predict freshwater stress using multi-source sustainability indicators?  
- Which factors (urbanization, agriculture, industry, rainfall) contribute most to freshwater stress?  
- Can explainable AI provide interpretable insights for decision-makers?  
- How might future socioeconomic and industrial changes impact water stress?

---

## 🧪 Hypotheses

1. Higher urbanization and industrial activity → higher freshwater stress  
2. Agricultural intensity strongly contributes to water stress  
3. Low rainfall / anomalies → increased stress  
4. Dynamic lag features improve predictive performance  
5. Water demand indicators are stronger predictors than climate alone  

---

## 📊 Dataset

- Global panel dataset of **~200 countries** (2001–2025)  
- 10 key indicators:  
  - Water stress  
  - Rainfall / precipitation  
  - Urban population & density  
  - Industrial & agricultural activity  
  - Water demand ratios and interactions  

**Source:** [World Bank Open Data](https://data.worldbank.org/) and other public sustainability datasets.

---

## ⚙ Methodology

1. **Data Preprocessing:** handle missing values, reshape into panel data  
2. **Feature Engineering:** create dynamic lag features, interaction variables  
3. **Machine Learning Models:** Random Forest, XGBoost  
4. **Explainable AI:** SHAP values and feature importance  
5. **Scenario Analysis:** simulate urbanization and industrial growth  
6. **Uncertainty Estimation:** bootstrap confidence intervals  
7. **Geospatial Visualization:** global map and top 20 risk countries  

---

## 📈 Results

### Model Performance

| Model | MAE | R² | Accuracy |
|-------|-----|----|---------|
| Random Forest (Dynamic Lag) | 2.57 | 0.992 | 99.4% |
| Before Lag Features | 52.2 | 0.28 | 78.4% |

**Interpretation:** Incorporating dynamic lag features drastically improved prediction performance.

---

### Top Predicted Freshwater Stress Countries

| Rank | Country | Predicted Stress |
|------|---------|----------------|
| 1 | Kuwait | 3850 |
| 2 | UAE | 1509 |
| 3 | Saudi Arabia | 974 |
| 4 | Libya | 817 |
| 5 | Qatar | 431 |

---

### Key Drivers (SHAP Feature Importance)

| Feature | Mean SHAP |
|---------|------------|
| Previous Year Water Stress | 61.86 |
| Urban Pressure | 2.01 |
| Urban Pressure Lag1 | 1.57 |
| Agricultural Intensity Lag1 | 0.32 |
| Industrial-Urban Interaction | 0.27 |

---

### Global Risk Map

![Global Freshwater Stress Map](results/figures/global_map.png)

- Dark red indicates **high stress**  
- Grey indicates missing/no data

---

### Top 20 High-Risk Countries

![Top 20 Countries](results/figures/top20_bar.png)

---

## 🏆 Project Contributions

- **Systems-level predictive modeling** of freshwater stress  
- **25-year global panel analysis**  
- **Explainable AI (SHAP)** to interpret drivers  
- **Feature engineering** for sustainability indicators  
- **Policy-relevant insights** for water governance  

---

## ⚠ Limitations

- Country-level aggregation may hide sub-national water stress  
- Limited hydrological variables (groundwater, surface water)  
- Predictions assume trends continue as in historical data  

---

## 🔮 Future Work

- Scenario-based forecasting for 2030+  
- Integration of groundwater and surface water datasets  
- Alternative ML models: LightGBM, temporal deep learning  
- Advanced uncertainty and sensitivity analysis  

---

## 💻 Technologies Used

- Python 3.12  
- Pandas, NumPy  
- Scikit-learn, XGBoost  
- SHAP  
- GeoPandas, Matplotlib, Seaborn  

---

## 📄 License

All Rights Reserved.  
Usage requires explicit permission from the author.  
Contact: [meenuhani27@gmail.com]
