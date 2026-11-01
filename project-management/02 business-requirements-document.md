# Business Requirements Document (BRD)

## 1. Document Information

| Field | Details |
|---|---|
| Project Name | Digital Banking Financial Performance & Customer Profitability Analysis |
| Document Type | Business Requirements Document |
| Project ID | DBFPA |
| Version | 1.0 |
| Status | Draft |
| Analysis Period | January–December 2025 |
| Currency | USD ($) |
| Data Source | Synthetic portfolio dataset |
| Prepared By | Portfolio Project Analyst |

---

## 2. Business Background

Digital banks operate in a competitive environment where understanding customer behavior, revenue generation, transaction performance, and operating costs is essential for sustainable growth.

A bank may experience increasing transaction volumes and customer acquisition while still facing challenges such as declining revenue per customer, inefficient operating costs, high transaction failure rates, or weak customer retention.

This project simulates a financial analysis engagement for a fictional digital bank. The analysis will use synthetic customer, transaction, revenue, customer support, and operating cost data to evaluate financial and operational performance during 2025.

The findings will be presented through PostgreSQL analysis and a Power BI dashboard to support business decision-making.

## 3. Business Problem Statement

The fictional digital bank requires a consolidated view of its financial and operational performance.

Currently, business stakeholders lack a single analytical view that connects:

- Revenue trends and revenue sources
- Customer activity and customer segments
- Transaction volumes, values, and success rates
- Customer support performance
- Operating cost trends
- Customer-level financial contribution, where supported by the available data

The project will address this gap by creating a structured analytical solution that helps stakeholders identify performance trends, potential risks, and opportunities for improvement.

## 4. Business Objectives

The project aims to:

1. Analyze monthly and annual revenue performance.
2. Identify the customer segments contributing most to revenue.
3. Understand customer activity and transaction behavior.
4. Evaluate transaction success and failure performance.
5. Examine operating cost trends and cost composition.
6. Explore customer financial contribution using defensible revenue and cost measures.
7. Identify opportunities to improve revenue performance, operational efficiency, and customer experience.
8. Present findings through an interactive Power BI dashboard.

## 5. Stakeholders

The following stakeholders are simulated for this portfolio project.

| Stakeholder | Responsibility | Information Required |
|---|---|---|
| Finance Manager | Reviews financial performance | Revenue, costs, financial trends |
| Head of Digital Banking | Oversees digital banking performance | Customer activity, transaction performance |
| Customer Analytics Manager | Evaluates customer behavior | Segments, activity, retention indicators |
| Operations Manager | Monitors operational efficiency | Transaction failures, support performance |
| Financial Analyst | Performs financial analysis | Revenue, costs, KPIs, business insights |
| BI Analyst | Develops analytical reporting | Data model, SQL outputs, Power BI dashboard |

## 6. Business Questions

### 6.1 Financial Performance

- How did total revenue change throughout 2025?
- Which revenue sources contributed the most?
- Which months had the highest and lowest revenue?
- How does revenue vary by customer segment and region?
- What proportion of revenue comes from transaction fees versus monthly account fees?

### 6.2 Customer Analytics

- Which customer segments generate the highest revenue?
- How does customer activity vary by segment?
- Which acquisition channels contribute the most customers?
- What trends can be observed in customer acquisition and retention?
- How does revenue per customer vary across customer segments?

### 6.3 Transaction Performance

- What is the total transaction volume and transaction value?
- What percentage of transactions are successful or failed?
- How do transaction outcomes vary by transaction type?
- Which months have the highest transaction activity?
- Is transaction performance associated with differences in revenue?

### 6.4 Operating Costs

- How do operating costs change over time?
- Which cost categories contribute the most to total operating costs?
- How do operating costs compare with revenue trends?
- What opportunities may exist to improve operating efficiency?

### 6.5 Customer Financial Contribution

- Which customers or segments contribute the most revenue?
- How does revenue per customer vary across segments?
- Where can customer-level or segment-level cost allocation be supported by the data?
- Which customers or segments may warrant further financial investigation?

**Important:** Revenue per customer is not the same as customer profit. Customer profitability will only be reported where cost allocation is supported by a reasonable and documented methodology.

## 7. Scope

### 7.1 In Scope

- Analysis of synthetic 2025 digital banking data
- PostgreSQL table creation and data import
- SQL-based financial and customer analysis
- Revenue and operating cost analysis
- Customer segment and transaction analysis
- Customer support performance analysis
- Power BI data modeling and dashboard development
- KPI calculations and visual reporting
- Reconciliation and analytical testing
- Business insights and recommendations
- Executive summary presentation
- GitHub portfolio documentation

### 7.2 Out of Scope

- Use of real customer or confidential banking data
- Live banking system integration
- Actual banking transactions or payment processing
- Regulatory reporting or compliance certification
- Credit risk scoring or loan underwriting
- Forecasting or predictive machine learning
- Production deployment
- Claims of actual financial impact for a real bank
- Definitive customer profitability where costs cannot be allocated reliably

## 8. Functional Requirements

