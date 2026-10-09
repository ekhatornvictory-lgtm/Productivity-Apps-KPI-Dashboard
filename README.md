# Productivity Apps KPI Dashboard
### Excel Dashboard | Revenue • Profit • Cash • Budget & Prior-Year Performance

An interactive Microsoft Excel dashboard for monitoring financial performance across a portfolio of productivity applications. The dashboard compares actual results with prior-year performance and budget, tracks year-to-date profit trends, and supports product-level performance review.

> **Portfolio note:** The workbook's displayed selection is **Productivity Apps, June 2017**. Findings below are based on the values stored in the uploaded workbook. Treat the data as a sample/dashboard case study unless you can verify the source system and business context.

![Productivity Apps KPI Dashboard](https://github.com/ekhatornvictory-lgtm/Productivity-Apps-KPI-Dashboard/blob/22866233bc3b3de4c2e3bdd34a289353d94674c0/Excel%20KPI.png)

## Project Overview

This project demonstrates how Excel can turn a multi-product financial dataset into a decision-support dashboard. It brings together:
- **Headline KPIs:** Revenue, Profit, and Cash.
- **Variance analysis:** Actual vs. prior year (PY) and actual vs. budget.
- **Product-level performance:** Revenue, profit, and cash by application.
- **Trend analysis:** Cumulative profit progression through the selected year, with prior-year and budget comparisons.
- **Interactive exploration:** Year, month, division, KPI, and top/bottom selections in the workbook.

## Business Questions

1. Is the selected division meeting its revenue, profit, and cash targets?
2. How does current performance compare with the prior year?
3. Which applications contribute most to revenue and profit?
4. Which products are underperforming against prior year or budget?
5. How has year-to-date profit developed month by month?

## Key Findings — Productivity Apps, June 2017

| KPI | Actual | Prior Year | YoY change | Budget | Actual vs. budget |
|---|---:|---:|---:|---:|---:|
| Revenue | $162,643 | $159,773 | +1.8% | $164,760 | $-2,117 (-1.3%) |
| Profit | $9,359 | $9,241 | +1.3% | $9,443 | $-84 (-0.9%) |
| Cash | $103,058 | $103,723 | -0.6% | $104,426 | $-1,368 (-1.3%) |

### What the numbers suggest

- **Revenue is growing year over year**, but the selected division is below its June budget. The positive year-over-year comparison should not hide the missed target.
- **Profit is slightly above prior year but below budget.** This suggests modest improvement, with an opportunity to close the remaining budget gap through product mix, pricing, or cost control.
- **Cash is lower than both prior year and budget.** Review collections, payment timing, working-capital needs, and the cash contribution of individual products before drawing a cause-and-effect conclusion.
- The cumulative profit trend rises through June, reaching **$9,359**. Because these values are cumulative/YTD-style figures, they should not be interpreted as each month's standalone profit.

### Product-level highlights

**Highest revenue applications in the displayed Productivity Apps group:**
- **Blend** — $17,990 revenue; profit $1,166.
- **Pet Feed** — $16,735 revenue; profit $800.
- **Mirrrr** — $15,627 revenue; profit $1,996.

**Highest profit applications in the displayed Productivity Apps group:**
- **Mirrrr** — $1,996 profit on $15,627 revenue.
- **Voltage** — $1,613 profit on $15,117 revenue.
- **Blend** — $1,166 profit on $17,990 revenue.

**Lower-profit applications to review:**
- **Right App** — $96 profit; investigate performance drivers before deciding on corrective action.
- **Halotot** — $150 profit; investigate performance drivers before deciding on corrective action.
- **WenCaL** — $240 profit; investigate performance drivers before deciding on corrective action.

These are descriptive rankings for the selected period, not proof that a product is inherently more or less profitable. Confirm costs, seasonality, product lifecycle, and data definitions before taking action.

## Data Cleaning & Preparation

The workbook is a pre-built dashboard model rather than a plain raw-data export. The `Data` sheet includes a note that the source is connected to a database via an add-in, and contains formulas/named references alongside values. For a reproducible analysis, the following checks should be performed before publishing refreshed results:

1. **Validate the source connection** — confirm the database/add-in refresh completes successfully and document the source and refresh date.
2. **Check the reporting grain** — establish whether each row represents an application, division subtotal, or other aggregation. Do not mix subtotal rows (for example, division totals) with product rows when calculating totals.
3. **Standardize dimensions** — normalize application and division names, reporting months, years, and metric labels.
4. **Validate numeric fields** — ensure revenue, profit, cash, and budget values are numeric and consistently scaled/currency-formatted.
5. **Check missing and duplicate records** — review product names, unique keys, and month/metric combinations before calculating variances.
6. **Validate comparison logic** — confirm prior-year and budget values use the same period, division, currency, and reporting definition as actuals.
7. **Review formulas and dependencies** — confirm named ranges such as year/month selectors and any external add-in references are available in the target environment.
8. **Reconcile totals** — compare product-level sums with division totals and investigate any mismatch rather than forcing values to agree.

**Transparency:** No undocumented changes to the source values are claimed in this repository. The cleaning steps above describe validation and preparation checks recommended for a robust refresh. The workbook may rely on Excel features, named ranges, or an external database add-in; interactive controls and formulas may not behave identically in every spreadsheet application.

## Trend Analysis

The dashboard's profit chart shows the selected year's cumulative profit against prior-year and budget references.

- Track the direction and pace of cumulative profit month by month.
- Compare actual against prior year to separate growth from target attainment.
- Use the budget line as an early-warning reference for underperformance.
- Drill into product-level variance to identify which applications explain the overall movement.
- Avoid treating cumulative values as monthly flows; calculate monthly profit separately if the business question requires month-only results.

## Business Recommendations

### 1. Close the revenue budget gap
Review products with negative budget variance, focusing first on material revenue contributors. Test whether the gap is driven by volume, price, customer mix, seasonality, or delayed recognition.

### 2. Protect and improve profit
Use product-level profit and profit variance together. Prioritize high-revenue products with weak margins for pricing, discount, or cost-to-serve review; protect products that combine strong revenue with healthy profit.

### 3. Investigate cash performance
Reconcile cash movement to collections, payment schedules, and working-capital drivers. Monitor receivables and payment timing, and avoid assuming lower cash is caused by lower sales without further evidence.

### 4. Establish product-level action thresholds
Create a monthly review list for products that are below prior year and below budget. Assign an owner, likely driver, corrective action, and review date to each item.

### 5. Improve trend monitoring
Add a clear monthly variance view (actual vs. prior year and budget), with conditional formatting for material deviations. Keep YTD and monthly metrics clearly labelled to avoid misinterpretation.

### 6. Make refresh and governance repeatable
Document the data source, refresh owner, reporting period, metric definitions, and reconciliation checks. Store a dated snapshot when results are used for formal business decisions.

## Dashboard Components

- KPI cards for Revenue, Profit, and Cash.
- Product table with actual values and percentage variances.
- Actual revenue vs. budget comparison.
- Profit trend chart with prior-year and budget references.
- Interactive year, month, division, KPI, and top/bottom controls.

## Tools & Skills Demonstrated

- Microsoft Excel dashboard design
- KPI reporting and variance analysis
- Revenue, profit, and cash performance monitoring
- Prior-year and budget comparisons
- Trend interpretation and business recommendations
- Data validation and reporting-quality checks

## Repository Structure

```text
Productivity-Apps-KPI-Dashboard/
├── README.md
├── dashboard/
│   └── KPI-Dashboard.xlsx
├── images/
│   └── productivity-apps-kpi-dashboard.png
└── documentation/
    └── data-quality-and-methodology.md
```

[Project File](https://github.com/ekhatornvictory-lgtm/Productivity-Apps-KPI-Dashboard/blob/0b76da4266d1caf3a629826e0651ab35c65c2eaf/KPI-Dashboard.xlsx)

## Limitations

- The current displayed view is a historical example for June 2017, not a live business performance feed.
- Source-system and business definitions are not fully documented in the workbook provided.
- A database add-in connection is referenced in the source sheet; the repository does not include database credentials or the source database.
- Findings describe the workbook values and should not be treated as causal conclusions.

## Suggested Future Improvements

- Add a data dictionary defining revenue, profit, cash, budget, and prior-year measures.
- Add explicit monthly and year-to-date measures side by side.
- Add automated reconciliation checks for product totals vs. division totals.
- Add exception flags for large negative budget or prior-year variances.
- Publish a static PDF/screenshot alongside the interactive Excel workbook for easy portfolio review.

## Author

**Ekhator Victory**  
Data Analyst | Excel Dashboarding | Power BI | SQL

Connect: [GitHub](https://github.com/ekhatornvictory-lgtm)

---

*Built as a portfolio case study to demonstrate KPI reporting, data quality awareness, trend analysis, and business-focused recommendations in Excel.*
