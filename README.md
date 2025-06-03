# 📊 Layoff Trends Analysis Using SQL

This project is an end-to-end data analysis of global layoff trends using SQL. It focuses on data cleaning and exploratory data analysis (EDA) using real-world data sourced from Kaggle.

---

## 📁 Project Structure

- `layoffs.csv` – Original raw dataset downloaded from Kaggle  
- `Data_Cleaning_project.sql` – SQL scripts to clean, standardize, and prepare the data  
- `EDA_practice.sql` – SQL queries for exploratory data analysis and insight generation

---

## 🔧 Tools & Technologies

- MySQL (SQL)
- Kaggle Dataset
- Excel (used for initial checks)

---

## 🧹 Data Cleaning Highlights

- Removed NULL and irrelevant values
- Standardized inconsistent formatting
- Trimmed extra spaces and fixed company/location names
- Removed duplicate rows
- Converted date formats for time-based analysis

---

## 📈 Key Insights from EDA

- Most layoffs occurred in 2022 across multiple tech industries
- US-based companies were most affected in terms of volume
- Identified top 10 companies with highest layoffs
- Monthly and yearly layoff trends uncovered using SQL date functions
- Sector-wise comparison of layoffs and total employees affected

---

## 📊 Sample Queries Used

```sql
-- Total layoffs per company
SELECT company, SUM(total_laid_off) AS total_layoffs
FROM layoffs_cleaned
GROUP BY company
ORDER BY total_layoffs DESC
LIMIT 10;
