# Flight Delay Analysis

An exploratory data analysis of airline flight data to determine departure delays and identify night-time flight patterns.

## 📊 Overview
This project processes a dataset of flight schedules to calculate:
* Total observations and dimensionality of flight data.
* Average departure delays across all records.
* Identification of flights delayed by more than 60 minutes.
* Feature engineering to classify "Night Flights" based on actual departure times.

## 🛠️ Technologies Used
* **Language:** R
* **Format:** R Markdown
* **Libraries:** `knitr`
* **Dataset:** [FlightsWithAirlines.csv](https://s3.us-east-2.amazonaws.com/artificium.us/datasets/FlightsWithAirlines.csv)

## 📈 Key Metrics
Based on the analysis, the following insights were derived:
* **Average Delay:** Rounding to the nearest minute.
* **Night Flight Threshold:** Flights departing between 7:00 PM and 5:00 AM.

## 🚀 How to Run
1. Clone the repository:
   ```bash
   git clone [https://github.com/Adidaware/Machine-Learning-Algorithm.git](https://github.com/Adidaware/Machine-Learning-Algorithm.git)
