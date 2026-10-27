# Loan Approval Analysis

Exploratory data analysis (EDA) of 4,269 loan applications to identify which
applicant and loan characteristics have the clearest relationship with loan
approval.

> This is an exploratory analysis. It identifies associations in the dataset;
> it does not prove causation or reproduce a bank's lending policy.

## 📌 Objective
Find out which factors (CIBIL score, loan term, income, loan amount, assets,
education, employment type, dependents) are most closely linked to approval.

## 📂 Dataset
- **File:** `loan_approval_dataset.csv`
- **Records:** 4,269 loan applications
- **Target:** `loan_status` (Approved / Rejected)
- **Features:** income, loan amount, loan term, CIBIL score, residential /
  commercial / luxury / bank assets, education, self-employed, dependents

## 🛠️ Tools & Libraries
Python | pandas | NumPy | Matplotlib | Jupyter Notebook

## 🧹 Data Preparation
- Stripped extra whitespace from column names and text values
- Validated `loan_status` values
- Found **28 negative asset values** and replaced each with the median of the
  valid values in the same column
- Created new columns: approval flag, income, loan amount and total assets in
  ₹ lakhs
- Grouped CIBIL scores into ranges and income, loan amount and assets into
  quartile bands

## 🔍 Key Findings
- **Overall approval rate: 62.2%** (2,656 approved, 1,613 rejected)
- **CIBIL score has the strongest relationship with approval.** Approval is
  11.0% for scores 300–449 and 38.4% for 450–599, and above 99% for both
  ranges over 600.
- **Loan term shows a smaller pattern.** 4-year loans have the highest
  approval rate (81.9%), then 2-year loans (78.0%). Most terms from 6 to
  20 years are around 53–61%.
- **Education and self-employment barely matter.** Graduates 62.5% vs
  non-graduates 62.0%; self-employed and not self-employed both about 62.2%.
- **Number of dependents shows no clear trend** (60.3% to 64.2%).
- Income, loan amount and total assets do not individually explain the
  decision well.

## 📊 Visualizations
![Overall Approval]<img width="1088" height="537" alt="image" src="https://github.com/user-attachments/assets/741c86be-6cef-4f68-8a7e-1bd98ac4cb52" />
![Approval by CIBIL Score]<img width="1088" height="646" alt="image" src="https://github.com/user-attachments/assets/15ad9a4e-0d15-4c20-9590-f6cd55e3375a" />
![Approval by Loan Term]<img width="1088" height="581" alt="image" src="https://github.com/user-attachments/assets/b954f987-c424-4973-9789-171c0f26e249" />


## ▶️ How to Run
1. Clone the repository
   `git clone https://github.com/YOUR-USERNAME/loan-approval-analysis.git`
2. Install dependencies
   `pip install -r requirements.txt`
3. Open the notebook
   `jupyter notebook loan_approval_analysis.ipynb`

## ⚠️ Limitations
- Associations only; no causal claims
- Income, loan and asset ranges are quartile bands created for this project,
  not official banking categories
- EDA only; no machine learning model was built

## 👤 Author
**Habeeb mohmaed** | [LinkedIn](www.linkedin.com/in/habeeb-mohamed-77004b416) | habeebmohamed2016@gmail.com
