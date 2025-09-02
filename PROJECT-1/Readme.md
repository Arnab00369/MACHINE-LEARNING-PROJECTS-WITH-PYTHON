<!-- Banner (capsule-render image is external and works on GitHub) -->
<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:00c6ff,100:0072ff&height=200&section=header&text=Medical%20Insurance%20Cost%20Analysis%20%26%20Forecasting&fontSize=36&fontColor=ffffff&animation=fadeIn&fontAlignY=40" alt="banner" />
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Notebook-Jupyter-orange?logo=jupyter" alt="notebook" />
  <img src="https://img.shields.io/badge/Language-Python-blue?logo=python" alt="python" />
  <img src="https://img.shields.io/badge/Environment-Google%20Colab-lightgrey?logo=googlecolab" alt="colab" />
  <img src="https://img.shields.io/badge/Libraries-pandas%20%7C%20NumPy%20%7C%20scikit--learn%20%7C%20Seaborn-green" alt="libs" />
  <img src="https://img.shields.io/badge/Status-Complete-success" alt="status" />
</p>

---

# 🩺 **Medical Insurance Cost Analysis & Forecasting**
**A focused, production-ready Jupyter Notebook** that predicts health insurance charges using demographic and lifestyle features and demonstrates model development, validation, and interpretation.

> **One-liner:** Predict insurance charges (target `charges`) using features like **age, sex, bmi, children, smoker, region** — with explainable models, visual EDA, and actionable insights.

---

## 🔎 Quick repo highlights (what recruiters care about)
- **Data-driven problem**: Predict insurance charges to assist in premium-setting and risk analysis.
- **Clean pipeline**: Data cleaning → EDA → Feature engineering → Modeling → Evaluation → Interpretation.
- **Models used**: Linear Regression, Polynomial Regression, (optionally) Tree-based baseline & ensemble mention.
- **Metrics reported**: MAE, RMSE, R².
- **Tools**: Python, pandas, NumPy, scikit-learn, Seaborn, Matplotlib, Google Colab.
- **Deliverables**: Jupyter Notebook (`Medical_Insurance_Data_Analysis_and_Forecasting.ipynb`), visuals (`assets/*.png`), README (this file).

---

## 📁 Repository structure
| File / Folder | Purpose |
|---|---|
| `Medical_Insurance_Data_Analysis_and_Forecasting.ipynb` | Main notebook (run this to reproduce results) |
| `assets/` | Plots & screenshots used in README (`eda_age_bmi.png`, `model_residuals.png`, etc.) |
| `requirements.txt` | Python dependencies to reproduce environment |
| `README.md` | This file — polished project summary for recruiters |
| `LICENSE` | Project license (e.g., MIT) |

---

## 🧾 Dataset (source & schema)
**Source:** Kaggle (Medical Insurance dataset) — link in the notebook.  
**Typical columns (used in this notebook):**

| Column | Type | Description |
|---:|---|---|
| `age` | int | Age of primary beneficiary |
| `sex` | categorical | Male / Female |
| `bmi` | float | Body Mass Index — numeric |
| `children` | int | Number of children covered by health insurance |
| `smoker` | categorical | Yes / No |
| `region` | categorical | e.g., southwest, southeast, northwest, northeast |
| `charges` | float | Yearly medical insurance charges (target variable) |

---

## 🚦 Project Workflow (what I did — one line per step)
1. **Load dataset** (CSV) and quick sanity checks (`.head()`, `.info()`, `.describe()`).
2. **Data cleaning**: Convert datatypes, handle duplicates, check missing values.
3. **Feature engineering**: One-hot encode categorical variables (`sex`, `smoker`, `region`); create BMI categories or `age_group` if helpful.
4. **Exploratory Data Analysis (EDA)**: distributions, pairplots, correlations, boxplots for outliers.
5. **Modeling**:
   - Baseline: Mean predictor.
   - Linear Regression (OLS).
   - Polynomial Regression (degree 2 or tuned).
   - (Optional) Tree-based model for nonlinear baseline (e.g., RandomForestRegressor).
6. **Evaluation**: Train/test split (typical 80/20), metrics (MAE, MSE, RMSE, R²), residual plots.
7. **Interpretation**: Feature importance, coefficients, partial dependence (if used).
8. **Conclusions & Future scope**.

---

## 📊 Key EDA & Visuals
> Replace the `assets/*.png` with the actual exported images from your notebook.

<p align="center">
  <img src="assets/eda_age_bmi.png" width="380" alt="age bmis" />
  <img src="assets/charges_v_smoker.png" width="380" alt="smoker charges" />
</p>

**Insights from EDA (examples — update with your exact notebook findings):**
- **Smoker vs Non-smoker:** Smokers have dramatically higher median charges (visualized via boxplot).
- **BMI correlation:** Positive correlation between `bmi` and `charges` with notable outliers.
- **Age effect:** Charges increase with age; older groups show higher variance.
- **Children:** small positive contribution; check interaction with smoking & BMI.

---
