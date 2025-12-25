# White Wine Characteristics & Statistical Analysis

This project explores a dataset of white wine variants to analyze chemical properties, alcohol content distribution, and the relationship between sugar levels and quality ratings.

## 📊 Project Overview
The analysis focuses on filtering high-alcohol wines and implementing a custom scoring metric to identify specific wine profiles.

### Key Objectives:
* **Data Inspection:** Analyzing attributes for over 4,800 wine samples.
* **High-Alcohol Filtering:** Identifying wines with alcohol content > 12%.
* **Quality Analysis:** Isolating wines that maintain high alcohol levels but receive low quality scores.
* **Feature Engineering:** Implementing the "Swill Index" to rank wines based on their chemical composition.

## 🧪 The "Swill Index"
A custom feature was engineered to evaluate the wines, defined by the formula:

$$Swill = \left( \frac{Alcohol}{Quality} \right) \times Residual\ Sugar$$

This index highlights wines with high residual sugar and alcohol relative to their perceived quality rating.

## 🛠️ Technologies & Dataset
- **Language:** R
- **Format:** R Markdown (`.Rmd`)
- **Main Library:** `knitr` (for table rendering)
- **Data Source:** [White Wine CSV](https://s3.us-east-2.amazonaws.com/artificium.us/datasets/whitewines.csv)

## 📁 Repository Contents
* `white_wine_analysis.Rmd`: The primary source code and analysis.
* `README.md`: Project documentation and summary.

## 🚀 Usage
1. Clone the repository:
   ```bash
   git clone [https://github.com/Adidaware/Machine-Learning-Algorithm.git](https://github.com/Adidaware/Machine-Learning-Algorithm.git)
