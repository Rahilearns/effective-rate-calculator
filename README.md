# Effective Rate Calculator

A mobile-accessible, single-file HTML calculator for the **effective interest rate (EIR)** of a loan facility — supporting new loans, existing loans with rate revisions, multiple payment modalities, cash security/FDR offset, and customised repayment schedules.

🔗 **Live:** https://rahilearns.github.io/effective-rate-calculator/

## What it does

- **New Loan** — given loan amount, offered rate, modality, and tenure, computes the effective rate. Supports an optional cash-security (FDR / Cash Security / EMI-equivalent / EQI-equivalent) section that nets the security's interest income against the loan's cost.
- **Existing Loan** — given the original loan amount, modality, tenure, and a layered history of rates (and optionally a layered FDR), computes the blended effective rate post-rate-revision.
- **Payment modalities** — EMI, EQI, Equal Monthly/Quarterly Principal + Interest, Monthly/Quarterly Interest with bullet principal, and a fully customised schedule.

## Conventions

- Effective rate is computed via **IRR × periods-per-year** (nominal annualisation, matching `=IRR(range)*N` in Excel — the banking-disclosure standard).
- The FDR principal is modelled as a real cashflow: placed at t=0, repaid in full at loan maturity, with monthly interest accrual and 3-month renewal (principal-only payout vs. compounded).

## Stack

A single `index.html` — vanilla HTML / CSS / JS, no build step, no dependencies. Includes a strict CSP and a light/dark theme toggle that respects `prefers-color-scheme`.

## Deployment

Hosted on GitHub Pages from the `main` branch. Pushes deploy automatically within ~1 minute of commit.
