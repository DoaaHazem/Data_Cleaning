<a>
<img width="868" height="831" alt="Screenshot 2025-09-20 014041" src="https://github.com/user-attachments/assets/c641efc3-a383-432f-9e26-a55d4d03238b" />
</a>

# 📊 Intro to Data Cleaning
This project was developed as part of a task assigned by the **Digital Egypt Pioneers Initiative (DEPI)**, under the **Ministry of Communications and Information Technology (MCIT), Egypt**.  

This project demonstrates practical steps in **data cleaning**, **handling missing values**, **detecting and treating outliers**, and preparing a dataset for **Exploratory Data Analysis (EDA)** and **Machine Learning**.

---

## 📁 Dataset Description
The dataset contains demographic and academic information about students, including:
- **Age**
- **Gender**
- **Country of origin**
- **Previous Education**
- **Study Hours**
- **Python Course Score (out of 100)**
- **Database (DB) Course Score (out of 100)**

The dataset was initially raw and contained:
- **Inconsistencies** (e.g., "Male" vs. "M", "Barrrchelors" vs. "Bachelor")  
- **Missing values** (mainly in Python scores)  
- **Outliers** (unrealistic values in performance scores and study hours)

---

## 🛠️ Data Cleaning
- **Gender column**: Standardized values to `"M"` and `"F"` only.
- **Country column**: Fixed inconsistent capitalization (e.g., `"norway"` → `"Norway"`).
- **Previous Education column**: Corrected typos such as `"Barrrchelors"` → `"Bachelor"`, and standardized Diploma variations.
- **Duplicates**: Checked and dropped any duplicate rows.

---

## 🔧 Handling Missing Data
- **Numerical Columns (Python scores)**:
  - **Mean imputation**: Filled missing values with the column mean (to preserve trend).
  - **Median imputation**: Also tested using the median (more robust against outliers).

📌 **Reason:** These methods preserve the dataset size without dropping rows, ensuring no information is lost.

---

## 📉 Outliers
- **Detection:**  
  - Used **Boxplots** (`sns.boxplot`) and **IQR method** to identify outliers.  

- **Findings & Treatment:**  
  - **Python**: Very low scores (15, 30, 31, 33, 45, 48) were treated as outliers and removed.  
  - **Study Hours**: Some low values were detected but considered realistic, so they were kept.  
  - **DB**: Low scores were also considered natural performance variations and kept.  

---

## ✅ Deliverables
- **Cleaned Dataset** → `cleaned_students.csv`  
- **Jupyter Notebook** → Contains full code and explanations  
- **Short Report (Markdown)** → Explains:  
  - Inconsistencies found and fixed  
  - How missing values were imputed  
  - How outliers were detected and treated  

---

## 🚀 Next Steps
- Perform **EDA** (visualizations, correlations, distributions).  
- Apply **Machine Learning models** for prediction tasks (e.g., predicting scores based on features).  

---
