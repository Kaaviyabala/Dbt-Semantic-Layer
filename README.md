# dbt Semantic Layer
**MetricFlow · dbt Cloud · Snowflake**

A working prototype of the architecture I'm piloting at work — define metrics once, govern them centrally, serve them consistently across every BI tool.

---

## The Problem I'm Solving

At large financial institutions:
- Finance has one number. Treasury has another. Same metric, different logic.
- Business logic is scattered across SQL scripts, BI reports, and people's heads.
- Getting a simple metric means filing a ticket and waiting — for data needed every month.
- Stakeholders can't ask questions in plain English. A technical person is always in the loop.

This repo explores how the dbt Semantic Layer fixes all four.

---

## What's Built

Two semantic models (`fct_orders`, `dim_customers`) with all five MetricFlow metric types:

| Type | Examples |
|------|---------|
| Simple | `revenue`, `avg_revenue`, `distinct_customers`, `high_value_customer_count` |
| Ratio | `large_orders_percentage`, `avg_orders_value` |
| Cumulative | `cumulative_revenue_l30d`, `cumulative_revenue_mtd`, `cumulative_revenue_alltime` |
| Derived | `large_orders_percentage_derived` |
| Filtered | `orders_over_20`, `high_value_customer_count` |

Plus a saved query with a governed export to the `analytics` schema.

---

## What's Next

Layering **LLM-interpretable metadata** so stakeholders can query metrics in plain English — no SQL, no ticket, no wait.

---

## Stack
`dbt Cloud` · `MetricFlow` · `Snowflake` · `Tableau` · `Google Sheets` · `Power BI`

---

**Kaaviya Balasubramanian** — Analytics Engineer
[LinkedIn](https://www.linkedin.com/in/) · [GitHub](https://github.com/)
