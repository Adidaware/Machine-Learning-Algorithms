# Diabetes Prediction using k-Nearest Neighbors (kNN)

This project implements a supervised machine learning pipeline to predict diabetes in patients. It demonstrates a comprehensive approach to handling "messy" real-world data, including gender-based imputation, frequency encoding, and distance-based classification.

## 🧪 Machine Learning Pipeline

### 1. Data Preprocessing & Imputation
* **Segmented Imputation:** Missing BMI values were not simply replaced by a global average. Instead, I used **10% trimmed means** calculated separately for males and females to ensure biological accuracy and reduce the influence of outliers.
* **Feature Encoding:** * **One-Hot Encoding:** Categorical gender data was converted into binary indicators.
    * **Frequency Encoding:** The `smoking_history` feature was encoded based on the frequency of each category, preserving the prevalence information within the dataset.

### 2. Normalization & Scaling
Because kNN relies on **Euclidean distance**, features with larger ranges (like BMI) can disproportionately influence the model.
* **Z-score Standardization:** All numeric features were scaled to have a mean of 0 and a standard deviation of 1.



### 3. Model Implementation
* **Stratified Sampling:** Used `caret` to partition data into Training (80%) and Validation (20%), ensuring the minority "diabetes" class was represented proportionally in both sets.
* **Classification:** Implemented the `knn` algorithm with **$k = 5$**.

### 4. Performance Evaluation
The model's performance was analyzed using a Confusion Matrix via the `gmodels` package.
* **High Accuracy:** The model achieved a high overall classification rate.
* **Sensitivity/Specificity:** Analyzed the True Positive and True Negative rates to ensure the model effectively identifies diabetic patients without excessive false alarms.



## 🛠️ Tech Stack
- **Language:** R
- **Libraries:**
    - `class`: Core kNN implementation.
    - `caret`: Data partitioning and stratified sampling.
    - `dplyr`: Data manipulation and feature scaling.
    - `gmodels`: Detailed cross-tabulation and model evaluation.
- **Dataset:** [Diabetes Dataset with Missing Values](https://s3.us-east-2.amazonaws.com/artificium.us/datasets/DiabetesDatasetWithMissingValues.csv)

## 📁 Repository Contents
* `knn_analysis.Rmd`: The full source code and analysis.
* `README.md`: Project documentation.

## 🚀 Usage
1. Clone the repository.
2. Install the required libraries in R:
   ```r
   install.packages(c("class", "caret", "dplyr", "gmodels"))
