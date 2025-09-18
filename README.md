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
