# Machine Learning & Statistical Analysis in R

A collection of R Markdown projects on statistics, forecasting and machine learning, ranging from exploratory data analysis to classifier ensembles. Each folder holds a self-contained analysis that knits into a full report with code, output and plots.

![R](https://img.shields.io/badge/R-276DC3?logo=r&logoColor=white) ![R Markdown](https://img.shields.io/badge/R%20Markdown-knitr-blue)

## 📚 Projects

| Project | What it does | Methods | Rendered |
| :--- | :--- | :--- | :--- |
| [Getting to Know R](<Getting%20to%20Know%20R/>) | Exploratory analysis of flight delays and night-flight patterns | Data wrangling, feature engineering | — |
| [Statistical Analysis of the Characteristics of White Wines](<Statistical%20Analysis%20of%20the%20Characteristics%20of%20White%20Wines/>) | Filtering and a custom "Swill Index" on 4,800+ white wines | Data frames, derived features | — |
| [Descriptive Analysis](<Descriptive%20Analysis/>) | Normality, correlation and hypothesis testing on white wines | Shapiro-Wilk, Spearman/Pearson, t-test, z-scores | — |
| [Forecasting](<Forecasting/>) | Price forecasting for a bond in a financial portfolio | SQL with `sqldf`, weighted moving average, seasonal index, MAE | — |
| [Water Usage Forecasting](<Water%20Usage%20Forecasting/>) | Forecast of monthly average water usage | Linear trend, Holt-Winters, prediction intervals | [report](https://htmlpreview.github.io/?https://github.com/Adidaware/Machine-Learning-Algorithms/blob/main/Water%20Usage%20Forecasting/water_usage_forecasting.html) |
| [kNN](<kNN/>) | Diabetes prediction from data with missing values | Grouped imputation, frequency encoding, z-score scaling, kNN | — |
| [Parkinsons kNN Classification](<Parkinsons%20kNN%20Classification/>) | Parkinson's diagnosis with kNN, checked on unseen patients | Outlier handling, normalization, kNN (k = 45), precision/recall/F1 | [report](https://htmlpreview.github.io/?https://github.com/Adidaware/Machine-Learning-Algorithms/blob/main/Parkinsons%20kNN%20Classification/parkinsons_knn.html) |
| [Naive Bayes](<Naive%20Bayes/>) | Party prediction from 1984 congressional votes | Naive Bayes ensemble with majority voting | [report](https://htmlpreview.github.io/?https://github.com/Adidaware/Machine-Learning-Algorithms/blob/main/Naive%20Bayes/naivebayes.html) |
| [Parkinsons Tree Models and Logistic Regression](<Parkinsons%20Tree%20Models%20and%20Logistic%20Regression/>) | Comparing three classifiers and combining them in an ensemble | Decision tree, random forest, logistic regression, majority vote | [report](https://htmlpreview.github.io/?https://github.com/Adidaware/Machine-Learning-Algorithms/blob/main/Parkinsons%20Tree%20Models%20and%20Logistic%20Regression/parkinsons_classifiers.html) |
| [Multiple Linear Regression](<Multiple%20Linear%20Regression/>) | Regression modeling on a synthetic dataset | VIF, scaling and encoding, model comparison, MSE, residual checks | [report](https://htmlpreview.github.io/?https://github.com/Adidaware/Machine-Learning-Algorithms/blob/main/Multiple%20Linear%20Regression/multiple_linear_regression.html) |

Each project folder has its own README with the full method write-up and the R packages it needs.

## 🚀 Running an analysis

```bash
git clone https://github.com/Adidaware/Machine-Learning-Algorithms.git
```

1. Open any `.Rmd` file in RStudio.
2. Install the packages listed in that project's README.
3. Click **Knit**. Every dataset is loaded from a public URL, so nothing needs to be downloaded by hand.

## 👤 Author

**Aditya Daware**, Computational Biologist · [LinkedIn](https://www.linkedin.com/in/aditya-daware) · [GitHub](https://github.com/Adidaware)
