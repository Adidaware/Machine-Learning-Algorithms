# Descriptive Analytics & Statistical Inference (White Wine Dataset)

This repository contains a rigorous statistical analysis of white wine characteristics, focusing on distribution normality, correlation analysis, and hypothesis testing to validate chemical relationships.

## 📊 Key Analytical Components

### 1. Data Structure & Normality
An assessment of central tendency and dispersion for key variables. This includes:
* **Median vs. Trimmed Means:** Comparing the 10% trimmed mean to the median to assess the impact of skewness.
* **Shapiro-Wilk Test:** Formal normality testing for Residual Sugar, Alcohol, Sulphates, and Quality.

### 2. Correlation Analysis
* **Spearman Rank Correlation:** A non-parametric correlation matrix was constructed to identify monotonic relationships between features without assuming linear distribution.
* **Feature Engineering:** Implementation of a custom "Swill Coefficient" to test its relationship with perceived quality using the **Pearson-Moment** coefficient.

$$Swill\ Coefficient = \frac{100 \times Alcohol}{Residual\ Sugar \times \sqrt{Sulphates}}$$

### 3. Hypothesis Testing (t-Test)
A **two-sample t-test** was conducted to determine if there is a statistically significant difference in residual sugar levels between:
* **Group A:** Low-alcohol wines (< 10%)
* **Group B:** High-alcohol wines (≥ 10%)

### 4. Outlier Detection
Used **Z-score Analysis** to identify data points located more than 2 standard deviations from the mean for:
* Total Sulfur Dioxide
* Chlorides
* Density

## 🛠️ Tech Stack
- **Language:** R
- **Tools:** R Markdown, `knitr`
- **Statistical Methods:** Shapiro-Wilk Test, Spearman/Pearson Correlation, Two-sample T-test, Z-score Outlier Detection.

## 📁 Repository Files
* `descriptive_analytics.Rmd`: The complete source code and mathematical logic.
* `README.md`: Project summary and documentation.

## 🚀 How to Use
1. Clone the repository.
2. Ensure you have the `knitr` library installed in R.
3. Knit the `.Rmd` file to view the comprehensive report including the correlation matrix and scatterplot visualizations.

---
**Author:** Daware Aditya   

