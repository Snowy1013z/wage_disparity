# 👩‍💼 Gender Wage Disparity: Analyzing Inequities in Income Across the U.S. Labor Market

**Tools:** Python | Pandas | NumPy | Scikit-learn | Statsmodels | Seaborn | Matplotlib | Lasso Regression

This project investigates wage disparities between genders using 2021 U.S. Census data. By applying multiple regression models and feature selection techniques, we examine how gender, occupation, age, and other factors contribute to income inequality. The study reveals statistically significant gaps and provides actionable recommendations for both employees and employers.

---

## 🔍 Methodology

- **Data Source:** 2021 U.S. Census
- **Data Cleaning:**
  - Removed irrelevant columns (e.g., weight, citizenship, marriage status)
  - Removed NaNs and duplicates
  - Mapped occupation codes (`OCCSOC`) into named sectors
- **Feature Engineering:**
  - One-hot encoded categorical variables (e.g., gender, occupation)
  - Transformed wage to log scale: `log(Wage)`
- **Modeling Approaches:**
  - `log(Wage) ~ SEX` — Baseline model (R² ≈ 2.2%)
  - `log(Wage) ~ SEX * Occupation` — (R² ≈ 1.8%)
  - `log(Wage) ~ SEX * Age` — (R² ≈ 2.0%)
  - Final Model: Lasso regression with selected variables (R² ≈ 4.0%)

---

## 📌 Project Highlights

- After adjusting for **occupation, age, education, hours worked, and state**, being **male is associated with ~$19,100 higher income** compared to females.
- Despite controls, **gender remains a statistically significant predictor of wage**.
- Applied Lasso regression for variable selection and regularization, improving model interpretability.

---

## 💡 Insights & Recommendations

### Occupation
- **Employees:** Focus on personal skill development and consider switching to high-paying industries.
- **Employers:** Reevaluate talent acquisition and promotion strategies to support equitable outcomes.

### Location
- **Employees:** Explore remote work or relocation to higher-paying areas.
- **Employers:** Consider adjusting pay based on regional cost-of-living differences.

---

## 🧩 Limitations

- The dataset was **not designed for causal inference**, limiting generalizability.
- **Possible omitted variables** (e.g., job level, company size, negotiation skills).
- Census data relies on **self-reporting**, introducing potential bias.
- Model assumptions may oversimplify nonlinear relationships.

---

## 📁 Deliverables

- `Wage_Disparity - LMU Case Comp.pdf`: A PPT used to present infont of judges 
- Visualizations: Wage vs. gender, occupation-adjusted income, regional wage comparisons

---

## 🚀 Future Directions

- Promote **wage transparency** at organizational and industry levels
- Use more granular and updated datasets (e.g., company payroll, IRS records)
- Enhance model complexity to account for **interaction effects and non-linearity**
