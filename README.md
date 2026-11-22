# Algerian Forest Fire Prediction using Logistic Regression

This repository contains a simple, beginner-friendly machine learning project that predicts whether a forest fire will occur based on weather observations and weather-derived fire indices.

The project uses **Logistic Regression** implemented with Python and `scikit-learn`, designed to be clean, interpretable, and easy to run.

## 📌 Project Overview

Forest fires pose significant environmental and economic risks. By analyzing weather parameters (temperature, relative humidity, wind speed, rainfall) along with standardized Fire Weather Index (FWI) components, this model classifies weather conditions into two categories:

* **$1$ (Fire)**: Conditions indicate high likelihood of forest fire occurrence.
* **$0$ (Not Fire)**: Conditions indicate low risk of fire occurrence.

---

## 📊 Dataset Information

* **Original Source:** [UCI Machine Learning Repository - Algerian Forest Fires Dataset](https://archive.ics.uci.edu/dataset/547/algerian+forest+fires+dataset)
* **Regions Covered:** Bejaia Region and Sidi-Bel Abbes Region in Algeria (June 2012 – September 2012)
* **Original Size:** $244$ instances
* **Cleaned Data:** $243$ instances across $10$ feature columns and $1$ binary target column (`Classes`)

### Features Used

1. **`Temperature`**: Noon temperature in $^\circ\text{C}$ (range: $22$ to $42$)
2. **`RH`**: Relative Humidity in $\%$ (range: $21$ to $90$)
3. **`Ws`**: Wind speed in $\text{km/h}$ (range: $6$ to $29$)
4. **`Rain`**: Total rainfall per day in $\text{mm}$ (range: $0$ to $16.8$)
5. **`FFMC`**: Fine Fuel Moisture Code index (range: $28.6$ to $92.5$)
6. **`DMC`**: Duff Moisture Code index (range: $1.1$ to $65.9$)
7. **`DC`**: Drought Code index (range: $7$ to $220.4$)
8. **`ISI`**: Initial Spread Index (range: $0$ to $18.5$)
9. **`BUI`**: Buildup Index (range: $1.1$ to $68$)
10. **`FWI`**: Fire Weather Index (range: $0$ to $31.1$)

---

## 🧹 Data Preprocessing

The raw dataset contains stacked regional datasets along with header artifacts. Preprocessing steps included:

1. Stripping leading/trailing whitespaces from column headers and values.
2. Removing redundant title/header rows embedded in the middle of the dataset.
3. Dropping invalid or corrupted rows.
4. Encoding binary class labels ($1$ for `fire`, $0$ for `not fire`).
5. Exporting the cleaned data to `forest_fires_cleaned.csv`.

---

## ⚙️ Model & Implementation

* **Algorithm:** Logistic Regression (`LogisticRegression(max_iter=1000)`)
* **Train/Test Split:** $80\%$ Training data, $20\%$ Testing data (`random_state=42`)
* **Decision Threshold:** Probability threshold $P(\text{Fire}) \ge 0.5$
* **Interactive Inference:** Includes a CLI prompt at the end of the script/notebook for manual real-time prediction based on user-provided feature inputs.

---

## 📈 Results & Key Insights

* **Test Accuracy:** $\approx 98\%$
* **Feature Importance:** Higher values of `FFMC`, `ISI`, and `FWI` strongly correlate with fire occurrences.

---
## GitHub Submission

Submitted to: [@complexiota](https://github.com/complexiota)
---

## 🚀 How to Run

### 1. Clone the repository
```bash
git clone https://github.com/superiorshree/forest-fire-prediction.git
cd forest-fire-prediction
```

### 2. Install dependencies
```bash
pip install -r requirements.txt
```

### 3. Run the project

* **Option A: Run Jupyter Notebook**
  ```bash
  jupyter notebook forest_fire_logistic_regression.ipynb
  ```

* **Option B: Run Python Script**
  ```bash
  python forest_fire_logistic_regression.py
  ```

---

## 👨‍💻 Author & Acknowledgments

Student Name: Shreeyansh Mahamuni

Roll Number: AD3231

Course: Artificial Intelligence and Data Science

Activity: Activity 2 – Logistic Regression Algorithms
 **Dataset Credit:** Faroudja Abid & UCI Machine Learning Repository
