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
