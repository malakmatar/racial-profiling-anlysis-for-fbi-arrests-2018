# Racial Profiling — FBI Arrests by Race (2018) Analysis

## Project overview
This repository contains an exploratory data analysis (EDA) group project for the Data Managment course in Sapienza investigating the question:

> **Are certain races associated with certain crimes?**

Using the **FBI “Arrests by Race and Ethnicity” (2018)** dataset (12,212 reporting agencies; estimated population 247,752,415), we:
- clean and restructure the data for analysis,
- compare **juvenile (Under 18)** vs **adult (Over 18)** arrest patterns,
- compute **marginal proportions** and **conditional probabilities** to study association,
- visualize results with bar plots, heatmaps, and bipartite graphs,
- summarize notable associations and limitations.

This work is presented in the accompanying slides.

---

## Data
**Source:** FBI — *Arrests by Race and Ethnicity (2018)* (UCR program extract).

**Structure used in the analysis:**
- two age groups: **Under 18** and **Over 18**
- **5 race categories**
- **28 offense categories**

> Note: these data are *arrest counts*, not convictions, and are influenced by enforcement, reporting practices, and exposure/opportunity factors.

---

## Methods (what we compute)
### 1) Initial descriptive analysis
- overall shares of arrests by race within selected categories (e.g., murder, violent crimes)
- broad comparisons between juveniles and adults

### 2) Association via probabilities
For each offense category:
- **Marginal proportion**:  
  \( P(\text{offense}) \) — how common the offense is overall.
- **Conditional probability**:  
  \( P(\text{offense} \mid \text{race}) \) — how common the offense is *within a race group*.

We flag “associations” where the conditional probability is meaningfully higher than the marginal proportion for that offense (see slides for the specific comparisons and outputs).

---

## Visualizations included
- **Proportion-by-offense bar charts** (race distribution within each offense)
- **Heatmap** of proportions across offenses × races
- **Bipartite graphs** (race ↔ offense) for Under 18 and Over 18
- **Histogram-style comparisons** for violent vs property crimes

---

## Key observations
From the presented outputs:
- Some offense types show stronger concentration by race in the conditional-probability comparisons.
- The pattern differs between **Under 18** and **Over 18** for several offenses.
- The project emphasizes that statistical association in arrest data **does not imply causation**.

