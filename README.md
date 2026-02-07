# 🚀 ETL Pipeline for Hackathon Data (Python & Pandas)

An end-to-end Data Engineering project that builds an automated ETL (Extract, Transform, Load) pipeline using **Python**, **Pandas**, and **Regular Expressions (Regex)**. The goal is to sanitize raw, unstructured registration logs into a clean, warehouse-ready schema for analytics.

## 📌 Project Overview
* **Role:** Data Engineer
* **Problem:** A raw dataset of 5,000+ hackathon participants contains inconsistent PII formats (phone numbers with various prefixes, mixed address strings) and missing analytical features.
* **Solution:** Developed a Python script to automate data extraction, perform complex Regex cleaning, engineer new features (Team Name, Email), and enforce strict data typing for MySQL compatibility.

## 🛠️ Tools & Technologies
* **Language:** Python 3.9+
* **Libraries:** `pandas`, `re` (Regex), `datetime`
* **Techniques:** Data Cleaning, Feature Engineering, String Manipulation, Data Warehousing

## 📊 Key Transformation Steps
The pipeline performs the following transformations:
1.  **Extraction:** Ingests raw CSV data directly from Cloud Storage.
2.  **Phone Number Standardization:** Uses Regex to normalize formats (e.g., converts `+62` to `0`, removes dashes/brackets).
3.  **Address Parsing:** Splits unstructured address strings into distinct `City` and `Postal Code` columns.
4.  **Feature Engineering:**
    * **Team Name:** Auto-generated from abbreviations of Name + Country + Institute.
    * **Email:** Synthesized based on Institute type (Universitas vs Corporate) and Country origin.
5.  **Schema Enforcement:** Converts Unix Timestamp (`register_time`) to Datetime objects and formats Birth Dates to `YYYY-MM-DD`.

## 📂 File Structure
* `ETL_Pipeline_Project.ipynb`: The main Jupyter Notebook containing the full code and logic.
* `README.md`: Documentation of the project.

## ⚠️ Disclaimer
* **Dataset:** This project is based on the **Data Engineer Challenge** by **DQLab**.
* **Privacy:** The dataset used is **synthetic/dummy data**. All personal information (names, addresses, phones) is fictitious and for educational purposes only.

## 🤝 Connect
Feel free to reach out if you have questions about the regex patterns or logic used in this project!
