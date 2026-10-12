# Customer Retention & Churn Analysis

Why do telecom customers leave, and which customers are most at risk? This project analyses 7,043 customers from the IBM Telco Customer Churn dataset using SQL and Python, and turns the patterns into retention recommendations.

## Question

Roughly 1 in 4 customers churned. Which contract, service and billing characteristics explain who leaves, and where should a retention team focus first?

## Dataset

- IBM Telco Customer Churn: 7,043 customers, 21 columns (`Customer-Churn.csv`)
- Fields cover demographics, services (internet, phone, add-ons), contract type, billing and tenure

## Method

1. Load and clean the data in Python (pandas)
2. SQL analysis in SQLite (`churn_analysis_sql.ipynb`): churn rate by contract, service and payment method
3. Exploratory analysis and visualisation (`Customer_Retention_Analysis.ipynb`, matplotlib)
4. Business recommendations

## Key findings

**Overall churn rate: 26.5%** (1,869 of 7,043 customers).

| Segment | Churn rate |
|---|---|
| Month-to-month contract | 42.7% |
| One-year contract | 11.3% |
| Two-year contract | 2.8% |
| Fiber optic internet | 41.9% |
| DSL internet | 19.0% |
| No internet service | 7.4% |
| Electronic check payment | 45.3% |
| Automatic card / bank payment | 15.2% to 16.7% |

- **Contract type is the strongest signal.** Month-to-month customers churn about 15 times as often as two-year customers.
- **Tenure:** customers who churned stayed 18 months on average, versus 37.6 months for customers who stayed. 55.5% of churned customers left within their first 12 months.
- **Price:** churned customers paid more per month on average (USD 74.4 vs 61.3).

## Recommendations

- Offer discounts or upgrades that move month-to-month customers onto one-year or two-year contracts.
- Focus onboarding and check-ins on the first year, when over half of churn happens.
- Review fiber optic pricing and service quality, since it has more than double the churn of DSL.
- Encourage automatic payment methods over electronic check.

## Tools

Python, pandas, matplotlib, SQLite, Google Colab.

