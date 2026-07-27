# 🏦 Largest Banks ETL Pipeline

An end-to-end ETL (Extract, Transform, Load) pipeline built with Python. This project extracts data about the world's largest banks from an archived Wikipedia page, transforms market capitalization values into multiple currencies using exchange rates, exports the processed data to CSV, loads it into a SQLite database, and executes SQL queries for analysis.

---

## 📌 Project Overview

This project demonstrates the complete ETL workflow:

- **Extract** bank data from a web page using BeautifulSoup.
- **Transform** market capitalization values into GBP, EUR, and INR.
- **Load** the processed data into both a CSV file and a SQLite database.
- **Query** the database using SQL.
- **Log** each ETL stage with timestamps.

---

## 📂 Project Structure

```
Largest-Banks-ETL/
│
├── ETL_Project.ipynb
├── exchange_rate.csv
├── Largest_banks_data.csv
├── Banks.db
├── code_log.txt
├── README.md
└── requirements.txt
```

---

## 🛠 Technologies Used

- Python
- Pandas
- Requests
- BeautifulSoup4
- SQLite3

---

## ⚙ ETL Workflow

### 1️⃣ Extract

- Download the archived Wikipedia page.
- Parse the HTML using BeautifulSoup.
- Extract:
  - Bank Name
  - Market Capitalization (USD)
- Clean the Market Cap column.
- Store the data in a Pandas DataFrame.

---

### 2️⃣ Transform

Read exchange rates from a CSV file and create the following columns:

- MC_GBP_Billion
- MC_EUR_Billion
- MC_INR_Billion

---

### 3️⃣ Load

Save the transformed dataset to:

- CSV file
- SQLite database

---

### 4️⃣ Query

Execute SQL queries on the database using Pandas.

Example:

```sql
SELECT * FROM Largest_banks;
```

---

### 5️⃣ Logging

Every ETL stage is recorded in:

```
code_log.txt
```

Example:

```
2026-Jul-27 13:10:22, Extraction Started
2026-Jul-27 13:10:24, Data extracted successfully
2026-Jul-27 13:10:25, Transformation completed
2026-Jul-27 13:10:26, Data loaded to CSV
2026-Jul-27 13:10:27, Data loaded to Database
2026-Jul-27 13:10:28, SQL query executed
```

---

## 🚀 How to Run

### Clone the repository

```bash
git clone https://github.com/your-username/largest-banks-etl.git
```

### Install dependencies

```bash
pip install -r requirements.txt
```

### Run the notebook

Open:

```
ETL_Project.ipynb
```

Run all cells.

---

## 📊 Output

The pipeline generates:

- Largest_banks_data.csv
- Banks.db
- code_log.txt

---

## 📚 Learning Objectives

This project demonstrates:

- Web Scraping
- Data Cleaning
- ETL Pipelines
- Pandas
- BeautifulSoup
- SQLite
- SQL Queries
- Logging
- Data Engineering Fundamentals

---

## 📄 Requirements

```text
pandas
requests
beautifulsoup4
lxml
```

---

## 👨‍💻 Author

**Ashraf Aboalyazid**

Data Engineer

- GitHub: https://github.com/agaboalyazid
- LinkedIn: https://www.linkedin.com/in/agaboalyazid/

---

⭐ If you found this project useful, consider giving it a star!
