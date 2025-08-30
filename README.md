# energy-efficiency-models

## 📚 Project Overview
This project explores a range of **linear and nonlinear regression models** to predict the **Heating Load (Y1)** of buildings using the **Energy Efficiency Dataset (ENB2012)**. The objective is to evaluate how different models handle real-world data, and to analyze the trade-offs between **accuracy, interpretability, and computational efficiency**.

## 📝 Problem Statement
Energy modeling plays a vital role in **sustainable building design**. The aim of this project is to build predictive models for **Heating Load (Y1)** using building features, supporting better energy-efficient architectural decisions.

## 📂 Repository Contents
- `Exploring_Nonlinear_Models_and_Model_Selection.ipynb` → Jupyter Notebook with complete workflow (EDA + models)  
- `screenshots/` → Visualizations and plots  
- `report.pdf` → Detailed project report (optional)  
- `README.md` → Documentation  

## 📦 Dataset
- **Source:** UCI Machine Learning Repository  
- **Dataset:** Energy Efficiency Dataset (ENB2012)  

| Feature | Description |
|---------|-------------|
| X1 | Relative Compactness |
| X2 | Surface Area |
| X3 | Wall Area |
| X4 | Roof Area |
| X5 | Overall Height |
| X6 | Orientation |
| X7 | Glazing Area |
| X8 | Glazing Area Distribution |
| Y1 | Heating Load (*target variable*) |
| Y2 | Cooling Load (*not used in this project*) |

## 🧰 Tools & Technologies
- Python 3.9+  
- pandas, numpy  
- matplotlib, seaborn  
- scikit-learn  

## 🔥 Models Implemented
- **Linear Regression** → Baseline, residual analysis  
- **Polynomial Regression (degree=2)** → Captures nonlinear trends, cross-validation applied  
- **Ridge Regression (α=0.1)** → Regularized linear model  
- **Decision Tree Regressor (pruned)** → Interpretable, provides feature importance visualization  

## ✅ Results Summary
| Model                     | MSE   | RMSE | R²   |
|----------------------------|-------|------|------|
| Linear Regression          | 8.25  | 2.87 | 0.92 |
| Polynomial Regression (d=2)| 0.33  | 0.57 | 1.00 |
| Ridge Regression (α=0.1)   | 8.27  | 2.88 | 0.92 |
| Decision Tree (pruned)     | 0.36  | 0.60 | 1.00 |

**Insights:**  
- Polynomial Regression achieved the **best accuracy** with near-perfect fit.  
- Decision Tree offered **interpretability** with competitive results.  
- Linear & Ridge were **simpler but less accurate**.  

## 📈 Visualizations
- Correlation heatmap  
- Residual plots (linear & polynomial)  
- Residual histogram  
- Predicted vs actual values (polynomial regression)  
- Feature importance chart  
- Decision tree structure  

📸 All visualizations are available in the `/screenshots` folder.

## 💡 Interpretability & Trade-offs
- **Polynomial Regression** → Highly accurate but computationally expensive.  
- **Decision Trees** → Easy to interpret, prone to overfitting (pruned for stability).  
- **Ridge Regression** → Adds regularization but no significant boost over linear regression.  

