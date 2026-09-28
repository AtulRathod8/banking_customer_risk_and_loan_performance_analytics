# 📊 Banking Customer Risk & Loan Performance Dashboard

[![Power BI](https://img.shields.io/badge/Dashboard-Power%20BI-yellow.svg)](https://powerbi.microsoft.com/)
[![Data Modeling](https://img.shields.io/badge/Schema-Relational-orange.svg)]()
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

An interactive Power BI analytics dashboard designed to evaluate consumer loan portfolios, quantify credit risk exposure, and support data-driven lending decisions for financial services.

---

## 🎯 Problem Statement
Retail banking and financial institutions face continuous exposure to credit default risks. The core challenge is understanding how to leverage historical data to **minimize the risk of losing money** while lending to customers. Financial institutions need clear analytical frameworks to accurately assess whether an applicant is likely to repay a loan before approving credit.

---

## 💡 Solution
This project delivers a comprehensive **Power BI Dashboard** that transforms raw client and banking data into actionable visual insights. The solution enables risk managers and loan officers to make informed, automated decisions based on applicant profiles:
* **Approve Loans:** For clients identified with low risk and a high likelihood of repayment.
* **Decline / Restrict Loans:** For applicants flagged with high credit risk and poor historical performance indicators.

---

## 📂 Dataset & Relational Architecture
The project utilizes a multi-table relational dataset connected via primary and foreign keys to maintain data integrity across banking operations. 

The core schema comprises the following interconnected tables:
1. **`Banking Relationship`**: Captures details regarding client-bank interactions, account types, and service ties.
2. **`Client-Banking`**: Stores core client demographic data, financial histories, and loan application markers.
3. **`Gender`**: Categorizes demographic distributions for segment-based risk analysis.
4. **`Investment Advisor`**: Tracks assigned advisors and portfolio oversight details.
5. **`Period`**: Time dimension table enabling trend analysis across months, quarters, and years.

---

## 🧹 Data Cleaning & Feature Engineering
To prepare the dataset for effective dashboard visualization, key transformation steps were performed:
* **Timeline Tracking:** Created a brand new calculated column named **`Engagement Timeframe`** within the `Client-Banking` table. This metric calculates and categorizes the duration of the client's relationship with the bank, serving as a vital behavioral feature for risk evaluation.

---

## 📈 Key Performance Indicators (KPIs) Tracked
The dashboard monitors critical financial metrics to evaluate portfolio health and profitability:
* **Total Portfolio Value / Lending Volume:** Aggregate monetary value of all active loans issued.
* **Default Rate / Non-Performing Loan (NPL) Ratio:** Percentage of total loans classified as defaulted or severely delinquent.
* **Loan Approval Rate:** Proportion of total loan applications approved versus rejected based on risk criteria.
* **Portfolio Yield / Average Interest Rate:** Average rate of return generated across the lending portfolio.
* **Average Client Tenure (`Engagement Timeframe`):** Mean duration of customer relationships with the institution.

---

## 💡 Important Insights Discovered
Analysis through the Power BI dashboard revealed several critical trends for risk mitigation:
1. **Tenure Mitigates Risk:** Clients with an extended **`Engagement Timeframe`** (e.g., multi-year banking history) demonstrate a substantially lower default rate compared to newly onboarded clients.
2. **The Risk-Yield Tradeoff:** High-risk applicant tiers offer higher interest yields, but they disproportionately drive up the portfolio's default losses, indicating a need for stricter underwriting thresholds for high-risk bands.
3. **Advisor Portfolio Variance:** Performance benchmarking across **Investment Advisors** highlights distinct variations in portfolio default rates, showing that proactive account monitoring directly correlates with lower NPL ratios.
4. **Demographic Repayment Patterns:** Segment-level breakdowns reveal specific risk concentrations across demographics, enabling the bank to fine-tune its targeted lending strategies.

---

## 📊 Dashboard Features & Visuals

* **Executive Summary / KPI Overview:** High-level metrics tracking total loans, approval rates, portfolio yield, and default percentages.
* **Applicant Risk Profiling:** Visualizes client risk scores against historical repayment performance.
* **Engagement & Tenure Analysis:** Uses the `Engagement Timeframe` feature to correlate customer loyalty/tenure with lower default risks.
* **Advisor Portfolio Breakdown:** Evaluates loan performance metrics segmented across different investment advisors.
* **Interactive Slicers:** Dynamic filtering by period, gender, relationship type, and risk tiers.

---

## 🛠️ Project Structure

```text
banking-risk-dashboard/
│
├── data/                  # Cleaned CSV files / data sources used for Power BI import
├── dashboard/             # Power BI (.pbix) dashboard file
├── queries/               # SQL queries or Power Query M scripts used for data modeling
├── assets/                # Dashboard screenshots and architecture diagrams
└── README.md              # Project documentation
