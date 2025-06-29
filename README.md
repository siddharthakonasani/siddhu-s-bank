# 📊 Yes Bank Stock Price Prediction using Machine Learning & Gen-AI

This project is an end-to-end machine learning pipeline to predict the **monthly closing stock price** of **Yes Bank** (or any other stock) using historical data, statistical analysis, and a production-ready ML model deployed on the cloud.

---

## 🚀 Project Overview

* **Objective:** Predict the monthly closing stock price using past stock data.
* **ML Techniques Used:** Feature engineering, preprocessing, PCA, hypothesis testing, and regression models.
* **Final Output:** A saved ML model (`.pkl`) with a Flask API for deployment on cloud platforms like AWS.

---

## 📁 Folder Structure

```
yesbank-ml-project/
├── notebooks/               # Google Colab .ipynb files
├── data/                    # Yes Bank stock CSV or any stock data
├── models/                  # Saved model (joblib)
├── api/
│   ├── app.py               # Flask app to serve predictions
│   ├── requirements.txt     # Dependencies
│   └── test_input.json      # Example request format
├── README.md                # This file
└── LICENSE
```

---

## 📊 Steps Performed

### 1. Know Your Data

* Loaded Yes Bank stock data
* Handled missing values, checked column types
* Univariate, bivariate, multivariate visualizations

### 2. Hypothesis Testing

* Pre vs post-2018 prices
* Close vs Open price
* Volatility vs price range

### 3. Feature Engineering

* `Price_Range`, `Close_Open_Diff`, `Log_Volatility`, `Month`, `Year`

### 4. Preprocessing Pipeline

* Missing values, outliers, encoding, scaling
* PCA for dimensionality reduction
* Train-test split

### 5. Model Building

* Compared **Linear Regression**, **Random Forest**, and **XGBoost**
* **XGBoost selected** with **94% R² accuracy**

### 6. Model Deployment

* Saved using `joblib`
* Built Flask API in `app.py`
* Deployment-ready for AWS EC2, Render, or Azure

---

## 📦 Dependencies

Install with:

```bash
pip install -r requirements.txt
```

Typical contents:

```
flask
xgboost
joblib
scikit-learn
numpy
pandas
```

---

## 🧪 Test the API (after running it)

```bash
curl -X POST http://localhost:5000/predict \
  -H "Content-Type: application/json" \
  -d @test_input.json
```

---

## ☁️ Cloud Deployment Options

* ✅ AWS EC2 (Ubuntu VM with Flask)
* ✅ AWS Elastic Beanstalk (upload zipped project)
* ✅ Render.com (GitHub auto-deploy)

---

## 📈 Accuracy Summary

* **Final Model:** XGBoost Regressor
* **R² Score:** 94% accuracy
* **Best Features:** `Log_Volatility`, `Price_Range`, `Close_Open_Diff`

---

## 📌 Future Enhancements

* Add Streamlit/Flask UI
* Real-time data fetching using `yfinance`
* Integrate financial news sentiment analysis
* Deploy using Docker + CI/CD pipeline

---

## 👤 Author

**Konasani Siddhartha Ram**
Machine Learning Project | AWS Learner Lab Deployment

---

## 📜 License

This project is open-source and available under the [MIT License](LICENSE).
