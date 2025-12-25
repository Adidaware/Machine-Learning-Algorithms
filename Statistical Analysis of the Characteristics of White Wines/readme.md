White Wine Characteristics & Statistical Analysis
This project performs an exploratory data analysis (EDA) on a dataset of white wine samples to identify relationships between chemical properties and quality ratings. A custom metric, the Swill Index, is introduced to rank wines based on alcohol, sugar, and quality.

📊 Analysis Objectives
Data Volume: Processing records for 4,898 white wine variants.

Alcohol Distribution: Filtering and identifying high-alcohol content wines ( > 12%).

Correlation Filtering: Finding outliers (high alcohol but low quality).

Feature Engineering: Creating the Swill Index to identify wines with specific high-sugar/high-alcohol profiles.

🧪 The "Swill Index" Formula
To identify specific wine profiles, the following calculation was implemented:

Swill=( 
Quality
Alcohol
​	
 )×Residual Sugar
This index helps highlight wines that have high residual sugar and alcohol relative to their perceived quality.

🛠️ Tools & Dataset
R Markdown: Used for integrated code and reporting.

Library: knitr for dynamic table generation.

Dataset: White Wine Quality Dataset (sourced from the UCI Machine Learning Repository).

📂 Repository Structure
analysis.Rmd: The source code containing the R chunks and logic.

README.md: Project documentation.

whitewines.csv: (External link) The raw data used for the analysis.

🚀 How to Replicate
Ensure you have R and RStudio installed.

Clone this repo:

Bash
git clone https://github.com/Adidaware/Machine-Learning-Algorithm.git
Open the .Rmd file and click Knit. R will automatically fetch the data from the S3 bucket and generate the report.
