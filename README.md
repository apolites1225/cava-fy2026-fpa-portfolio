# CAVA FY2026 FP&A Portfolio Package

A quarterly, restaurant-level forecast model for CAVA Group. The model reconstructs FY2025 performance from public filings, checks it against CAVA's original guidance, and builds a Low / Base / High FY2026 forecast from that base.

![KPI Dashboard](images/kpi_dashboard.png)

## Executive Summary

CAVA missed FY2025 same-restaurant sales growth guidance by up to 4 points — actual came in at 4.0% against a 6.0-8.0% guided range. Restaurant-level margin also landed just below guidance (24.4% actual vs. 24.8-25.2% guided), and pre-opening costs ran $4.1-5.1M over the guided range as the company leaned into unit growth.

That unit growth is what offset the shortfall: net new openings beat guidance (72 actual vs. 62-66 guided), and the added volume was enough to land Adjusted EBITDA within the original guidance range ($152.8M actual vs. $150.0-157.0M guided) despite the comp-sales miss. The FY2026 forecast in this workbook builds forward from that base, modeling Low / Base / High scenarios for same-restaurant sales growth, new unit openings, revenue, COGS, and labor.

**Scope note:** This analysis is intentionally scoped to information available as of CAVA's FY2025 year-end close (February 24, 2026). Subsequent disclosures — including Q1 FY2026 results and updated guidance issued May 19, 2026 — are out of scope by design, consistent with treating this as a point-in-time year-end review.

## Business Questions

- How did CAVA's FY2025 actual performance compare to original guidance across same-restaurant sales growth, restaurant-level margin, pre-opening costs, and Adjusted EBITDA?
- Did unit growth (new restaurant openings) offset the same-restaurant sales shortfall, and by how much?
- What does FY2026 look like under Low / Base / High scenarios for same-restaurant sales growth, new unit openings, revenue, COGS, and labor?
- Which FY2026 inputs are grounded in company guidance versus modeled assumptions, and where are the open disclosure gaps?

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

## Key Findings

**Same-Restaurant Sales & Margin**
Actual same-restaurant sales growth of 4.0% missed the 6.0-8.0% guided range by up to 4 points. Restaurant-level margin landed at 24.4% vs. 24.8-25.2% guided, and pre-opening costs ran $4.1-5.1M over the guided range.

**Unit Growth Offset**
Net new restaurant openings beat guidance (72 actual vs. 62-66 guided). That added volume was enough to land Adjusted EBITDA within the original guided range ($152.8M actual vs. $150.0-157.0M guided) despite the comp-sales miss.

**FY2026 Outlook**
Low / Base / High scenarios are modeled forward from the FY2025 base for same-restaurant sales growth, new unit openings, revenue, COGS, and labor.

## Planning Considerations for FY2026

- Unit growth is carrying more of the Adjusted EBITDA story than comp sales; if openings decelerate toward the guided 62-66 range, there is less cushion to absorb a comp miss of similar size.
- Pre-opening cost overruns are worth watching as a leading indicator of how the unit-growth strategy is being funded.
- Because CAVA does not guide FY2026 revenue, labor, COGS, G&A, or D&A directly, scenario ranges — not single-point estimates — should drive planning until further guidance is issued.

## Assumptions & Limitations

- This analysis is scoped to information available as of CAVA's FY2025 year-end close (February 24, 2026); Q1 FY2026 results and the May 19, 2026 guidance update are intentionally excluded.
- **Limitation:** CAVA does not disclose FY2026 revenue, labor, COGS, G&A, or D&A guidance directly. Where the company hasn't disclosed a figure, the model builds a labeled, sourced estimate rather than presenting it as fact — see the Data Gaps tab for what's explicitly left open.
- Historical inputs are reconstructed from public investor filings, not internal company data; any reporting revisions issued after this write-up are not reflected.

## Sources

All figures are drawn from CAVA's public investor releases (Q1–Q4 FY2025 and Q4/FY2025 results); full list with URLs in the Source Register tab.

## Project Structure

```
cava-fy2026-fpa-portfolio/
├── images/
│   └── kpi_dashboard.png
├── CAVA_FY2026_FPA_Portfolio_Package_v2.0.xlsx
└── README.md
```
