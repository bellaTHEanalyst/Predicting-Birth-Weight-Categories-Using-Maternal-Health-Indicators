# Predicting Birth Weight Categories Using Maternal Health Indicators

**Author:** Isabella Martins Iwuala  
**Course:** MATH 5383: Predictive Analytics  

---

## Overview

This project analyzes maternal health factors to predict newborn birth weight categories (Low/Normal) using regression modeling techniques. The analysis uses data from 200 maternal records to identify key predictors of birth outcomes.

## Dataset

**Source:** [Maternal Health Features Dataset (Kaggle)](https://www.kaggle.com/datasets/ziya07/maternal-health-features-dataset)

**Variables:**
- **Response:** Birth weight category (Low = 0, Normal = 1)
- **Predictors:** Age, BMI, gestational age, blood pressure, hemoglobin level, prenatal visits, household income, diabetes, hypertension, smoking status, alcohol consumption, education level, iron supplementation

**Dataset Characteristics:**
- 200 observations, no missing values
- 80% normal weight, 20% low birth weight
- All categorical variables encoded numerically

## Key Findings

### Simple Linear Regression
- **Gestational age** emerged as the strongest predictor
- Regression equation: `ŷ = -1.822 + 0.070 × Gestational Age`
- Each additional week of gestation increases probability of normal birth weight by ~7%
- Explained ~8.8% of variability in outcomes

### Multiple Linear Regression
- **Primary predictor:** Gestational age (p < 0.001)
- **Secondary predictors:** Hemoglobin level and number of prenatal visits
- **Non-significant:** BMI and systolic blood pressure (when controlling for other variables)
- VIF values: 1.02–1.06 (no multicollinearity concerns)
- Improved model fit over simple regression

### Statistical Summary

| Variable | Mean | SD | Range |
|----------|------|----|----|
| Age (years) | 30.1 | 6.8 | 18–44 |
| Gestational Age (weeks) | 37.5 | 1.2 | 35–40 |
| Hemoglobin (g/dL) | 11.5 | 1.3 | 8.3–14.7 |
| Prenatal Visits | 5.6 | 2.1 | 0–11 |
| Pre-pregnancy BMI | 25.6 | 4.2 | 11.7–38.7 |

## Conclusions

1. **Gestational age** is the primary determinant of birth weight category
2. **Maternal hemoglobin levels** and **prenatal care utilization** play secondary but meaningful roles
3. Model diagnostics confirmed assumptions of linearity, independence, normality, and homoscedasticity
4. Results suggest potential for public health interventions focused on maternal health and antenatal care

## Limitations & Future Work

- Small sample size (n = 200)
- Binary outcome may oversimplify birth weight categories
- Potential extensions:
  - Logistic regression for categorical outcomes
  - Interaction effects (e.g., gestational age × maternal health status)
  - Validation on larger, more diverse datasets

## Repository Contents

- 📄 **Full Report:** [Project_Report.pdf](./Project_Report.pdf)
- 📊 **Analysis Code:**
  - [Data Preprocessing & EDA](https://colab.research.google.com/drive/11-tNohJVUfhgq_Y_kMLwJ41x7wRlEYL8?usp=sharing)
  - [Simple Linear Regression](https://colab.research.google.com/drive/1_HpIlLUMva-J6deLUBgaVS_ktr8MbCDK?usp=sharing)
  - [Multiple Linear Regression](https://colab.research.google.com/drive/1dn0objURvTS2pfnG9niJiIkfgUXF9UtB?usp=sharing)

## Technologies Used

- **Language:** R
- **Platform:** Google Colab
- **Methods:** Linear Regression, VIF Analysis, Correlation Analysis
- **Visualization:** Heatmaps, Boxplots, Regression Diagnostics

---

**For detailed methodology, statistical tables, and visualizations, please refer to the full PDF report.**
