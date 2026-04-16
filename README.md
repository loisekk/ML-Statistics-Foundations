# 📊 Statistical Foundations for Machine Learning

<div align="center">

![Python](https://img.shields.io/badge/Python-3.13-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebooks-F37626?style=for-the-badge&logo=jupyter&logoColor=white)
![SciPy](https://img.shields.io/badge/SciPy-Statistics-8CAAE6?style=for-the-badge&logo=scipy&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-Arrays-013243?style=for-the-badge&logo=numpy&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-22C55E?style=for-the-badge)

**A structured collection of statistical concepts and hypothesis testing techniques — built as a foundation for Machine Learning and Agentic AI.**

</div>

---

## 🧭 Why This Repository Exists

When I started diving deeper into Machine Learning, I realized one thing — **without a solid understanding of statistics, models are just black boxes.**

This repository is my learning journal. Every notebook here represents a concept I studied, implemented, and documented to truly understand the *why* behind data-driven decision making — not just the how.

> *"Statistics is the grammar of science."* — Karl Pearson

---

## 📁 Repository Structure

```
Statistical-Foundations/
│
├── 📓 Z_TEST.ipynb               # Z-Test: population mean comparison
├── 📓 T_TEST.ipynb               # One-Sample T-Test
├── 📓 two_sample_T-test.ipynb    # Two-Sample T-Test (Welch's)
├── 📓 ANNOVA_Test.ipynb          # One-Way ANOVA
├── 📓 CHI_Square.ipynb           # Chi-Square Test of Independence
├── 📓 Outliers.ipynb             # IQR-Based Outlier Detection
│
└── README.md
```

---

## 🧪 Notebooks Overview

### 🔵 Z-Test — `Z_TEST.ipynb`
Tests whether a **sample mean significantly differs from a known population mean**, when the population standard deviation is known.

- **Dataset:** Synthetic height measurements (n=30)
- **Key formula:** `z = (x̄ − μ) / (σ / √n)`
- **Tools:** `numpy`, `scipy.stats.norm`
- **Result:** Failed to reject H₀ — sample mean not significantly different from population mean (p = 0.171)

---

### 🟢 One-Sample T-Test — `T_TEST.ipynb`
Similar to the Z-Test but used when **population standard deviation is unknown** — more practical for real-world scenarios.

- **Dataset:** Synthetic height sample (n=10)
- **Key formula:** `t = (x̄ − μ) / (s / √n)` with `ddof=1`
- **Tools:** `numpy`, `scipy.stats.t`
- **Result:** Failed to reject H₀ — no significant difference from the hypothesized mean of 170

---

### 🟡 Two-Sample T-Test — `two_sample_T-test.ipynb`
Compares the means of **two independent groups** to determine if they differ significantly (Welch's T-Test, assumes unequal variances).

- **Dataset:** Exam scores of Group A vs Group B
- **Tools:** `scipy.stats.ttest_ind(equal_var=False)`
- **Result:** Rejected H₀ — Group A scored significantly higher than Group B (t = 5.83)

---

### 🟠 One-Way ANOVA — `ANNOVA_Test.ipynb`
Tests whether **three or more groups have significantly different means** — an extension of the T-Test for multiple groups.

- **Dataset:** Titanic dataset — passenger age across 3 ticket classes
- **Tools:** `scipy.stats.f_oneway`, `seaborn`
- **Result:** Rejected H₀ — significant age differences exist across passenger classes (F = 57.44, p ≈ 7.49e-24)

---

### 🔴 Chi-Square Test — `CHI_Square.ipynb`
Tests **independence between two categorical variables** using a contingency table.

- **Dataset:** Titanic dataset — gender vs survival
- **Tools:** `scipy.stats.chi2_contingency`, `pandas.crosstab`
- **Result:** Rejected H₀ — strong statistical relationship between gender and survival (χ² = 260.72)

---

### ⚫ Outlier Detection (IQR Method) — `Outliers.ipynb`
Identifies and removes **statistical outliers** using the Interquartile Range (IQR) fencing method.

- **Dataset:** Custom numerical array with an extreme value (201)
- **Method:** `IQR = Q3 − Q1`, fences at `Q1 − 1.5×IQR` and `Q3 + 1.5×IQR`
- **Tools:** `numpy`, `seaborn.boxplot`
- **Result:** Detected and removed the outlier value (201), visualized via boxplots before and after

---

## 🧠 Concepts Covered

| Area | Topics |
|------|--------|
| **Descriptive Stats** | Mean, Variance, Standard Deviation, Percentiles, IQR |
| **Distributions** | Normal Distribution, T-Distribution, F-Distribution, Chi-Square Distribution |
| **Hypothesis Testing** | H₀ / H₁, p-values, alpha (α), Type I & Type II errors |
| **Statistical Tests** | Z-Test, One-Sample T-Test, Two-Sample T-Test, ANOVA, Chi-Square |
| **Data Cleaning** | Outlier Detection & Removal via IQR Fencing |

---

## 🛠️ Tech Stack

| Library | Purpose |
|---------|---------|
| `numpy` | Numerical computations, array operations |
| `scipy.stats` | Statistical tests and distributions |
| `pandas` | Data manipulation and contingency tables |
| `seaborn` | Dataset loading and boxplot visualization |

---

## ⚙️ Getting Started

```bash
# Clone the repository
git clone https://github.com/loisekk/<repo-name>.git
cd <repo-name>

# Install dependencies
pip install numpy scipy pandas seaborn jupyter

# Launch Jupyter
jupyter notebook
```

---

## 🗺️ What's Next

This statistical foundation is feeding directly into my **AI/ML roadmap**:

```
Statistics ──► ML Models ──► RAG Systems ──► Agentic AI ──► Multi-Agent Systems
```

Currently exploring how statistical reasoning integrates with **Agentic AI** and intelligent decision-making systems.

---

## 👤 Author

**Yash Brahmankar**
B.Tech — Artificial Intelligence & Machine Learning | OIST (2024–2028)

[![GitHub](https://img.shields.io/badge/GitHub-loisekk-181717?style=flat-square&logo=github)](https://github.com/loisekk)
[![Email](https://img.shields.io/badge/Email-yashbrahmankar95@gmail.com-D14836?style=flat-square&logo=gmail&logoColor=white)](mailto:yashbrahmankar95@gmail.com)

---

## 📄 License

This project is licensed under the **MIT License** — feel free to use, share, and build upon it.

---

<div align="center">

*Still learning. Still building. 🚀*

</div>
