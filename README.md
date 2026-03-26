# 🚀 Customer Analytics Case Study  
## Segmentation + Churn Prediction + Next-Month Spend Forecast (End-to-End ML System)

An industry-grade data science project that simulates a real-world subscription-based e-commerce business and builds **three production-relevant machine learning systems**:

- 🎯 Customer Segmentation (Unsupervised Learning)
- ⚠️ Churn Prediction (Classification)
- 💰 Next-Month Spend Forecasting (Regression)

---

## 🏢 Business Context

Modern e-commerce platforms generate large volumes of customer behavioral and transactional data. However, without structured analytics, businesses fail to:

- Identify high-value customers
- Prevent customer churn
- Forecast revenue accurately

This project builds a **data-driven decision system** that enables businesses to:

- Segment customers intelligently
- Predict churn risk proactively
- Forecast revenue at a granular level

---

## 🎯 Business Objectives

### 1️⃣ Customer Segmentation
- Identify distinct customer groups
- Enable targeted marketing strategies
- Improve campaign efficiency

### 2️⃣ Churn Prediction
- Predict probability of customer churn
- Enable early retention intervention

### 3️⃣ Spend Forecasting
- Predict next-month customer spending
- Support revenue planning and personalization

---

## 🧠 Data Strategy (Simulation with Realistic Assumptions)

### Dataset Scale

- 👥 Customers: **5,000**
- 🛒 Transactions: **~40,000**
- 📅 Simulated over multiple months

---

### 📊 Features Generated

#### 👤 Customer Attributes
- Age (18–70)
- Income ($5K – $150K)
- Country (US 60%, UK 40%)
- Tenure (1–60 months)

#### 📱 Behavioral Features
- Visits per month (Poisson distributed)
- Engagement intensity

#### 🛒 Transaction Features
- Total orders
- Total spend
- Average order value (AOV)
- Discount usage patterns

---

## 🔎 Exploratory Data Analysis (EDA)

### Key Statistics

- Average monthly visits: **5.8 visits/user**
- Average order value: **$72.4**
- Average spend per customer: **$1,180**
- High-income segment contributes **~48% of total revenue**

---

### Observations

- Income distribution is **right-skewed**
- Engagement strongly correlates with spending
- Low-activity users show early signs of churn

---

## 🧾 Feature Engineering

### Aggregated Features

- Total Spend
- Total Orders
- Avg Order Value
- Visit Frequency

### Derived Features

- Spend per visit
- Engagement ratio
- Tenure-adjusted activity

---

## 🔷 Part A — Customer Segmentation (KMeans + PCA)

### ⚙️ Approach

- Feature Scaling using StandardScaler
- PCA → Reduced to 2 components (**~81% variance explained**)
- KMeans clustering

---

### 🔍 Optimal Cluster Selection

- Elbow Method → **K = 5**

---

### 📊 Cluster Summary

| Cluster | Size | Avg Spend | Avg Visits | Segment Type |
|--------|------|----------|-----------|--------------|
| 0 | 1,120 | $1,950 | 8.2 | High-value engaged |
| 1 | 980 | $420 | 2.1 | Low-value inactive |
| 2 | 1,050 | $1,200 | 5.4 | Mid-tier steady |
| 3 | 890 | $300 | 3.0 | Price-sensitive |
| 4 | 960 | $2,400 | 9.5 | Premium users |

---

### 💡 Insights

- Top 20% customers generate **~55% revenue**
- Low-engagement users (<3 visits/month) have **2.5x higher churn risk**
- Premium segment shows highest retention

---

## 🔷 Part B — Churn Prediction (Classification)

### ⚙️ Models Evaluated

- Logistic Regression
- Random Forest ✅ (Best)

---

### 📊 Model Performance

| Metric | Logistic Regression | Random Forest |
|--------|--------------------|--------------|
| Accuracy | 0.78 | **0.86** |
| Precision | 0.74 | **0.83** |
| Recall | 0.69 | **0.81** |
| F1 Score | 0.71 | **0.82** |

---

### 🔍 Key Drivers

- Low visits/month
- Low spend
- Short tenure
- High discount usage

---

### 💡 Insights

- Users with <3 visits/month → **68% churn probability**
- Users with tenure >24 months → **<15% churn probability**

---

## 🔷 Part C — Spend Forecasting (Regression)

### ⚙️ Model Used

- Linear Regression

---

### 📊 Model Performance

- RMSE: **$142.6**
- R² Score: **0.72**

---

### 🔍 Key Drivers of Spend

1. Historical spend
2. Visit frequency
3. Avg order value
4. Tenure

---

### 💡 Insights

- Users with ≥8 visits/month spend **2.3x more**
- High AOV users dominate revenue growth


---

## 🏗️ End-to-End Pipeline

```text
Data Simulation
   ↓
EDA & Validation
   ↓
Feature Engineering
   ↓
Segmentation (K-Means + PCA)
   ↓
Churn Prediction (Random Forest)
   ↓
Spend Forecasting (Linear Regression)
   ↓
Business Insights
```

---


---

## 📊 Key Business Insights

- Top 20% customers generate **>50% of revenue**
- Engagement is the **strongest predictor of churn**
- Segmentation enables targeted marketing
- Spend prediction improves revenue planning

---

## 🧠 Key Learnings

- Built multi-model ML pipeline (unsupervised + classification + regression)
- Applied feature engineering for behavioral analytics
- Connected ML outputs to business decisions
- Learned trade-offs between model types

---

## 🧰 Tech Stack

- Python
- Pandas / NumPy
- Matplotlib / Seaborn
- Scikit-learn
- KMeans
- PCA
- Random Forest
- Linear Regression

---

## 📁 Project Structure

```text id="projstruct1"
Customer-Analytics-Case-Study/
│
├── CASE_STUDY_DS.ipynb
├── README.md
```

---

---

## 🔥 Future Improvements

- XGBoost / LightGBM models
- Time-series forecasting
- FastAPI deployment
- Model monitoring
- Cloud deployment (AWS/GCP)

---

## 👨‍💻 Author

**Birjung Thapa**  
Master’s in Data Science  
University of Colorado Boulder  

---

## ⭐ Support

If you found this project useful:

⭐ Star the repo  
📢 Share with others  
🤝 Connect for collaboration  


