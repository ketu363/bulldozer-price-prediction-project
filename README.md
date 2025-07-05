# 🏗️ Bulldozer Price Prediction

This project predicts the sale prices of used bulldozers using historical and temporal data. It's based on the Kaggle competition [“Blue Book for Bulldozers”](https://www.kaggle.com/competitions/bluebook-for-bulldozers). The dataset is sourced from auction-based records with a focus on forecasting future prices based on machine usage and configuration.

---

## 📌 Problem Statement

Many construction equipment auctions take place each year, but pricing heavy equipment is challenging due to its diverse usage history, specifications, and age. The goal of this project is to build a regression model that can predict a bulldozer's **sale price** given its features and **the date of sale**.

---

## 📁 Dataset

The dataset consists of:
- **Training data**: Historical auction data with features like machine ID, model, year, usage hours, sale date, etc.
- **Test data**: Data without target (sale price) to be predicted.
- **Data files**:
  - `Train.csv`
  - `Valid.csv` / `Test.csv`
  - `TrainAndValid.csv`
  - `Machine_Appendix.csv`
  - `Data_Dictionary.xlsx`

---

## 🧠 ML Approach

- **Type**: Regression problem
- **Model used**: Random Forest Regressor
- **Evaluation Metric**: RMSLE (Root Mean Squared Log Error)

---

## 🔧 Tools & Libraries

- Python 3.10+
- Jupyter Notebook
- Pandas & NumPy
- Scikit-learn
- Matplotlib & Seaborn
- XGBoost (optional)
- Missingno (for null value visualization)
- `dateutil` for parsing dates
- `joblib` for model persistence

---

## 📊 Features Engineering

Key preprocessing steps:
- Convert dates to `datetime` objects
- Extract useful time-based features (year, month, day)
- Encode categorical variables using label encoding
- Fill or drop missing values based on strategy
- Remove unnecessary or high-cardinality features

---

## 🧪 Model Evaluation

- Used `cross_val_score` with RMSLE
- Final RMSLE on validation data was **≈ 0.25**
- Feature importance was analyzed to determine which inputs most affect price

---

## 🔍 Key Learnings

- Real-world data is messy: date formats, missing values, outliers
- Feature engineering and domain understanding improve performance more than tuning alone
- Time-aware modeling is critical for price prediction
- Evaluation metrics like RMSLE are essential when the target has a wide range

---

✅ Status
✅ Completed core implementation
🔜 Potential improvements:

Add more time-series modeling (XGBoost, LightGBM)

Deploy model using FastAPI or Streamlit

## 🙋‍♂️ Author

**Nishant Ketu**  
_M.Tech in Data Science, IIT Jodhpur_  
[LinkedIn](www.linkedin.com/in/nishant-ketu-388a04152 | [GitHub](https://github.com/ketu363)
