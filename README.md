# 🏋️ Calories Burned Prediction — Linear Regression

A machine learning project that predicts calories burned during exercise using physiological features.  
Built with Python, scikit-learn, and seaborn.

---

## 📌 Objective

Given exercise and biometric data, can we accurately predict how many calories a person burns?  
This project explores that question using **exploratory data analysis** and a **Linear Regression model**.

---

## 📁 Dataset

Two CSV files merged on `User_ID`:

| File | Description |
|------|-------------|
| `exercise.csv` | Duration, Heart Rate, Body Temperature, Gender, Age, Height, Weight |
| `calories.csv` | Calories burned per session |

> Source: [Kaggle — Calories Burnt Prediction](https://www.kaggle.com/datasets/fmendes/fmendesdat263xdemos)

---

## 🔍 Exploratory Data Analysis

- Checked for missing values → none found
- Plotted calorie distribution → right-skewed
- One-hot encoded `Gender` for correlation analysis
- Heatmap revealed **Duration**, **Body_Temp**, and **Heart_Rate** as top correlates with Calories

---

## 🤖 Model

**Algorithm:** Linear Regression  
**Features used:** `Duration`, `Body_Temp`, `Heart_Rate`  
**Split:** 80% train / 20% test (`random_state=42`)

### Results

| Metric | Value |
|--------|-------|
| MAE | 10.65 |
| MSE | 216.08 |
| Cross-Val R² (5-Fold) | 0.95 |
> The model explains **95% of the variance** in calories burned,
> with an average prediction error of ~10.65 calories.


---

## 📊 Visualizations

- Calories distribution (histogram + KDE)
- Correlation heatmap (with encoded Gender)
- Actual vs. Predicted calories (scatter plot)

---

## 🚀 How to Run

1. Clone the repo
```bash
git clone https://github.com/your-username/calories-prediction.git
cd calories-prediction
```

2. Install dependencies
```bash
pip install pandas seaborn matplotlib scikit-learn
```

3. Open the notebook
```bash
jupyter notebook calories_prediction.ipynb
```

> ⚠️ The notebook was originally written in Google Colab. Remove the `files.upload()` cell and load CSVs directly if running locally.

---

## 💡 Key Takeaway

Exercise duration and body temperature are the strongest predictors of calories burned.  
Even a simple linear model captures the relationship well, suggesting a roughly linear relationship between these features and energy expenditure.

---

## 🛠️ Tech Stack

![Python](https://img.shields.io/badge/Python-3.10-blue)
![scikit-learn](https://img.shields.io/badge/scikit--learn-1.x-orange)
![Pandas](https://img.shields.io/badge/Pandas-2.x-green)
![Seaborn](https://img.shields.io/badge/Seaborn-0.13-lightblue)

---

## 👤 Author
Benkaji Ghassen

[LinkedIn](https://www.linkedin.com/in/benkaji-ghassen-8867bb397/) · [GitHub](https://github.com/gastonation)

