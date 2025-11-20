# Blood Pressure Medication Comparison

## Overview
This project presents a statistical analysis of a clinical trial comparing the efficacy of three antihypertensive medications: **Ramipril**, **Lisinopril**, and **Moexipril**. The study evaluates the reduction in Systolic Blood Pressure (SBP) across 12 participants to identify the most effective treatment while controlling for baseline variability.

## Study Design & Data
* **Subjects:** 12 participants randomized into 3 treatment groups (n=4 per group).
* **Variables:** Treatment type, Baseline SBP (pre-treatment), and Post-treatment SBP.
* **Primary Outcome:** Absolute reduction in SBP (mmHg) and percent reduction.

## Methodology
The analysis was conducted using **R (v4.5.1)**. The primary statistical approach was an **Analysis of Covariance (ANCOVA)** to adjust for baseline blood pressure differences.

### Statistical Workflow:
1.  **Exploratory Data Analysis (EDA):** Visualized individual SBP changes using paired line plots and summarized descriptive statistics.
2.  **Randomization Check:** Performed permutation tests to ensure group balance.
3.  **Model Selection:**
    * Tested for interaction effects between baseline SBP and drug type.
    * Adopted a main effects ANCOVA model.
4.  **Assumption Verification:**
    * **Normality:** Shapiro-Wilk test.
    * **Homoscedasticity:** Levene’s test.
    * **Outliers:** Checked using Cook’s distance.
5.  **Post-hoc Analysis:** Pairwise comparisons were conducted using **Tukey’s HSD** to control for Type I error.

### Key Libraries
* `car` (ANCOVA & diagnostics)
* `emmeans` (Estimated marginal means & contrasts)
* `ggplot2` (Visualization)
* `dplyr` & `kableExtra` (Data manipulation & reporting)

## Key Findings
* **Overall Effect:** There was a statistically significant difference in post-treatment SBP between the drug groups after adjusting for baseline levels.
* **Drug Efficacy:**
    * **Moexipril** demonstrated the greatest reduction in SBP.
    * **Moexipril** significantly outperformed **Ramipril**.
    * No statistically significant difference was found between Lisinopril and the other two medications.


---
*Note: This analysis is based on a small sample size (n=12) and should be interpreted as a preliminary exploration.*
