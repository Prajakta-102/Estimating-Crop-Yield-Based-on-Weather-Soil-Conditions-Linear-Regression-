# 🌾 Crop Yield Prediction using Linear, Ridge & Lasso Regression

## 📌 Project Overview

This project focuses on building a regression model to predict **Crop Yield** using agricultural data. With the help of **Linear, Ridge, and Lasso Regression** techniques, the goal is to aid in effective planning and decision-making for agricultural stakeholders like farmers, suppliers, and policymakers.

---

## 📊 Dataset Description

- **Total Records**: 19,689
- **Features**:
  - `Crop`: Type of crop
  - `Crop_Year`: Year of cultivation
  - `Season`: Season in which crop was grown
  - `State`: Indian state
  - `Area`: Area of land used
  - `Production`: Total crop production
  - `Annual_Rainfall`: Rainfall received annually
  - `Fertilizer`: Quantity of fertilizer used
  - `Pesticide`: Quantity of pesticide used
  - `Yield`: (Target) Crop yield (production per area)

---

## 🔍 Exploratory Data Analysis (EDA)

- Verified dataset shape: `(19689, 10)`
- Data types and null values were checked using `info()`
- Visualized using:
  - Bar plots: Yield vs Crop, Yield vs State
  - Box plots: Outlier detection
  - Correlation heatmap
  - Pairplot: Multivariate relationships

### 📌 Observations:
- No null or missing values
- Strong positive correlations found between yield and factors like fertilizer, rainfall, and pesticide
- Outliers found in production and area columns
- Heatmap revealed multicollinearity between area and production

---

## 🦖 Data Preprocessing

- Encoded categorical variables
- Split data into features `X` and target `y`
- X shape: `(19689, 9)` | Y shape: `(19689,)`
- Applied Train-Test split

---

## 💪 Model Building & Evaluation

### 1️⃣ Linear Regression

- **Mean Absolute Error**: 62.98  
- **Mean Squared Error**: 158,461.95  
- **Root Mean Squared Error**: 398.07  
- **R-Squared Score**: 0.8022

#### ✅ Cross-Validation:
- `Mean R2 = 0.851616`
- `Std Dev = 0.026554`

---

### 2️⃣ Ridge Regression

- **Best Alpha**: 0.1  
- **Ridge Regression R2 Score**: 0.85

---

### 3️⃣ Lasso Regression

- **Best Alpha**: 0.1  
- **Lasso Regression R2 Score**: 0.85  
- Lasso also helped reduce overfitting and confirmed the strength of linear features.

---

## 🔍 Model Comparison

| Model              | MAE    | MSE        | RMSE   | R² Score |
|-------------------|--------|------------|--------|----------|
| Linear Regression | 62.98  | 158,461.95 | 398.07 | 0.8022   |
| Ridge Regression  |   -    |     -      |   -    | 0.85     |
| Lasso Regression  |   -    |     -      |   -    | 0.85     |

📌 *(Values for Ridge and Lasso errors can be updated if available)*

---

## 🔺 Final Conclusion

- Linear models performed well due to strong linear relationships in the data.
- Ridge and Lasso regularization helped improve the model’s generalization and reduce overfitting.
- Similar performance between Ridge and Lasso indicates robust linear trends and clean feature contributions.
- The final model with regularization (R² = 0.85) can be reliably used for:
  - Government agricultural forecasting
  - Farm-level decision-making
  - Crop planning and fertilizer management

---

## 🛠️ Tech Stack Used

- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn

---

## 📁 Files Included

- `LR_crop_new.ipynb` - Notebook with EDA, preprocessing, model building, and tuning
- `README.md` - GitHub summary

---

## ⭐ Features

- End-to-end regression project using real agricultural data
- Includes EDA, data cleaning, encoding, model tuning, and visualization
- Highlights feature correlation and multicollinearity handling
- Applies and compares Linear, Ridge, and Lasso Regression techniques
- Cross-validation implemented for model robustness

---

## 👩‍💻 Author

**Prajakta More**  
EXTC Engineer | Data Analyst | Aspiring Data Scientist  
Power BI, Tableau & Python Enthusiast  
Turning data into insights with ML, SQL, Excel & storytelling

---
