# Loan Default Analysis Dashboard

An interactive **Power BI dashboard** for exploring loan defaults, borrower demographics, lending patterns, and financial risk indicators. The repository contains the Power BI report (`Dashboard.pbix`) and the raw loan dataset (`Loan_default.csv`).

## Project Overview

The dashboard is designed to help explore questions such as:

- How do default rates vary by employment type and year?
- How do loan amounts differ across loan purposes and age groups?
- How are borrower demographics and credit-score categories associated with lending patterns?
- How do financial and household characteristics relate to loan risk?

> **Important:** This is an exploratory analytics project. The visualizations show patterns in the supplied dataset and should not be interpreted as proof of causation or as a standalone basis for lending decisions.

## Dashboard Pages

### 1. Loan Default & Overview
Provides a high-level view of loan activity, including:
- Loan amount by purpose
- Average income by employment type
- Default rate by employment type
- Loan amount by age group
- Default rate by year

### 2. Applicant Demographics & Financial Profile
Explores applicant and loan characteristics, including:
- Median loan amount by credit-score category
- Average loan amount for higher-credit-score applicants by age group and marital status
- Total loan amount by credit-score bins
- Loan amount for middle-aged adults by mortgage and dependent status
- Number of loans by education type

### 3. Financial Risk Metrics
Focuses on financial-risk exploration, including year-to-date loan amount by credit-score bins and marital status, alongside additional trend and decomposition visuals.

*Visuals and available interactions are defined in the Power BI report. Open the PBIX file in Power BI Desktop to inspect the full report and interact with its filters and visuals.*

## Dataset

**File:** `Loan_default.csv`

The CSV contains **255,347 rows and 19 columns**.

| Column | Description |
|---|---|
| `LoanID` | Loan identifier |
| `Age` | Borrower's age |
| `Income` | Borrower's income |
| `LoanAmount` | Loan amount |
| `CreditScore` | Borrower's credit score |
| `MonthsEmployed` | Number of months employed |
| `NumCreditLines` | Number of credit lines |
| `InterestRate` | Loan interest rate |
| `LoanTerm` | Loan term |
| `DTIRatio` | Debt-to-income ratio |
| `Education` | Education category |
| `EmploymentType` | Employment category |
| `MaritalStatus` | Marital status |
| `HasMortgage` | Whether the borrower has a mortgage |
| `HasDependents` | Whether the borrower has dependents |
| `LoanPurpose` | Purpose of the loan |
| `HasCoSigner` | Whether the loan has a co-signer |
| `Default` | Default indicator (`1` = default, `0` = no default) |
| `Loan Date (DD/MM/YYYY)` | Date field supplied with the dataset |

In the supplied CSV, the date column's label says `DD/MM/YYYY`, but sample values such as `10/15/2018` appear to use **month/day/year** formatting. Verify the column's locale and data type when importing it into Power BI.

### Quick dataset note

In the supplied data, `Default = 1` appears in approximately **11.61%** of rows. This is a descriptive statistic for this dataset, not a forecast of future default risk.

## Tools Used

- **Microsoft Power BI Desktop** — report authoring and interactive visualization
- **CSV** — raw data source

## Future Improvements

- Add a screenshot or GIF preview of the dashboard.
- Document any Power Query cleaning steps and DAX measures used in the report.
- Add a data dictionary with business definitions and calculation logic for key metrics.
- Include a methodology section describing how age groups, credit-score bins, and default rates are calculated.
