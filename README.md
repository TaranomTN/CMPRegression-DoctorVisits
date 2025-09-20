# 🩺 CMPRegression-DoctorVisits

> **Regression analysis of doctor visit counts using Conway-Maxwell-Poisson (CMP) distribution — outperforming Poisson and ZIP models in real healthcare data.**

> **تحلیل رگرسیونی تعداد ویزیت‌های پزشکی با توزیع کانوی-مکسول-پواسون (CMP) — عملکرد بهتر نسبت به مدل‌های پواسون و ZIP در داده‌های واقعی سلامت.**

![Python 3.8+](https://img.shields.io/badge/Python-3.8%2B-blue)
![Jupyter Notebook](https://img.shields.io/badge/Jupyter-%23f37621.svg?logo=jupyter&logoColor=white)
![License: MIT](https://img.shields.io/badge/License-MIT-green)

---

## 🇺🇸 English Version

### 📌 Overview

This project implements and compares **three count regression models** — Poisson, Zero-Inflated Poisson (ZIP), and Conway-Maxwell-Poisson (CMP) — to model the number of doctor visits using real-world healthcare data.

The **CMP distribution** is particularly useful for modeling **over-dispersed or under-dispersed count data**, which is common in medical datasets where variance ≠ mean (violating Poisson assumptions).

---

### 🎯 Objective

- Fit count regression models to predict doctor visit frequency.
- Compare model performance using **NLL, MSE, RMSE, MAE**.
- Demonstrate the superiority of CMP in handling dispersion issues.

---

### 📊 Model Performance Comparison

| Model   | NLL         | MSE        | RMSE       | MAE        |
|---------|-------------|------------|------------|------------|
| Poisson | 3753.391119 | 0.602192   | 0.776011   | 0.452129   |
| ZIP     | 3550.806396 | 0.832637   | 0.912490   | 0.743798   |
| **CMP** | **3518.177246** | **0.421156** | **0.783904** | **0.421156** |

✅ **Key Findings**:
- **CMP achieves the lowest NLL**, indicating better probabilistic fit.
- **Lowest MSE and MAE** → more accurate predictions.
- ZIP improves over Poisson but still underperforms compared to CMP.
- This confirms that **CMP is more flexible and robust** for real-world count data with dispersion.

---

### 🧠 Why CMP?

Traditional Poisson regression assumes **mean = variance** — a condition rarely met in healthcare data (e.g., many patients have 0 visits, some have many → overdispersion).

- **ZIP** handles excess zeros, but still assumes Poisson within non-zero part.
- **CMP** generalizes Poisson by introducing a dispersion parameter **ν (nu)**, allowing it to model both over- and under-dispersion.

---
