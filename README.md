# Student Salary Prediction & Data Validation

**Objective:** Predict student salaries based on academic performance and skills, while validating dataset reliability against real-world market benchmarks.

---

## Business Problem

> Can we accurately predict entry-level salaries for engineering students? And more importantly — is the synthetic dataset we're using representative of the real Indian job market?

This project was completed as a **team project for the BCR Data Science Program**.

---

## My Contribution: Data Validation & Feasibility

Before building any model, I conducted a comprehensive validation to ensure the dataset reflected real-world market conditions.

### Validation Methodology

Compared **6 key metrics** against official sources: *India Skills Report 2026*, *NIE admission data*, and *academic research*.

### Validation Results

| Metric | Dataset Value | Real-World Benchmark | Source | Status |
|---|---|---|---|---|
| Placement Rate | 68.5% | 70.15% | India Skills Report 2026 | ✅ Valid |
| CGPA by Tier | Tier-1: 7.60 / Tier-3: 6.99 | Matches elite admission trends (NIE: 9.5/10 avg) | NIE Official Data | ✅ Valid |
| Branch Hierarchy | CSE (71.3%) > Civil (64%) | CSE (80%) > Civil (55%) | ISR 2026 | ✅ Valid |
| Avg Salary (IT) | 17.31 LPA | 15–25 LPA range | WJEBR Research | ✅ Valid |
| CGPA-Salary Correlation | r = 0.337 | r = 0.36 | IJACECT Study | ✅ Valid |
| Tier-1 Placement Rate | 83.1% | Up to 98% (RNSIT Bangalore) | RNSIT Official | ✅ Valid |

### Conclusion

Dataset validated with **<5% deviation** across all critical metrics. The synthetic data accurately reflects the Indian engineering job market and is suitable for predictive modeling.

### Sources

1. [India Skills Report 2026](https://wheebox.com/assets/pdf/ISR_Report_2026.pdf))
2. [National Institute of Engineering](https://nie.ac.in/)
3. [World Journal of Economics and Business Research](https://upubscience.com/wjebr/article/view/1516)
4. IJACECT Study on Placement Success
5. [RNSIT Bangalore Placement Data](https://www.rnsit.ac.in/blog/top-10-engineering-colleges-in-bangalore/)

---

## Team Project Results

The team tested **9 regression algorithms** to predict salary packages for engineering graduates.

### Best Model Performance

| Model | R² Score | MAPE (Error) |
|---|---|---|
| **LightGBM** | **0.783** | **5.69%** |
| Gradient Boosting | 0.779 | 5.85% |
| Random Forest | 0.760 | 6.01% |
| Linear Regression | 0.773 | 5.77% |

**Selected Model: LightGBM Regressor** — best balance between accuracy (78.3% variance explained) and error rate (5.69%).

### Top Salary Drivers (Feature Importance)

1. 🏢 **Internships** — Strongest positive correlation with salary
2. 💻 **DSA Score** — Technical algorithms skill
3. 🏫 **College Tier** — Institution prestige
4. 🤖 **Machine Learning Knowledge** — Specialized technical skill
5. 📊 **CGPA** — Academic performance

### Key Insight

> The model confirms that **experience beats grades**. Practical experience (internships) and technical skills (DSA, ML) are stronger salary predictors than pure academic performance (CGPA).

---

## Tools Used

- **Python:** pandas, numpy, matplotlib, seaborn
- **Machine Learning:** scikit-learn, LightGBM, SHAP
- **Environment:** Google Colab
- **Validation Sources:** Academic papers, official reports

---

## Repository Structure

```
student-salary-prediction/
│
├── notebooks/
│   ├── 01_data_validation.ipynb
│   └── 02_salary_model.ipynb
│
├── [presentation.pdf](https://canva.link/dws3caum1trwb7p)
└── README.md
```
*Project completed as part of BCR Data Science Program (2026).*
