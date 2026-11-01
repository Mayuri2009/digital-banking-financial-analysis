## 1. Purpose

This KPI catalog defines the business meaning, calculation logic, and intended use of the key financial and operational metrics in the project.

It establishes consistent definitions for PostgreSQL analysis and Power BI reporting, helping prevent different calculations of the same KPI across project deliverables.

All financial amounts will be reported in **US dollars (USD, $)**.

## 2. Financial Performance KPIs

### KPI-01: Total Revenue

| Attribute | Definition |
|---|---|
| KPI ID | DBFPA-KPI-01 |
| Business Definition | Total revenue recorded during the selected reporting period |
| Calculation | Sum of revenue amounts |
| SQL Logic | `SUM(revenue_amount)` |
| Unit | USD ($) |
| Business Use | Measure overall revenue generation |

**Interpretation:** Indicates the total revenue recorded during the selected period. It does not represent net income or profit.

### KPI-02: Monthly Revenue

| Attribute | Definition |
|---|---|
| KPI ID | DBFPA-KPI-02 |
| Business Definition | Total revenue recorded for each calendar month |
| Calculation | Sum of revenue amounts grouped by month |
| SQL Logic | `SUM(revenue_amount)` grouped by revenue month |
| Unit | USD ($) |
| Business Use | Monitor monthly revenue trends |

### KPI-03: Revenue by Source

| Attribute | Definition |
|---|---|
| KPI ID | DBFPA-KPI-03 |
| Business Definition | Revenue contribution from each revenue source |
| Calculation | Sum of revenue amounts grouped by revenue source |
| SQL Logic | `SUM(revenue_amount)` grouped by revenue source |
| Unit | USD ($) |
| Business Use | Understand revenue composition |

Revenue sources may include transaction fees and monthly account fees.

### KPI-04: Revenue per Customer

| Attribute | Definition |
|---|---|
| KPI ID | DBFPA-KPI-04 |
| Business Definition | Average revenue generated per distinct customer in the selected period |
| Calculation | Total revenue ÷ distinct customers associated with that revenue |
| SQL Logic | `SUM(revenue_amount) / COUNT(DISTINCT customer_id)` |
| Unit | USD ($) per customer |
| Business Use | Compare average revenue contribution across customer segments |

The customer population used in the denominator must be clearly defined. Revenue per customer is **not customer profit**.

### KPI-05: Revenue Mix Percentage

| Attribute | Definition |
|---|---|
| KPI ID | DBFPA-KPI-05 |
| Business Definition | Percentage of total revenue attributable to a particular revenue source or segment |
| Calculation | Revenue for category ÷ total revenue × 100 |
| SQL Logic | Category revenue divided by total revenue |
| Unit | Percentage |
| Business Use | Identify the largest contributors to revenue |

## 3. Customer Analytics KPIs

### KPI-06: Total Customers

| Attribute | Definition |
|---|---|
| KPI ID | DBFPA-KPI-06 |
| Business Definition | Number of distinct customers in the customer dataset |
| Calculation | Count of distinct customer IDs |
| SQL Logic | `COUNT(DISTINCT customer_id)` |
| Unit | Customers |
| Business Use | Understand the size of the customer base |

### KPI-07: Active Customers

| Attribute | Definition |
|---|---|
| KPI ID | DBFPA-KPI-07 |
| Business Definition | Distinct customers with at least one successful transaction during the selected period |
| Calculation | Count of distinct customer IDs with successful transactions |
| SQL Logic | `COUNT(DISTINCT customer_id)` filtered to successful transactions |
| Unit | Customers |
| Business Use | Measure customer activity |

This is a transaction-based activity definition. It does not necessarily represent every possible definition of an active banking customer.

### KPI-08: New Customers

| Attribute | Definition |
|---|---|
| KPI ID | DBFPA-KPI-08 |
| Business Definition | Customers whose recorded acquisition or signup date falls within the selected period |
| Calculation | Count of distinct customers by signup month |
| SQL Logic | `COUNT(DISTINCT customer_id)` grouped by signup month |
| Unit | Customers |
| Business Use | Monitor customer acquisition |

### KPI-09: Customer Retention Rate

| Attribute | Definition |
|---|---|
| KPI ID | DBFPA-KPI-09 |
| Business Definition | Percentage of customers active in a prior period who are also active in the following period |
| Calculation | Customers active in both periods ÷ customers active in the prior period × 100 |
| SQL Logic | Compare distinct customer IDs across consecutive periods |
| Unit | Percentage |
| Business Use | Monitor continued customer activity |

For this project, retention will be based on successful transaction activity. The reporting period—such as month-to-month—must be stated with the result.

## 4. Transaction Performance KPIs

### KPI-10: Transaction Volume

| Attribute | Definition |
|---|---|
| KPI ID | DBFPA-KPI-10 |
| Business Definition | Number of transactions recorded during the selected period |
| Calculation | Count of transaction IDs |
| SQL Logic | `COUNT(transaction_id)` |
| Unit | Transactions |
| Business Use | Measure transaction activity |

### KPI-11: Total Transaction Value

| Attribute | Definition |
|---|---|
| KPI ID | DBFPA-KPI-11 |
| Business Definition | Total monetary value of transactions during the selected period |
| Calculation | Sum of transaction amounts |
| SQL Logic | `SUM(transaction_amount)` |
| Unit | USD ($) |
| Business Use | Measure the monetary scale of transaction activity |

