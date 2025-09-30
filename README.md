# Nexus-ml-datascience-internship
## 🛒 Task 1: Exploratory Data Analysis (EDA) – Retail Sales

**🎯 Goal:**  
Perform a comprehensive EDA on a retail dataset to uncover customer buying behavior, product performance, and sales trends.

---

### 🔹 Steps Performed
- 📂 Loaded dataset (`Online Retail.csv`)
- 🧹 Cleaned data (removed duplicates, handled missing values, corrected data types)
- ➕ Created a new feature:  
  ```python
  df["Sales"] = df["Quantity"] * df["UnitPrice"]
## 📊 Task 2: Interactive Dashboard – Retail Sales

**🎯 Goal:**  
Build an interactive dashboard to present insights from Task 1 in a clear, visual way for non-technical stakeholders.

---

### 🔹 Steps Performed
- Cleaned dataset reused from Task 1 (`OnlineRetail.csv`).
- Built interactive visualizations using **Plotly Express**:
  - Top 10 countries by sales (bar chart)
  - Top 10 products by sales (bar chart)
  - Sales trend over time (line chart with slider)
  - Peak shopping hours (hourly sales line chart)

---

### 🔑 Dashboard Highlights
- Hover tooltips for exact values  
- Range slider on sales over time  
- Easy comparison of top products and countries  
- Clear view of peak shopping hours  



---
## 🔮 Task 3: Predicting Customer Churn (Classification)

**🎯 Goal:**  
Build a classification model to predict whether a customer will churn (leave the service), so retention efforts can be targeted effectively.

---

### 🔹 Steps Performed
- Loaded **Telco Customer Churn dataset**.  
- Cleaned data (handled missing values, dropped `customerID`, converted `TotalCharges`).  
- Encoded categorical variables using **Label Encoding**.  
- Split dataset into **train (80%)** and **test (20%)** sets.  
- Trained a **Logistic Regression model**.  
- Evaluated model performance using **Accuracy** and a **Confusion Matrix**.  

---

### 🔑 Key Results
- Accuracy score of the Logistic Regression model reported.  
- **Confusion Matrix** explained business-wise:  
  - **TP (True Positives):** Correctly predicted churners  
  - **TN (True Negatives):** Correctly predicted non-churners  
  - **FP (False Positives):** Non-churners flagged incorrectly  
  - **FN (False Negatives):** Missed churners (critical for business)  


---
## 🚀 Task 4: Optimizing Churn Prediction (Advanced Classification)

**🎯 Goal:**  
Enhance the customer churn prediction model by applying more powerful algorithms and advanced evaluation metrics to achieve higher accuracy and better identify at-risk customers.

---

### 🔹 Steps Performed
- Used the **Telco Customer Churn dataset** (same as Task 3).  
- Scaled numerical features with **StandardScaler**.  
- Trained and compared three models:  
  - Logistic Regression (baseline)  
  - Random Forest Classifier  
  - XGBoost Classifier  
- Evaluated performance using **Accuracy, Precision, Recall, and F1-Score**.  
- Analyzed results and provided a **business recommendation**.  

---

### 🔑 Key Results
- **Logistic Regression**: Simple baseline with fair accuracy.  
- **Random Forest**: Improved performance with better precision and recall.  
- **XGBoost**: Best trade-off between accuracy and recall, achieving the highest **F1-Score**.  

**Business Impact:**  
Since retaining customers is cheaper than acquiring new ones, minimizing **False Negatives** (missed churners) is crucial.  
➡️ **XGBoost** is recommended for deployment due to its superior ability to identify churners.  

---

## 🎬 Task 5: Building a Product Recommendation System

**🎯 Goal:**  
Develop a simple content-based movie recommendation system that suggests movies similar to the ones a user has already liked.

---

### 🔹 Steps Performed
- Used the **TMDB 5000 Movies dataset** (`tmdb_5000_movies.csv`).  
- Selected relevant columns: **title** and **overview**.  
- Preprocessed data by filling missing overviews with empty strings.  
- Applied **TF-IDF Vectorizer** to convert text (movie overviews) into numerical features.  
- Calculated **Cosine Similarity** between all movie vectors.  
- Built a **recommendation function** that returns the top 5 most similar movies for a given title.  

---

### 🔑 Key Results
- Implemented a function `recommend_movies(title)` that outputs 5 similar movies.  
- Tested with examples:  
  - **Inception** → Suggested other sci-fi thrillers.  
  - **The Dark Knight** → Suggested superhero/action films.  
  - **Avatar** → Suggested fantasy/adventure titles.  

---
# Task 6: Forecasting Future Sales (Time Series Analysis)

## 🎯 Goal
Build a time series model to forecast sales for the next 30 days, enabling GlobalMart to plan inventory and stock effectively.

## 🔹 Steps Performed

### 1. Data Preparation
- Loaded the **Superstore Sales** dataset.  
- Converted `Ship Date` to datetime and set it as the index.  
- Aggregated sales by day to create a **daily sales time series**.  
- Checked for stationarity using the **Augmented Dickey-Fuller (ADF) test**.

### 2. Train/Test Split
- Split data into **train** (all but last 30 days) and **test** (last 30 days).

### 3. Model Training
- Trained a **SARIMA** model on the training set with:
  - `order = (1,1,1)`
  - `seasonal_order = (1,1,1,7)`

### 4. Predictions on Test Set
- Predicted sales on the test set using **integer-based positions** to avoid KeyErrors.  
- Calculated **RMSE** to evaluate prediction accuracy.

### 5. Forecasting Future Sales
- Forecasted sales for the **next 30 days** beyond the dataset.  
- Generated **future dates** to match the forecast.

### 6. Visualization
- Plotted:
  - Historical sales
  - SARIMA predictions on the test set
  - 30-day future forecast
- Single graph clearly shows trends, short-term prediction performance, and future forecast.

## 🔑 Key Results
- **Test RMSE** reported to measure prediction accuracy.  
- **30-day sales forecast** provided actionable insights for inventory planning.  
- Visualization allows easy comparison of historical trends, model predictions, and future forecast.

## 💡 Business Impact
- Helps optimize inventory and reduce stockouts.  
- Prevents overstocking and supports better operational planning.  
- Enables targeted marketing campaigns and proactive inventory decisions.



