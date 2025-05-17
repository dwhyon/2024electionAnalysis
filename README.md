# 2024 U.S. Presidential Election Analysis by County

**Author:** David Hyon   

## Overview

This project analyzes the 2024 U.S. presidential election using county-level data, integrating demographic information, COVID-19 health metrics, and economic indicators. The goal was to explore how historical and contextual variables influenced voting outcomes and to assess the predictive power of different machine learning classification models.

## Abstract

Using a dataset of 3,100 counties and 176 variables, this analysis examined electoral trends with a focus on bellwether counties and swing states. Principal Component Analysis (PCA) and clustering were used for dimensionality reduction and pattern recognition. Classification models including random forest, boosted tree, SVM (linear and radial), decision tree, and LASSO-regularized logistic regression were trained and evaluated. The boosted tree and random forest models achieved the highest F1 and AUC scores, with key predictors including race, education, and COVID-19 mortality rates. Findings suggest that demographic structure and pandemic-related death rates significantly influenced the 2024 election outcome.

## Data Sources

- **Election Data (2008–2024):** County/ward-level vote counts from public news sources.
- **COVID-19 Data:** Opportunity Insights Economic Tracker (e.g., spending, business closures, deaths).
- **Demographics:** 2020 Decennial Census and American Community Survey (ACS).

## Methods

- PCA for dimensionality reduction
- Gaussian Mixture Model clustering using `mclust` (VVV model)
- Classification models:
  - Gradient Boosted Trees (`gbm`)
  - Random Forest
  - Decision Tree
  - LASSO Logistic Regression (`glmnet`)
  - Support Vector Machines (Linear & Radial)

## Key Findings

- **Demographics (Race and Education):** Most important predictors of county-level voting outcomes.
- **COVID-19 Mortality:** Maximum weekly and cumulative death rates were highly predictive.
- **Model Performance:**
  - Boosted Tree: AUC 0.977, F1 0.965
  - Random Forest: AUC 0.972, F1 0.963
  - SVM (Linear): F1 0.966
  - SVM (Radial): AUC 0.280 (underperformed)

## Limitations

- COVID data was aggregated across 2020–2022, limiting temporal resolution.
- Spatial and temporal autocorrelation were not modeled explicitly.
- Additional factors like campaign spending, media exposure, and religion were not included.
- Binary classification limits analysis of vote margins.

## Future Directions

- Incorporate regression models using vote margins instead of binary labels.
- Apply spatial econometrics to capture local dependencies.
- Extend to time-varying panel models with finer temporal granularity.

## References

- Brookings Institution (2024): *Why Donald Trump won and Kamala Harris lost*
- Pew Research Center (2024): *Issues and the 2024 election*
- Reuters (2024): *US presidential election results 2024*
- Al Jazeera (2024): *The Elon Musk effect*
- The Guardian (2025): *Biden and Harris campaign issues*
- World Economic Forum (2022): *Global concern about inflation*
- BBC News (2024): *ANC loses majority in South Africa*

---

> 📁 If you're using this project in a data science or political analysis context, you may cite this work or reference the methodology in similar applications. For full reproducibility, access to the Opportunity Insights dataset and cleaned election data is required.
