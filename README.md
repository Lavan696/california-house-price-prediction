# California Housing Price Prediction (scikit-learn Dataset)

## Project Overview
This project focuses on predicting **median house values in California** using the **California Housing dataset provided by scikit-learn** (`fetch_california_housing`).  
 **Note:** This is **not the original California Housing dataset**, but a **processed version provided by scikit-learn** for educational and research purposes.

Demonstrates a complete end-to-end regression workflow, including data exploration, feature analysis, model training, evaluation, and interpretation—using a reliable ensemble method on a real-world housing dataset.
The target variable represents **median house value expressed in units of \$100,000**.

A **Random Forest Regressor** was trained and evaluated using robust cross-validation and multiple regression metrics.

---

## Dataset Details
- **Source:** `sklearn.datasets.fetch_california_housing`
- **Number of Features:** 8
- **Target:** Median house value (in \$100,000s)

---

## Key Exploratory Insights
- **Median Income (`MedInc`)** shows a **strong positive correlation (≈ 0.69)** with the target variable, making it the most influential feature.
- Some features exhibited **right-skewed distributions**.
- Applying **log-transformations** to selected features made their distributions **closer to Gaussian**, which helps improve model stability and learning behavior.
- Geographic features (latitude & longitude) reveal clear spatial patterns in house pricing.

---


## Model Performance

| Metric                      | Value         |
|-----------------------------|---------------|
| Cross-Val Mean Score ± std  | 0.506 ± 0.014 |
| RMSE                        | 0.504         |
| MAE                         | 0.327         |
| R² Score                    | 0.8055        |

✅ The model explains **~80% of the variance** in median house prices, indicating strong predictive performance.

---

## Visualizations Included
- Feature correlation heatmap  
- Correlation of features with target  
- Scatter plots (Actual vs Predicted)  
- Residuals vs Predicted values  
- Distribution plots (original vs log-transformed features)  
- Geographic visualization of house values across California  

These visualizations help validate assumptions, detect patterns, and interpret model behavior.

---
## Tech Stack

- Python
- NumPy, Pandas,Matplotlib, Seaborn
- scikit-learn

---

I also included markdown explanations for every major code cell to clearly describe the purpose of each step and make the workflow easier to understand.

---
## Model Persistence
The trained **Random Forest Regressor** was saved using `joblib` for reuse and deployment:
`python
joblib.dump(model, "california_housing_random_forest.pkl")`

---

##  Author  

**Lavan Kumar Konda**  
-  Student at NIT Andhra Pradesh  
-  Passionate about Data Science, Machine Learning, and AI  
-  [LinkedIn](https://www.linkedin.com/in/lavan-kumar-konda/)
