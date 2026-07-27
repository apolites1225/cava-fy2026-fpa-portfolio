# CAVA FY2026 FP&A Portfolio Package

A quarterly, restaurant-level forecast model for CAVA Group, built as a final project for a Data Analytics & Analysis (DAA) course. The model reconstructs FY2025 performance from public filings, checks it against CAVA's original guidance, and builds a Low / Base / High FY2026 forecast from that base.

**Scope note:** This analysis is intentionally scoped to information available as of CAVA's FY2025 year-end close (February 24, 2026). Subsequent disclosures — including Q1 FY2026 results and updated guidance issued May 19, 2026 — are out of scope by design, consistent with treating this as a point-in-time year-end review.

## File

`CAVA_FY2026_FPA_Portfolio_Package_v2.0.xlsx`

## Workbook structure

- **KPI Dashboard** — headline revenue, restaurant-level margin, and Adjusted EBITDA by quarter (FY2025) plus FY2026 scenario output.
- **Guidance vs Actual** — CAVA's original FY2025 guidance (low/mid/high) vs. actual results, with variances and sourcing for each line.
- **Quarterly Trend** — quarter-over-quarter trend view across FY2025.
- **FY25 Actuals** — reconstructed FY2025 income statement inputs from public filings.
- **FY26 RL Assumptions** — editable restaurant-level assumptions driving the FY2026 forecast.
- **FY26 RL Forecast** — FY2026 restaurant-level P&L build.
- **Margin Reconciliation** — bridges restaurant-level margin to Adjusted EBITDA.
- **Scenario Summary** — Low / Base / High FY2026 scenarios for same-restaurant sales growth, new unit openings, revenue, COGS, and labor.
- **Model Guide** — legend, units, and documentation of modeling conventions (see below).
- **Data Gaps** — items not disclosed in public filings, flagged rather than estimated.
- **Source Register** — primary sources (CAVA investor releases) with reporting dates and URLs.

## Modeling conventions

- Units: $ in thousands, except percentages, weeks, and restaurant counts.
- **Blue font** — hardcoded historical inputs and editable assumptions.
- **Green font** — formulas linked from another worksheet.
- **Black font** — formulas calculated within the same worksheet.
- **Yellow fill** — open assumption requiring human input or approval.
- Status labels: Actual / Guidance-derived / Modeled assumption / Open assumption.

**Limitation:** CAVA does not disclose FY2026 revenue, labor, COGS, G&A, or D&A guidance directly. Where the company hasn't disclosed a figure, the model builds a labeled, sourced estimate rather than presenting it as fact — see the Data Gaps tab for what's explicitly left open.

## Sources

All figures are drawn from CAVA's public investor releases (Q1–Q4 FY2025 and Q4/FY2025 results); full list with URLs in the Source Register tab.
