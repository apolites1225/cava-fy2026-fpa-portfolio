# Modeling CAVA's Unit Economics: An FP&A Deep Dive

![KPI Dashboard](images/kpi_dashboard.png)

<video src="https://raw.githubusercontent.com/apolites1225/cava-fy2026-fpa-portfolio/main/media/cava_walkthrough_compressed.mp4" controls width="700">
  Video walkthrough of the model — if it doesn't render, watch it directly: media/cava_walkthrough_compressed.mp4
</video>

## Why I built this

I wanted to go beyond a resume line and actually do the work of a Financial Analyst at a public, multi-unit restaurant company — not summarize CAVA's numbers, but build the model an analyst on their team would actually maintain: a full restaurant-level P&L, a FY2026 forecast built two independent ways, and a reconciliation between them.

Everything in this project is sourced directly from CAVA's public SEC filings — 10-Qs for Q1–Q3, and the 8-K Exhibit 99.1 for Q4/full-year results. No modeled figure went into the workbook without being traced back to a primary source first.

## What's in the model

The final workbook is eleven tabs, moving from raw inputs to finished analysis:

- **FY25 Actuals** — quarterly restaurant-level P&L, rebuilt entirely on a consistent basis (more on why below)
- **FY26 RL Assumptions** — the drivers behind the forecast: same-restaurant sales growth, new unit openings, ramp timing
- **FY26 RL Forecast** — a bottom-up build, quarter by quarter
- **Scenario Summary** — a top-down build, working backward from management's own guidance
- **Margin Reconciliation** — where the two approaches get checked against each other
- **KPI Dashboard, Quarterly Trend, Guidance vs. Actual, Model Guide, Data Gaps, Source Register** — supporting structure and documentation

## The mistake that shaped the whole project

Early on, my restaurant-level profit reconciliation wasn't tying out — the numbers were close, but not exact. I traced it back line by line and found the actual problem: I'd pulled Restaurant-Level Profit from CAVA's segment-basis disclosures, and COGS from a consolidated-basis statement in a different filing. Both figures were individually correct. They just weren't measuring the same thing.

That distinction turned out to matter more than I expected. CAVA's own MD&A states that segment-basis results are what's most useful for assessing restaurant performance — consolidated figures blend in G&A and pre-opening costs that have nothing to do with whether an individual restaurant's unit economics actually work. I rebuilt the FY2025 actuals entirely on segment basis, quarter by quarter, and the reconciliation held exactly.

It's a small thing on the surface, but it's the kind of error that's invisible until you build a check that forces it to surface — which became the design principle for the rest of the project.

## Two ways to forecast the same year

Rather than build one FY2026 margin forecast, I built two, deliberately, using the same revenue base but different cost logic:

**Bottom-up:** Each quarter's COGS, Labor, and Occupancy percentages are built from that same quarter's actual FY2025 performance, with a +0.4 point COGS overlay applied to reflect the upward trend CAVA's actuals showed through the year (29.3% in Q1 FY25 climbing to 30.4% by Q4). This produced a 23.98% full-year Restaurant-Level Margin.

**Top-down:** Apply CAVA's own guided margin range directly to modeled revenue and solve backward for implied costs. Guidance midpoint: 23.95%.

The two approaches came in 0.03 points apart — close enough that the bottom-up build effectively corroborates what management is telling the market, using a completely independent methodology. Neither number is "more correct" than the other; they're two different lenses answering the same question, and having them agree is the actual point.

## Building verification into the process, not around it

Since I used AI tools throughout this project — for research, structuring, and parts of the build — I treated verification as a required step, not an optional check. A few things that discipline caught:

- A research tool that generated a table of citations pointing to the wrong source documents entirely
- A $4M reconciliation error, traced to a modeling step that had silently re-derived a number instead of using my verified dataset
- Two hardcoded totals that looked correct but wouldn't update if an input changed — converted to live formulas
- The segment-vs-consolidated basis conflict described above

None of these were dramatic failures — they were the ordinary kind of error that creeps into any complex model, AI-assisted or not. The difference was having a reconciliation structure built in from the start that made errors surface instead of hide.

## What I'd do differently

The model is intentionally built on simple, auditable formulas — SUM, IF, and SUMPRODUCT rather than more complex lookup functions — because a model other people have to trust and maintain is worth more than one that's needlessly clever. If I extended this project, the next step would be integrating a proper data model (Power Query/Power Pivot/DAX) the way I've done in other practice projects, to make the structure scale past a single company's filings.

## The takeaway

Building this wasn't really about proving I could model CAVA's numbers. It was about proving I default to checking my own work — tracing figures to source, reconciling independent methods against each other, and treating a clean-looking output as a hypothesis to test rather than a fact to trust. That's the habit I think matters most in FP&A, and it's the one this project was actually designed to demonstrate.

## File

`CAVA_FY2026_FPA_Portfolio_Package_v2.0.xlsx`

## Modeling conventions

- Units: $ in thousands, except percentages, weeks, and restaurant counts.
- **Blue font** — hardcoded historical inputs and editable assumptions.
- **Green font** — formulas linked from another worksheet.
- **Black font** — formulas calculated within the same worksheet.
- **Yellow fill** — open assumption requiring human input or approval.
- Status labels: Actual / Guidance-derived / Modeled assumption / Open assumption.

## Sources

All figures sourced from CAVA Group, Inc. public SEC filings (10-Q, 8-K); full list with URLs in the Source Register tab.

---

*This project was built independently as a demonstration of financial modeling and analysis methodology, and is not affiliated with or endorsed by CAVA Group, Inc.*
