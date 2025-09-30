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



