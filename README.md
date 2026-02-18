# 📊 Excel Data Cleaning Project

## 🔎 Project Overview

This project involves cleaning and standardizing three separate datasets using Microsoft Excel.  
The objective was to improve data quality, ensure consistency, and prepare each dataset for reliable analysis and reporting.

---

## 🗂 Datasets Summary

| Dataset | Size | Key Issues | Cleaning Approach |
|----------|------|------------|-------------------|
| Dataset 1 | 20 rows | Inconsistent text, unnecessary columns, mixed year format | Structural cleanup and formatting |
| Dataset 2 | 12,000+ rows | Missing numerical values, blank discounts | Calculated imputations + controlled averaging |
| Dataset 3 | 10,000+ rows | Extensive blanks, unknown entries, structural inconsistencies | Derived values + selective deletion + ongoing validation |

---

# 🧹 Dataset 1 – Small Structured Dataset (20 Rows)

### Issues Identified
- Unnecessary columns
- Inconsistent text and special characters
- Combined year range column
- Incorrect data formats

### Cleaning Actions
- Removed irrelevant columns
- Standardized text entries
- Split `Year` column into:
  - `Start Year`
  - `End Year`
- Applied appropriate data types (Text, Number, Date where applicable)

### Result
A fully standardized and analysis-ready dataset with consistent formatting and structure.

---

# 📦 Dataset 2 – Large Transaction Dataset (12,000+ Rows)

### Issues Identified
- Missing values in:
  - `Price Per Unit`
  - `Quantity`
  - `Total Spent`
- Blank entries in `Discount Applied`
- Inconsistent column formatting

### Cleaning Strategy

#### 1️⃣ Numerical Imputation
Where possible:
- Derived missing values using:
  - `Total Spent = Price Per Unit × Quantity`
  - Reverse calculations when one value was missing

If calculation was not possible:
- Filled missing values using column averages to maintain dataset integrity

#### 2️⃣ Categorical Handling
- Filled blank `Discount Applied` entries with `NA`
  - Prevented misinterpretation as zero discount
  - Preserved analytical clarity

#### 3️⃣ Formatting
- Standardized numerical formats
- Applied currency formatting where required
- Ensured consistent decimal precision

### Result
A large, structured dataset with minimal data loss and clearly documented imputation logic.

---

# 🏗 Dataset 3 – Large Dataset with Structural Issues (10,000+ Rows)

### Issues Identified
- Large volume of unknown, blank or invalid entries in:
  - `Price Per Unit`
  - `Quantity`
  - `Total Spent`
  - `Date`
  - `Location`
  - `Payment Method`
  - `Item`

### Cleaning Strategy

#### 1️⃣ Numerical Recovery
- Derived missing numerical values using logical calculations
- Deleted rows only when:
  - Values could not be logically reconstructed
  - The number of affected rows was statistically insignificant

#### 2️⃣ Item Deduction
- Inferred missing `Item` entries using transaction patterns and related fields where possible

#### 3️⃣ Formatting
- Standardized numeric and date formats
- Removed obvious structural errors

---

## ⚠ Ongoing Challenges

Dataset 3 contains a significant number of:

- Unverifiable dates
- Ambiguous locations
- Invalid payment methods
- Non-deducible item entries

These entries require further investigation and potentially:
- External validation
- Business rules clarification
- Or structured removal based on defined thresholds

---

# 🛠 Tools Used

- Microsoft Excel
- Formulas (IF, Arithmetic Operations)
- Data Filtering & Sorting
- Conditional Formatting
- Column Splitting
- Data Type Standardization

---

# 🎯 Key Skills Demonstrated

- Data cleaning and transformation
- Logical value derivation
- Controlled imputation strategies
- Data integrity preservation
- Handling large datasets (10k+ rows)
- Structured documentation
- Analytical decision-making

---

# 📌 Conclusion

This project demonstrates practical experience in cleaning both small and large datasets, applying logical imputation methods, preserving data integrity, and preparing raw data for analysis.

Further improvements to Dataset 3 will focus on establishing structured rules for handling ambiguous categorical data to enhance reliability and analytical validity.
