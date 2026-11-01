# Clean a Messy CSV Dataset with Pandas

**Author:** Mohamed BEN ALI  
**Date:** November 1, 2026  17:38

---

## 🔗 Solution & Walkthrough
To present the project solution within the platform’s roadmap
🔗 **[Solution](https://roadmap.sh/projects/clean-csv/solutions?u=6acfe5d47bc4b9873155668f)**

---

### 🌐 Connect & Profiles

* 🐙 **GitHub:** [mohammedbenali4321-a11y](https://github.com/mohammedbenali4321-a11y)
* 💼 **LinkedIn:** [Mohamed BEN ALI](www.linkedin.com/in/mohamed-ben-ali-m)
* 🏆 **Kaggle:** [mbaitri](https://www.kaggle.com/mbaitri)
* 🏆 **Roadmap:** [benalimohamed](https://roadmap.sh/u/benalimohamed)

---

## 📌 Project Description
In this project, you will clean a messy synthetic employee dataset using a structured, step-by-step workflow. The dataset includes encoding issues, wrong date formats, mixed types, corrupted columns (like negative phone numbers), missing data, and inconsistent categorical values.

The primary focus is on building a **repeatable, 5-stage cleaning process** rather than just fixing one specific file.

---

## 📋 Project Requirements
- **Load & Inspect:** Load the dataset and perform an initial visual and statistical audit before making any modifications.
- **Data Load Handling:** Handle encoding and delimiter issues at load time.
- **Explicit Dtypes:** Fix column data types explicitly using proper casting (`astype()`, `dtype`).
- **Date Parsing:** Convert date columns safely using `pd.to_datetime()` with `errors='coerce'`.
- **Categorical Standardization:** Clean categorical strings (strip whitespace, standardize capitalization, split combined fields like `Department-Region`).
- **Audit & Export:** Perform a final quality audit and export the cleaned dataset to a new CSV file.

---

## 🛠️ Technologies Used
- **Python** (Data processing and cleaning)
- **Pandas** (Data manipulation and analysis)
- **Jupyter Notebook** (Interactive environment)

---

## 🔄 The 5-Stage Data Cleaning Workflow

```
┌─────────┐     ┌─────────┐     ┌─────────┐     ┌─────────┐     ┌─────────┐
│ 1. LOAD │ ──► │2.INSPECT│ ──► │ 3.CLEAN │ ──► │4.REVIEW │ ──► │5.EXPORT │
└─────────┘     └─────────┘     └─────────┘     └─────────┘     └─────────┘
```

1. **Load:** Read the raw dataset using `pd.read_csv()` (handling delimiter and encoding rules if needed).
2. **Inspect:** Audit structure and data integrity using `df.shape`, `df.head()`, `df.info()`, `df.describe()`, and `df.isnull().sum()`.
3. **Clean:** 
   - Standardize column names into `snake_case` using `.str.lower().str.replace(' ', '_').str.strip()`.
   - Set `employee_id` as the primary index.
   - Fix corrupted phone numbers by removing non-digit characters (`regex=True`).
   - Handle missing data (remove missing `salary` records; impute missing `age` with the median).
   - Split `department_region` into two distinct columns: `department` and `region`.
   - Parse `join_date` into proper `datetime64[ns]` format.
4. **Review:** Perform a final sanity check using `df.info()` and `df.describe()` to ensure data types, counts, and ranges make logical sense.
5. **Export:** Save the finalized dataset to `cleaned_employee_data.csv`.

---

## 🧠 What You Will Learn
- A repeatable **5-stage framework** (`Load` ➔ `Inspect` ➔ `Clean` ➔ `Review` ➔ `Export`) applicable to any tabular dataset.
- How to detect hidden data bugs like **silent type casting** and corrupted numbers (e.g., negative scientific notation in strings).
- Strategies for deciding whether to **impute** (e.g., median for age) or **drop** missing values (e.g., critical financial metrics like salary).
- Why previewing data structure upfront saves hours of troubleshooting downstream.

---

## 🔗 Solution & Walkthrough
A full walkthrough of this project is available on roadmap:  
🔗 **[I Cleaned a Messy CSV File Using Pandas](https://roadmap.sh/projects/clean-csv)**

### 🌐 Connect & Profiles

* 🐙 **GitHub:** [mohammedbenali4321-a11y](https://github.com/mohammedbenali4321-a11y)
* 💼 **LinkedIn:** [Mohamed BEN ALI](www.linkedin.com/in/mohamed-ben-ali-m)
* 🏆 **Kaggle:** [mbaitri](https://www.kaggle.com/mbaitri)
* 🏆 **Roadmap:** [benalimohamed](https://roadmap.sh/u/benalimohamed)