Transaction value and revenue are different measures. The total value of customer transactions must not be treated as bank revenue.

### KPI-12: Successful Transaction Rate

| Attribute | Definition |
|---|---|
| KPI ID | DBFPA-KPI-12 |
| Business Definition | Percentage of recorded transactions with a successful status |
| Calculation | Successful transactions ÷ all recorded transactions × 100 |
| SQL Logic | Successful transaction count divided by total transaction count |
| Unit | Percentage |
| Business Use | Monitor transaction completion performance |

### KPI-13: Failed Transaction Rate

| Attribute | Definition |
|---|---|
| KPI ID | DBFPA-KPI-13 |
| Business Definition | Percentage of recorded transactions with a failed status |
| Calculation | Failed transactions ÷ all recorded transactions × 100 |
| SQL Logic | Failed transaction count divided by total transaction count |
| Unit | Percentage |
| Business Use | Identify transaction performance issues |

The success and failure rates use the same transaction population and should be interpreted alongside any other transaction statuses present in the dataset.

## 5. Operating Cost KPIs

### KPI-14: Total Operating Costs

| Attribute | Definition |
|---|---|
| KPI ID | DBFPA-KPI-14 |
| Business Definition | Total operating costs recorded during the selected period |
| Calculation | Sum of operating cost amounts |
| SQL Logic | `SUM(cost_amount)` |
| Unit | USD ($) |
| Business Use | Monitor operating expenditure |

### KPI-15: Operating Cost by Category

| Attribute | Definition |
|---|---|
| KPI ID | DBFPA-KPI-15 |
| Business Definition | Operating costs grouped by cost category |
| Calculation | Sum of cost amounts by category |
| SQL Logic | `SUM(cost_amount)` grouped by cost category |
| Unit | USD ($) |
| Business Use | Understand the composition of operating costs |

### KPI-16: Operating Cost-to-Revenue Ratio

| Attribute | Definition |
|---|---|
| KPI ID | DBFPA-KPI-16 |
| Business Definition | Operating costs as a proportion of revenue for the same reporting period |
| Calculation | Operating costs ÷ revenue × 100 |
| SQL Logic | Total operating costs divided by total revenue |
| Unit | Percentage |
| Business Use | Compare operating cost levels with revenue |

This ratio is meaningful only when the revenue and cost populations and reporting periods are aligned. It is not automatically equivalent to a formal banking efficiency ratio.

### KPI-17: Revenue Less Operating Costs

| Attribute | Definition |
|---|---|
| KPI ID | DBFPA-KPI-17 |
| Business Definition | Revenue minus the operating costs included in the analysis |
| Calculation | Total revenue − total operating costs |
| SQL Logic | Revenue aggregate minus operating cost aggregate |
| Unit | USD ($) |
| Business Use | Provide a simplified view of revenue relative to included operating costs |

This measure is not net income or a complete profit measure. It excludes any costs, taxes, adjustments, or other financial items not represented in the dataset.

## 6. Customer Support KPIs

### KPI-18: Support Ticket Volume

| Attribute | Definition |
|---|---|
| KPI ID | DBFPA-KPI-18 |
| Business Definition | Number of support tickets recorded during the selected period |
| Calculation | Count of support ticket IDs |
| SQL Logic | `COUNT(ticket_id)` |
| Unit | Tickets |
| Business Use | Monitor customer support demand |

### KPI-19: Average Resolution Time

| Attribute | Definition |
|---|---|
| KPI ID | DBFPA-KPI-19 |
| Business Definition | Average elapsed time between ticket creation and resolution |
| Calculation | Average resolution timestamp minus ticket creation timestamp |
| SQL Logic | Average elapsed time for resolved tickets |
| Unit | Hours |
| Business Use | Evaluate customer support resolution performance |

Only tickets with valid resolution timestamps will be included. The exact calculation will be based on the available fields in the support dataset.

## 7. Customer Profitability Considerations

Customer profitability requires customer-level revenue and customer-level costs.

The project will distinguish between:

- **Revenue per customer:** Revenue divided by a defined customer population.
- **Revenue less operating costs:** Total revenue minus the operating costs included in the analysis.
- **Customer profit:** Customer revenue minus costs reasonably attributable to that customer.

The available operating cost data may be recorded by month and cost category rather than by customer. Therefore, customer-level profitability will only be calculated if a defensible allocation method can be established.

If allocation is not supported, the project will report revenue contribution and segment-level financial comparisons without presenting them as customer profit.

## 8. KPI Reporting Standards

The following standards will apply across PostgreSQL and Power BI:

1. Financial values will use USD ($).
2. Financial measures will use consistent decimal precision.
3. Percentages will be displayed with a consistent number of decimal places.
4. Transaction value will be distinguished from revenue.
5. Revenue will be distinguished from profit.
6. KPI definitions will remain consistent across SQL queries and dashboard measures.
7. Reporting periods and filters will be stated where they affect interpretation.
8. Unsupported measures will be excluded or clearly labeled as unavailable.

## 9. Conclusion

This KPI catalog establishes the metric definitions for the Digital Banking Financial Performance & Customer Profitability Analysis project.

The catalog will guide PostgreSQL query development, Power BI measures, testing, reconciliation, and executive reporting.



