#  House Price Prediction

A machine learning project that predicts house prices based on key property features using three different ML models - Linear Regression, Random Forest, and Gradient Boosting.

---

##  Project Overview

This project uses a real-world housing dataset of **545 houses** to build and compare ML models that can predict the price of a house based on its features such as area, number of bedrooms, bathrooms, stories, amenities, and more.

---

## 📂 Project Structure

```
House-Price-Prediction/
│
├── Housing.csv                      # Dataset
├── House_Price_Prediction.ipynb     # Jupyter Notebook (main project)
└── README.md                        # Project documentation
```

---

##  Dataset

| Property | Details |
|----------|---------|
| Source | Housing.csv |
| Rows | 545 |
| Columns | 13 |
| Target | `price` |
| Missing Values | None |

### Features

| Feature | Type | Description |
|---------|------|-------------|
| `area` | Numerical | Area of the house (sq ft) |
| `bedrooms` | Numerical | Number of bedrooms |
| `bathrooms` | Numerical | Number of bathrooms |
| `stories` | Numerical | Number of stories |
| `mainroad` | Categorical | Connected to main road (yes/no) |
| `guestroom` | Categorical | Has guest room (yes/no) |
| `basement` | Categorical | Has basement (yes/no) |
| `hotwaterheating` | Categorical | Has hot water heating (yes/no) |
| `airconditioning` | Categorical | Has air conditioning (yes/no) |
| `parking` | Numerical | Number of parking spaces |
| `prefarea` | Categorical | Located in preferred area (yes/no) |
| `furnishingstatus` | Categorical | Furnished / Semi-furnished / Unfurnished |

---

## ⚙️ Tech Stack

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?logo=pandas)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-ML-F7931E?logo=scikit-learn)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-blue)
![Seaborn](https://img.shields.io/badge/Seaborn-Visualization-9cf)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter)

---

##  Project Workflow

```
Load Data  →  EDA  →  Preprocessing  →  Train/Test Split  →  Train Models  →  Evaluate  →  Predict
```

1. **Load Data** — Import and explore the dataset
2. **EDA** — Visualize price distribution, correlations, and feature relationships
3. **Preprocessing** — Encode categorical features (`yes/no` → `1/0`, ordinal encoding for furnishing status)
4. **Train/Test Split** — 80% training, 20% testing
5. **Model Training** — Train 3 ML models
6. **Evaluation** — Compare using R², RMSE, and MAE
7. **Prediction** — Predict price for new house inputs

---

##  Models & Results

| Model | R² Score | RMSE | MAE |
|-------|----------|------|-----|
| Linear Regression | 0.6495 | 1,331,071 | 979,680 |
| Random Forest | 0.6128 | 1,398,901 | 1,024,081 |
| **Gradient Boosting** ✅ | **0.6652** | **1,300,896** | **963,191** |

>  **Best Model: Gradient Boosting** with R² = **0.6652**

---

##  Feature Importance

Based on Random Forest analysis, the most influential features are:

1.  **area** — Strongest predictor of house price
2.  **bathrooms** — Second most important feature
3.  **stories** — Third most important feature

---

## 🔮 Sample Prediction

```python
predict_price(
    area=5000, bedrooms=3, bathrooms=2, stories=2,
    mainroad='yes', airconditioning='yes',
    parking=1, furnishingstatus='semi-furnished'
)
# Output → Predicted Price: 6,381,592 (6.38 Million)
```

---



## 📈 Visualizations Included

- Price Distribution Histogram
- Price vs Area Scatter Plot
- Feature Correlation Heatmap
- Model R² Comparison Chart
- Feature Importance Bar Chart
- Actual vs Predicted Plot
- Residual Plot

---

## 📜 License

This project is open source and available under the [MIT License](LICENSE).
