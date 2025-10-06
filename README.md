# Loan Default Risk Analysis

Exploratory Data Analysis (EDA) on a bank’s loan application dataset to identify the key factors influencing a client’s likelihood of default, helping financial institutions minimize lending risk while maintaining business growth.


## Introduction

This case study applies **Exploratory Data Analysis** in a real-world **risk analytics** scenario for a consumer finance company.  
The goal is to analyze historical loan data to identify behavioral and demographic patterns that distinguish **potential defaulters** from **reliable borrowers**.

When a loan company receives an application, it faces two major risks:
1. Rejecting a creditworthy client → **loss of potential business**
2. Approving a risky client → **financial loss due to default**

This project demonstrates how data-driven insights can help strike the right balance between the two.


## Business Understanding

The company provides loans to urban clients, many of whom have limited or no credit history. Using EDA, we explore how applicant and loan attributes (income, education, family, occupation, etc.) influence the likelihood of default.

The dataset includes two perspectives:
- **Clients with payment difficulties:** at least one late payment beyond a set threshold.
- **Clients without payment difficulties:** all payments made on time.

Each application has one of the following outcomes:
- **Approved** – loan granted  
- **Cancelled** – withdrawn by client  
- **Refused** – rejected by company  
- **Unused offer** – pre-approved but not utilized  


## Business Objectives

The primary objective is to identify **driving factors of loan default**, which can guide:
- Loan approval or rejection decisions  
- Risk-based pricing (interest rate adjustments)  
- Credit portfolio risk assessment  

In short, the aim is to ensure that creditworthy clients are not rejected and risky clients are identified early.


## Analytical Approach

1. **Data Understanding**
   - Combined data from three sources: `application_data.csv`, `previous_application.csv`, and `columns_description.csv`.

2. **Data Cleaning**
   - Dropped columns with >40% missing values.
   - Imputed values for <40% missing data based on skewness and data type.
   - Combined 21 document flag columns into one aggregated indicator.

3. **Outlier & Imbalance Detection**
   - Examined numerical distributions and identified outliers related to income, credit, and annuity amounts.
   - Checked for data imbalance in the target variable (default vs non-default).

4. **Exploratory Data Analysis**
   - Univariate, segmented univariate, and bivariate analysis.
   - Correlation analysis (top correlated features for each segment).
   - Visualization-driven insights into education, occupation, income, and family-related risks.

5. **Business Interpretation**
   - Mapped each statistical pattern to real-world implications in lending and portfolio management.


## Tools & Libraries

- **Python** (Jupyter Notebook)
- **Pandas**, **NumPy**, **Matplotlib**, **Seaborn**
- **EDA Techniques:** Univariate, Segmented Univariate, and Bivariate Analysis


## Key Insights

### Application Data
- Majority of loans are **cash loans**, with higher default ratios.  
- **Male** clients show a higher default probability than **females**.  
- **Clients with no children** have a lower default rate.  
- **Laborers** have the most defaults; **Managers** have the least.  
- Default ratio increases with **larger family size (>2)**.  
- **Self-employed** and **Business Entity Type 3** clients default more often.  
- **Higher education** and **older age (60–70 years)** correlate with fewer defaults.

### Merged Application Data
- **Home ownership** positively influences loan approval likelihood.  
- **Secondary or higher education** strongly correlates with approvals.  
- **Laborers, core staff, and sales staff** most often receive loan approvals.


## Conclusion & Business Impact

Clients more likely to **default**:
- Male  
- Married with >2 children  
- Education below secondary  
- Occupation: Laborer / Businessman / Self-employed  
- Family size >4  
- Income between **100K–200K**  
- Credit amount between **200K–750K**  
- Annuity between **10K–50K**  
- Age **21–50 years**

Clients least likely to **default**:
- Female  
- Single / Widowed / Separated  
- Pensioners or Managers  
- Higher education level  
- Age **60+ years**

**Impact:**  
By identifying these patterns, lenders can refine credit scoring models, set better interest rates, and reduce non-performing loans.


## Files in this Repository

| File Name | Description |
|------------|-------------|
| `LOAN_APPLICATION_CASE_STUDY.ipynb` | Jupyter notebook with complete EDA, data cleaning, and visualizations |
| `Loan_Application_Analysis_Aakash_Maskara.pdf` | Final report and summary presentation |
| `application_data.csv` | Client application data (demographics, employment, income, etc.) |
| `previous_application.csv` | Historical loan records and outcomes |
| `columns_description.csv` | Metadata dictionary describing dataset variables |

---

## Author

**Aakash Maskara**  
*M.S. Robotics & Autonomy, Drexel University*  
Data Science | Machine Learning | Quantitative Finance  

[LinkedIn](https://linkedin.com/in/aakashmaskara) • [GitHub](https://github.com/AakashMaskara)
