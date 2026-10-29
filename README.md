# Meridian Capital Markets — Financial Data Analytics

## Project Overview

Meridian Capital Markets is a financial data analytics project built using a synthetic investment banking dataset containing approximately **4.75 million rows across 25 tables**.

The dataset represents financial market operations, including trading, settlements, positions, market risk, profitability, client information, and regulatory compliance.

The project focuses on relational data handling, data profiling, data quality assessment, and financial data analysis.

**Disclaimer:** This project uses synthetic data for educational and portfolio purposes. It does not contain actual customer transactions or confidential banking records.

## Dataset Overview

The dataset consists of 25 tables divided into two categories.

### Dimension Tables (10)

- Clients
- Employees
- Offices
- Desks
- Instruments
- Counterparties
- Currencies
- Products
- Accounts
- Risk Limits

### Fact Tables (15)

- Trades
- Trade Settlements
- Positions
- Prices
- Profit and Loss (P&L)
- Value at Risk (VaR)
- Cash Flows
- Corporate Actions
- Compliance Alerts
- KYC Reviews
- Credit Exposures
- Collateral
- Order Book
- Audit Log
- Margin Calls

The dataset also includes a data dictionary containing column definitions and key relationships between tables.

## Tools & Technologies

| Category | Technology |
|---|---|
| Programming Language | Python |
| Database | PostgreSQL |
| Data Manipulation | Pandas, NumPy |
| Query Language | SQL |
| Development Environment | Visual Studio Code |
| Notebook Environment | Jupyter Notebook |
| Version Control | Git, GitHub |

## Project Workflow

1. **Data Ingestion:** Load CSV datasets into PostgreSQL.
2. **Database Setup:** Organize the data into relational tables.
3. **Data Profiling:** Examine row counts, columns, data types, missing values, distinct values, and duplicate records.
4. **Data Quality Assessment:** Investigate missing values, duplicate records, and potential inconsistencies.
5. **SQL Analysis:** Analyze relationships between tables and investigate financial and operational business questions.
6. **Reporting and Visualization:** Prepare analytical reports and dashboards as the project progresses.

## Data Quality Assessment

The source dataset contains intentional data quality issues that require investigation.

- **Missing Values:** Approximately 3% of values in `01_dim_clients.kyc_status` are missing.
- **Missing Trade Prices:** Approximately 0.5% of values in `11_fact_trades.price` are missing.
- **Duplicate Trade Records:** Approximately 0.1% duplicate rows exist in `11_fact_trades`, including repeated `trade_id` values.

These issues provide opportunities to investigate data completeness, uniqueness, and consistency.

## Work Completed

- Loaded CSV datasets into PostgreSQL.
- Started data profiling using Python and Pandas.
- Identified duplicate records in the trades fact table for further investigation.

## Potential Business Questions

The dataset can be used to investigate the following business questions:

- What is the trading volume across different instruments, desks, and clients?
- What proportion of trades settle successfully?
- Which trades require settlement exception analysis?
- How do profit and loss figures vary across desks and products?
- Which counterparties have the largest credit exposures?
- What compliance alerts and KYC review statuses require attention?
- How can data quality issues affect downstream financial reporting?

## Repository Structure

```text
meridian-capital-markets-analytics/
│
├── README.md
├── data_dictionary.csv
│
├── notebooks/
│   └── data_profiling.ipynb
│
├── sql/
│   └── analysis_queries.sql
│
└── dashboards/
    └── dashboard_screenshots/
```

## Future Improvements

- Complete data profiling across all 25 tables.
- Validate primary keys, duplicate records, and missing values.
- Document relationships between tables using an Entity Relationship Diagram (ERD).
- Develop SQL queries to answer business questions.
- Improve database performance through appropriate indexing and query optimization.
- Build a Power BI dashboard to communicate financial and operational insights.
- Document analytical findings and business recommendations.

## How to Use

1. Clone or download the repository.
2. Set up PostgreSQL and create the required database and schema.
3. Place the source CSV files in the appropriate local directory.
4. Configure the database connection in your local scripts.
5. Run the Python profiling scripts or Jupyter Notebook.
6. Use SQL queries to explore and analyze the data.

##  Data Dictionary

The data dictionary provides column definitions and information about the structure of the 25 tables used in this project.

It helps users understand the dataset, identify relevant columns, and explore relationships between tables.

 **[View Data Dictionary](./data_dictionary.csv)**

## Project Disclaimer

This project is intended for educational purposes and portfolio development. The dataset is synthetic and does not represent the actual operations or confidential information of any financial institution.
