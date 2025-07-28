#  Sales Performance Analysis — Exploratory Data Analysis & Machine Learning

This project performs a complete **Exploratory Data Analysis (EDA)** and builds a **sales prediction model** using a cleaned and feature-engineered version of the *Global Superstore* dataset.

---

##  Project Objective

- Analyze sales data to uncover patterns, trends, and actionable business insights.
- Build a predictive model to estimate **Sales** using features like **Profit**, **Discount**, **Category**, **Region**, **Days to Ship**, etc.
- Improve model accuracy using **advanced feature engineering**, **hyperparameter tuning**, and **tree-based regressors**.

---

##  Dataset Overview

Dataset: `Sales_Superstore.csv`  
Source: Kaggle / Global Superstore  
Features include:

- Order Date, Ship Date
- Category, Sub-Category, Region
- Sales, Profit, Discount, Quantity
- Customer and Product details

---

##  Tasks Performed

###  Data Cleaning
- Removed duplicates and missing values
- Handled outliers using **IQR method**
- Encoded categorical features using **One-Hot Encoding**
- Removed high-cardinality features like Customer Name and Product Name

###  Feature Engineering
- Extracted:
  - `Order Year`, `Order Month`, `Order Weekday`
  - `Is Weekend`
  - `Days to Ship` (calculated from Order and Ship Dates)
- Created interaction terms: `Profit * Discount`, `Quantity * Discount`

###  Exploratory Data Analysis (EDA)
- **Heatmap** of feature correlation
- **Histograms** & **boxplots** for numerical features
- **Sales trends over time**
- **Bar charts** for Region-wise and Category-wise performance
- **Scatter plot**: Profit vs Discount

---

##  Modeling

###  Models Used
- **Linear Regression** (baseline)
- **Random Forest Regressor** (tuned)
- **XGBoost Regressor**
- **LightGBM Regressor**
- **Ensembled predictions**

###  Performance Metrics
- **R² Score**: ~0.67 (Random Forest tuned)
- **MSE**: Low and stable
- **Log-transformation** applied to improve predictions on skewed targets
- **Hyperparameter tuning** using `RandomizedSearchCV`

---

## 📈 Key Insights

- 🚚 **Days to Ship** slightly affects Sales but varies across segments.
- 🔻 **High discounts reduce Profit** after a threshold.
- 🌍 **West and East regions** contribute the most to Sales.
- 🛍️ **Technology and Office Supplies** categories perform best.
- 📦 Faster delivery boosts repeat customer segments.

---

## 📦 Deliverables

- `Sales_Analysis_Task_2.ipynb` – Full analysis and model training
- `README.md` – Summary of the entire project
- Optional (if added):
  - `sales_predictions.csv` – Predictions from the model
  - `sales_prediction_model.pkl` – Saved model
  - PDF/HTML export of report

---

## 🛠 Tools Used

- **Python**, **Pandas**, **NumPy**
- **Matplotlib**, **Seaborn**
- **Scikit-learn**
- **XGBoost**, **LightGBM**

---

## 📚 How to Run

1. Clone the repo or open the notebook in Google Colab
2. Upload `Sales_Superstore.csv`
3. Run the notebook cell-by-cell
4. Adjust hyperparameters in tuning cell if desired
5. View the final predictions and evaluation metrics

---

## ✨ Future Improvements

- Deploy as a Flask or Streamlit app
- Add cross-validation with time-based splits
- Integrate external factors like holiday seasons or marketing campaigns
- Use SHAP for feature interpretability

---

## 🧑‍💻 Author

**Riyan Ozair**  
B.E AI & DS | Data Analyst | Machine Learning Enthusiast

---

> “Data is the new oil, but insight is the engine.” 🔍
