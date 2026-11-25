# PhonePe Payment Insights Dashboard | Power BI

An interactive Power BI dashboard that analyses **300K digital payment transactions** from **108K unique users** to understand payment success, transaction value trends, user demographics and service performance.

![Dashboard preview](dashboard.png)

## Project Overview

Digital payment platforms handle huge volumes of transactions every day. This project turns raw transaction and user data into a single dashboard that answers questions such as:

- How many transactions were made, and what was their total value?
- How many users are active, and how often do payments succeed?
- How does transaction value change month to month?
- Which services and age groups drive the most activity?

## Key Metrics

| KPI | Value |
|---|---|
| Total Transactions | 300K |
| Total Transaction Value | Rs. 3.47bn |
| Unique Users | 108K |
| Successful Rate | 96.00% |

## Key Insights

- **Monthly trend:** monthly transaction value stayed between about Rs. 279M and Rs. 314M, with the highest month in **July (Rs. 314M)**.
- **Services:** **Loans** contributed the highest transaction value, ahead of Insurance, Money Transfer and Recharge & Bill payments.
- **Age segments:** **GenX** was the largest user group at about **42%** of users.
- **Reliability:** about **96%** of transactions were successful.

## Data Model

The report uses three linked tables:

| Table | Purpose | Example fields |
|---|---|---|
| `All_Users` | User details | User_ID, Name, Age Group |
| `All_Transactions` | Every payment | Service, Payment_Status |
| `Date` | Calendar table for time analysis | Month, Weekend |

Relationships connect transactions to users and to the date table, so every visual can be filtered by month, status, service or age group.

## DAX Measures

| Measure | What it calculates |
|---|---|
| Total Transaction | Total transaction value |
| Total Transaction Count | Number of transactions |
| Success Count | Number of successful transactions |
| Success Rate | Successful transactions as a percentage of all transactions |
| Total Id | Unique users |
| Previous Month Value | Transaction value in the previous month |
| Transaction Value MoM | Month-over-month growth |

Month-over-month growth formula:

```
MoM Growth % = ((Current Month Value - Previous Month Value) / Previous Month Value) * 100
```

## Dashboard Visuals

- **KPI cards:** total transactions, total value, unique users, success rate
- **Line chart:** transaction value over time (by month)
- **Donut chart:** age segment contribution
- **Column chart:** service-wise transaction value
- **Column chart:** top 5 users by transaction value
- **Slicers:** month and payment status

## Tools Used

- **Power BI Desktop:** data modelling, visuals and dashboard design
- **DAX:** measures for KPIs, success rate and month-over-month growth
- **Power Query:** data cleaning and preparation

## Repository Structure

```
phonepe-payment-insights-powerbi/
├── Project_Phone_pay.pbix   # Power BI report
├── dashboard.png            # Dashboard screenshot
└── README.md
```

## How to Use

1. Download `Project_Phone_pay.pbix`.
2. Open it in [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (free).
3. Use the month and payment status slicers to explore the data.

## What I Learned

- Building a data model with relationships and a date table
- Writing DAX measures for KPIs and month-over-month growth
- Designing a clean dashboard that is easy for non-technical users to read

## Author

**Om Danej**
Aspiring Data Analyst | SQL | Power BI | Python
[LinkedIn](https://linkedin.com/in/om-danej-analytics) | [GitHub](https://github.com/omdanej1122-afk) | omdanej1122@gmail.com

<img width="960" height="522" alt="image" src="https://github.com/user-attachments/assets/d17548c6-f794-44f2-a5ff-190c1d9f44c6" />
