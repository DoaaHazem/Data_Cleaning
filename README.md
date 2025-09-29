<a>
<img width="868" height="831" alt="Screenshot 2025-09-20 014041" src="https://github.com/user-attachments/assets/c641efc3-a383-432f-9e26-a55d4d03238b" />
</a>

# 📊 Intro to Data Cleaning

This project was developed as part of a task assigned by the **Digital Egypt Pioneers Initiative (DEPI)**, under the **Ministry of Communications and Information Technology (MCIT), Egypt**.  

The dataset, titled *"Intro to Data Cleaning, EDA, and Machine Learning"*, provides hands-on practice in:
- **Data Cleaning**
- **Handling Missing Values**
- **Detecting and Treating Outliers**
- Preparing the dataset for **Exploratory Data Analysis (EDA)** and **Machine Learning**.

---

## 📁 Dataset Description
The dataset contains demographic and academic information about students, including:
- **fNAME / lNAME** (student names)
- **Age**
- **Gender**
- **Country of origin**
- **Residence type**
- **Entry Exam score (out of 100)**
- **Previous Education**
- **Study Hours (weekly)**
- **Python Course Score (out of 100)**
- **Database (DB) Course Score (out of 100)**

The dataset was initially raw and required significant preprocessing to resolve:
- **Inconsistencies** (e.g., `"Male"` vs. `"M"`, `"Barrrchelors"` vs. `"Bachelor"`, `"Rsa"` vs. `"RSA"`).  
- **Missing values** (mainly in Python and DB scores).  
- **Outliers** (unrealistic values in study hours and performance scores).

---

## 🛠️ Data Cleaning
- **Gender column** → Standardized values to `"M"` and `"F"`.  
- **Country column** → Fixed inconsistent capitalization (e.g., `"norway"` → `"Norway"`).  
- **Previous Education column** → Corrected typos (`"Barrrchelors"` → `"Bachelor"`) and standardized Diploma variations.  
- **Duplicates** → Checked with `df.duplicated().sum()` and dropped with `df.drop_duplicates()`.  

---

## 🔧 Handling Missing Data
- **Numerical Columns (Python)**:
  - Mean and Median imputation were tested to fill missing values.
  - but i used Median.

📌 **Reason**: Preserves dataset size and avoids loss of information.

---

## 📉 Outliers
- **Detection**:
  - Used **Boxplots** (`sns.boxplot`) and the **IQR method**.  

- **Treatment Options**:
  - treat them as realistic values.  

- **Findings**:
  - Very low Python scores (15, 30, 31, 33, 45, 48) were flagged as potential outliers but were realistic, so kept.  
  - Study Hours had some low values but were realistic, so kept.  
  - DB scores showed variations but within realistic performance ranges, so kept.  

---

## ✅ Deliverables
- **Cleaned Dataset** → `cleaned_students.csv`  
- **Jupyter Notebook** → Full code with explanations  
- **Markdown Report** → Explains:  
  - Inconsistencies found and fixed  
  - How missing values were imputed  
  - How outliers were detected and treated  

---

## 🚀 Next Steps
- Perform **EDA** (visualizations, correlations, distributions).  
- Apply **Machine Learning models** to predict performance scores based on features.
---
