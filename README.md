# 🧹 Data Cleaning Exercise (Single Notebook)

[![Python](https://img.shields.io/badge/Python-3.9-blue.svg)]()
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)]()
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

This project demonstrates how to **clean messy datasets step by step** using **pandas** inside a Jupyter Notebook.  
It simulates common real-world data quality issues and walks through fixes with clear explanations.

👉 _This project is part of my learning portfolio to showcase practical skills in data cleaning, diagnostics, and reporting._

---

## 📂 Project Structure
---


## 🚀 Workflow Covered

### 1. Generate Messy Data  
Synthetic CSV with:
- Mixed date formats  
- Numeric values as text (commas, spaces)  
- Missing values  
- Duplicates  
- A junk row  

### 2. Load & Diagnose  
Check shape, data types, and quick preview.

### 3. Clean Text Columns  
- Trim whitespace  
- Standardize casing (e.g., `north` → `North`)  

### 4. Parse Dates Safely  
- `errors="coerce"` → invalid → `NaT`  
- Drop bad date rows  

### 5. Normalize Numeric Values  
- Replace commas → dots  
- Convert to float  
- Impute missing values with **median**  

### 6. Deduplicate & Tidy  
- Remove duplicates by `Date + Region`  
- Keep only clean columns  

### 7. Save Outputs  
- **CSV**: cleaned dataset  
- **TXT**: summary statistics  
- **PNG**: sanity plot  

---

## 📊 Demo Outputs


### Demo Outputs

**Cleaned CSV (first 5 rows)**

| Date       | Region | Rainfall(mm) |
|------------|--------|--------------|
| 2024-01-01 | North  | 12.5         |
| 2024-01-02 | South  | 15.0         |
| 2024-01-03 | East   | 15.0         |
| 2024-01-05 | North  | 20.3         |


---

## 📂 Project Structure
```
pandas-data-cleaning-project/
│
├── data/
│ └── messy_rainfall.csv # Raw messy dataset (auto-generated)
│
├── notebooks/
│ └── cleaning_exercise.ipynb # Main Jupyter notebook
│
├── results/
│ ├── cleaned_rainfall.csv # Cleaned tidy dataset
│ ├── summary.txt # Summary statistics
│ └── quick_plot.png # Sanity line plot
│
└── README.md # Project documentation
```

---

## 🛠️ Tech Stack
- **Python 3**
- **pandas** – tabular data cleaning & manipulation
- **NumPy** – numerical operations & transformations
- **Jupyter Notebook** – step-by-step exploration

---


### Summary Statistics  
See: [`results/summary.txt`](/results/summary.txt)

### Quick Plot  
Sanity check rainfall trends across regions:  

![Rainfall Plot](/results/quick_plot.png)

---

## 🛠️ Tools Used
- [Python](https://www.python.org/)  
- [pandas](https://pandas.pydata.org/)  
- [Matplotlib](https://matplotlib.org/)  
- [Jupyter Notebook](https://jupyter.org/)  

---

## 🎯 Key Outcomes
- Handling **messy dates, numbers, and text**  
- Detecting & filling **missing values**  
- Removing **duplicates**  
- Saving **tidy outputs** for downstream use  
- Building a **single notebook pipeline** for cleaning  

---

## 📌 Conclusion

This project demonstrated a full **data cleaning workflow** in a single Jupyter Notebook:

- **Generated a messy dataset** with simulated real-world issues:
  - Mixed date formats, numeric strings with commas/spaces, missing values, duplicates, and junk rows.  
- **Text Cleaning**  
  - Used `.str.strip()` to remove whitespace.  
  - Standardized categorical values with `.str.title()`.  
- **Date Handling**  
  - Parsed dates with `pd.to_datetime(..., errors="coerce")`.  
  - Removed invalid or empty rows safely.  
- **Numeric Normalization**  
  - Replaced comma decimals with dots using `.str.replace()`.  
  - Converted to numeric with `pd.to_numeric()`.  
  - Filled missing values using **median imputation** (`.fillna(median)`).  
- **Deduplication & Structuring**  
  - Removed duplicates with `.drop_duplicates()`.  
  - Selected and renamed columns for tidy output.  
  - Sorted chronologically with `.sort_values()`.  
- **Exporting Results**  
  - Saved a clean CSV (`to_csv`).  
  - Created summary statistics with `.describe()`.  
  - Built a quick validation plot using **Matplotlib**.  

📊 Final outputs are stored in `results/`:  
- `cleaned_rainfall.csv` → tidy dataset  
- `summary.txt` → descriptive statistics  
- `quick_plot.png` → sanity visualization  

---

✅ This exercise shows how to transform **messy raw data** into **clean, structured datasets** using **pandas, NumPy, and Matplotlib** — a practical foundation for analytics and machine learning workflows.


