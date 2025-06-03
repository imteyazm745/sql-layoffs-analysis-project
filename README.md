# 📊 Layoff Trends Analysis Using SQL

This project is a complete end-to-end **data analysis** of global tech layoffs using SQL. It demonstrates practical skills in **data cleaning**, **data transformation**, and **exploratory data analysis (EDA)** using a real-world dataset sourced from [Kaggle](https://www.kaggle.com/datasets/swaptr/layoffs-2022).

The analysis focuses on understanding global layoff patterns from **COVID-19 through the present**, uncovering trends by year, industry, geography, and company.

---

## 📦 Dataset Information

- **Source**: [Kaggle - Tech Layoffs](https://www.kaggle.com/datasets/swaptr/layoffs-2022)
- **Description**: Real-time data of tech industry layoffs collected since the start of COVID-19. Includes information like company name, total laid off, percentage of workforce affected, industry, country, dates, and more.

---

## 🗂️ Project Structure

- `layoffs.csv` – Original raw dataset from Kaggle  
- `Data_Cleaning_project.sql` – SQL scripts for cleaning and preparing the data  
- `EDA_practice.sql` – SQL queries for performing exploratory data analysis and generating insights  

---

## 🛠️ Tools & Technologies

- **MySQL** – For writing and executing SQL queries  
- **Excel** – Used for preliminary checks and validations  
- **Kaggle** – Data source for real-world relevance  

---

## 🧹 Data Cleaning Highlights

The raw dataset had several inconsistencies that needed to be cleaned before analysis:

- Removed irrelevant rows and entries with missing essential data (`NULL` values)
- Standardized inconsistent entries (e.g., company names, country formats)
- Removed extra whitespace and formatting issues in text columns
- Converted and formatted dates using SQL functions
- Removed duplicate rows for accurate aggregation
- Created a cleaned version of the dataset for analysis

---

## 📈 Key Insights from EDA

Using SQL queries, I uncovered several trends:

- 🔺 **2022** saw the highest number of layoffs, peaking during economic downturns post-COVID
- 🌎 **US-based companies** contributed the most to global layoffs
- 🏢 Identified the **Top 10 companies** with the largest number of laid-off employees
- 🗓️ Discovered **monthly and yearly layoff trends** using SQL `DATE_FORMAT()` and grouping
- 💼 Layoffs were most common in **Tech, Consumer, and Finance** sectors
- 📊 Correlation found between company size and layoff volume

---

## 💻 Sample SQL Queries

```sql
-- Top 10 companies by total number of layoffs
SELECT company, SUM(total_laid_off) AS total_layoffs
FROM layoffs_cleaned
GROUP BY company
ORDER BY total_layoffs DESC
LIMIT 10;