| Requirement ID | Requirement | Priority |
|---|---|---|
| DBFPA-FR-01 | The solution shall organize customer, transaction, revenue, support, and operating cost data for analysis. | High |
| DBFPA-FR-02 | The solution shall calculate total revenue and revenue by month. | High |
| DBFPA-FR-03 | The solution shall break down revenue by revenue source, customer segment, and region. | High |
| DBFPA-FR-04 | The solution shall calculate transaction volume and transaction value. | High |
| DBFPA-FR-05 | The solution shall calculate transaction success and failure rates. | High |
| DBFPA-FR-06 | The solution shall analyze customer activity and revenue contribution by segment. | High |
| DBFPA-FR-07 | The solution shall analyze operating costs by month and cost category. | High |
| DBFPA-FR-08 | The solution shall analyze customer support volume and performance. | Medium |
| DBFPA-FR-09 | The Power BI dashboard shall provide filters for relevant dimensions such as month, segment, and region. | High |
| DBFPA-FR-10 | The solution shall provide a documented basis for any customer profitability or cost allocation analysis. | High |
| DBFPA-FR-11 | The solution shall present business findings and recommendations supported by analysis. | High |

## 9. Non-Functional Requirements

| Requirement ID | Requirement | Requirement Description |
|---|---|---|
| DBFPA-NFR-01 | Accuracy | KPI calculations shall use documented definitions and consistent logic. |
| DBFPA-NFR-02 | Traceability | Key dashboard metrics shall be traceable to SQL queries and source tables. |
| DBFPA-NFR-03 | Usability | Dashboard pages shall be clearly labeled and understandable to business stakeholders. |
| DBFPA-NFR-04 | Consistency | Currency, date, and KPI definitions shall be consistent across the project. |
| DBFPA-NFR-05 | Privacy | The project shall use synthetic data and shall not expose real customer information. |
| DBFPA-NFR-06 | Maintainability | SQL scripts and project documentation shall use clear naming conventions. |
| DBFPA-NFR-07 | Reproducibility | The documented workflow shall allow another analyst to understand and reproduce the analysis. |

## 10. Key KPI Requirements

The project will define and document its KPI calculations in the separate `kpi-catalog.md` file.

The initial KPI list includes:

| KPI | Business Purpose |
|---|---|
| Total Revenue | Measure overall revenue generation |
| Monthly Revenue | Monitor revenue trends over time |
| Revenue by Source | Understand revenue composition |
| Revenue per Customer | Compare revenue contribution across customers or segments |
| Transaction Volume | Measure transaction activity |
| Transaction Value | Measure the total monetary value of transactions |
| Transaction Success Rate | Monitor successful transaction performance |
| Transaction Failure Rate | Identify transaction performance issues |
| Active Customers | Measure customer activity |
| Customer Acquisition | Monitor new customer growth |
| Customer Retention | Understand continued customer engagement |
| Total Operating Costs | Monitor operating expenditure |
| Cost by Category | Understand cost composition |
| Revenue-to-Cost Comparison | Compare revenue and operating costs at an appropriate reporting level |
| Support Ticket Volume | Monitor customer support demand |

KPI definitions will specify the numerator, denominator, date basis, relevant filters, and interpretation wherever applicable.

## 11. Data Requirements

The analysis will use the following synthetic datasets:

| Dataset | Intended Use |
|---|---|
| Customers | Customer attributes, segments, regions, acquisition channels |
| Transactions | Transaction activity, amounts, types, statuses, dates |
| Revenue | Revenue source, amount, date, and customer linkage where available |
| Customer Support | Support ticket volume, categories, status, and resolution measures |
| Operating Costs | Monthly operating cost amounts by category |

The analysis will use GBP as the reporting currency and January–December 2025 as the primary reporting period.

Monthly account fees may not have a transaction ID because they are not necessarily associated with an individual transaction. They will be analyzed using their available revenue records and appropriate customer or date relationships.

## 12. Assumptions and Constraints

### Assumptions

- The datasets represent a fictional digital bank.
- All data is synthetic and created for portfolio demonstration.
- The reporting period is January–December 2025.
- GBP is the reporting currency.
- Data fields and KPI definitions are sufficiently documented for analysis.
- Stakeholder roles and business needs are simulated.

### Constraints

- The analysis is limited to the fields included in the synthetic datasets.
- No real banking systems or live customer information are available.
- Some financial measures may not support customer-level allocation.
- Findings demonstrate analytical reasoning and do not represent actual banking performance.
- The project is independently developed as a portfolio exercise.

## 13. Expected Deliverables

The project will produce:

1. Project initiation document
2. Business requirements document
3. Stakeholder analysis
4. KPI catalog
5. Agile planning artifacts
6. Banking process flow
7. Structured data files and data dictionary
8. PostgreSQL schema and analytical SQL scripts
9. Power BI financial performance dashboard
10. Testing cases and reconciliation documentation
11. Executive summary presentation
12. GitHub repository documentation

## 14. Business Acceptance Criteria

The project will be considered complete when:

- All agreed datasets are represented in the analytical data model.
- Core financial and operational KPIs have documented definitions.
- SQL queries answer the defined business questions.
- Revenue and operating cost analysis can be reconciled to the source data.
- The Power BI dashboard presents the agreed KPIs and supports relevant filtering.
- Key dashboard metrics can be traced to SQL logic or documented calculations.
- Analytical limitations are clearly communicated.
- Recommendations are supported by findings from the synthetic dataset.
- The project artifacts are organized and documented in GitHub.

