# Copay

**Which health plan actually costs less?**

A single-file health insurance cost estimator. Enter the plans you're choosing
between — premium, deductible, out-of-pocket max, visit copays, prescription
tiers — plus what you actually use (your prescriptions and how often you see a
doctor), and Copay shows the true monthly and annual cost of each plan side by
side. It answers the real question: is the plan with the $5-cheaper
prescription still cheaper after its $20-higher premium?

Live: https://itsavibecode.github.io/copay/ · Demo with sample data: add `?demo=1`

## Features (v0.1)

- Compare any number of plans: premium (monthly or per-paycheck), deductible,
  out-of-pocket max, employer HSA/HRA contribution, PCP/specialist/urgent-care
  copays, and four prescription tiers
- Prescriptions with per-plan tier assignment (the same drug is often a
  different tier under different insurers) or an exact custom cost per fill
- Winner banner explaining the annual savings and where they come from
- Sortable comparison table, plus a per-prescription cost table by plan
- Worst-case-year column: premiums + out-of-pocket max − employer HSA money
- All data stays in your browser (localStorage). Export/Import JSON for backup
- Demo mode (`?demo=1`) with two sample plans — changes aren't saved

## What v0.1 does *not* do yet

v0.1 compares the copay amounts you enter directly. It does **not** simulate
deductible timing (paying full price until the deductible is met, then copays,
capped at the out-of-pocket max). For high-deductible plans, enter your best
estimate of what a visit or fill really costs you. A month-by-month deductible
simulation with a cumulative-cost chart is planned for v0.2.

## Privacy

No accounts, no server, no analytics. Health and cost data never leaves your
browser unless you export it yourself.

## Changelog

### v0.1.0 — 2026-07-07

First release. Built to answer a simple question that plan-comparison sheets
make surprisingly hard: after premiums, prescriptions, and doctor visits, which
plan is actually cheaper per month? Simple mode only for now — copay-based
math with a worst-case column; deductible-aware simulation is next.
