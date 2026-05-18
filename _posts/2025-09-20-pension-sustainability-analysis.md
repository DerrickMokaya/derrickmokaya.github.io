---
title: "Pension Sustainability Analysis: Applying Actuarial Methods to Demographic Risk"
date: 2025-09-20 09:00:00 +0300
categories: [Projects, Actuarial Science]
tags: [actuarial-science, pension, demographic-risk, excel, statistical-modelling, nssf]
pin: false
math: true
---

## Overview

One of the most pressing challenges facing pension funds in Sub-Saharan Africa is long-term sustainability. With aging populations, increasing life expectancy, and shifting employment patterns, defined-benefit pension schemes face mounting pressure to remain solvent across 30–50 year time horizons.

During my actuarial studies and internship at **NSSF Kenya**, I conducted a pension sustainability study that applied classical actuarial methods to assess whether a defined-benefit fund could meet its long-term obligations under various demographic and economic scenarios.

---

## The Problem: Why Pension Funds Fail

A pension fund becomes unsustainable when the **present value of future liabilities** exceeds the **present value of future contributions plus current assets**. This gap can emerge from:

- **Longevity risk** — members living longer than assumed
- **Contribution rate risk** — declining active membership or wage stagnation
- **Investment return risk** — actual returns below the discount rate assumption
- **Demographic imbalance** — rising retiree-to-active-member ratio

> A fund with a retiree-to-active ratio above 1:3 is typically considered under stress. Kenya's formal sector employment trends make this a real concern.

---

## Methodology

### 1. Data Inputs

The analysis required the following data:

| Input | Source | Description |
|---|---|---|
| Member age distribution | NSSF records | Active members by age band |
| Mortality tables | Kenya National Bureau of Statistics | Age-specific death rates |
| Salary growth assumption | CBK economic data | Projected wage inflation |
| Discount rate | Government bond yield | Long-term risk-free rate proxy |
| Contribution rate | NSSF Act | % of gross salary |

### 2. Actuarial Assumptions

The core assumptions used in the model:

- **Discount rate:** 11.5% p.a. (Kenya 10-year bond yield)
- **Salary growth:** 7.0% p.a.
- **Inflation:** 5.5% p.a.
- **Mortality:** EAT (East African Tables) with improvement factors
- **Withdrawal rate:** 8% p.a. for members aged 18–35

### 3. Projected Benefit Obligation (PBO)

The Projected Benefit Obligation was calculated as:

$$PBO = \sum_{x} \, l_x \cdot B_x \cdot v^{n-x}$$

Where:
- $l_x$ = number of members alive at age $x$
- $B_x$ = projected benefit at retirement based on final salary
- $v$ = discount factor $= \frac{1}{1+i}$
- $n$ = retirement age (60)

### 4. Funding Ratio

$$\text{Funding Ratio} = \frac{\text{Market Value of Assets}}{\text{Actuarial Value of Liabilities}}$$

A funding ratio below **100%** indicates an underfunded scheme. A ratio below **80%** is considered a critical threshold requiring corrective action.

---

## Scenario Analysis

I modelled three scenarios across a 30-year projection horizon:

| Scenario | Discount Rate | Salary Growth | Mortality Improvement | Outcome |
|---|---|---|---|---|
| **Base Case** | 11.5% | 7.0% | None | Funding ratio: 94% by 2055 |
| **Pessimistic** | 9.0% | 8.5% | +2 years life expectancy | Funding ratio: 71% by 2055 ⚠️ |
| **Optimistic** | 13.0% | 6.0% | None | Funding ratio: 112% by 2055 ✅ |

### Key Finding

The **discount rate assumption is the most sensitive variable**. A 2.5 percentage point reduction in the discount rate (from 11.5% to 9.0%) reduces the funding ratio by over 20 percentage points over 30 years — more than any other single assumption change.

This has a direct policy implication: as Kenya's interest rate environment evolves, NSSF's liability calculations must be reviewed regularly to avoid funding surprises.

---

## Demographic Risk: The Dependency Ratio

Beyond the financial model, I analysed the **demographic dependency ratio** — the ratio of retirees drawing benefits to active members contributing.

```
Year 2025: 1 retiree per 6.2 active members  ← comfortable
Year 2035: 1 retiree per 4.1 active members  ← manageable
Year 2045: 1 retiree per 2.8 active members  ← under pressure
Year 2055: 1 retiree per 2.1 active members  ← critical threshold
```

This trajectory is driven by:
1. Kenya's improving life expectancy (currently 67.3 years, projected 72+ by 2050)
2. Growth in formal sector employment not keeping pace with the maturing membership base
3. Early retirement and withdrawal patterns among younger members

---

## Recommendations

Based on the analysis, three interventions would materially improve long-term sustainability:

**1. Increase the contribution rate progressively**
A phased increase from 12% to 15% of gross salary over 10 years would add approximately KES 4.2 billion to annual inflows under base case assumptions.

**2. Introduce tiered benefit structures**
Linking benefit accrual rates to fund performance in high-stress years reduces the liability sensitivity to investment return shocks.

**3. Expand formal sector coverage**
Kenya's informal sector represents 83% of employment. Each 1% increase in formal sector coverage adds approximately 180,000 new contributing members — significantly improving the dependency ratio.

---

## Tools Used

- **Microsoft Excel** — actuarial projection model, scenario analysis, sensitivity tables
- **Statistical methods** — life table construction, present value calculations, regression on demographic trends
- **Kenya EAT mortality tables** — standard actuarial tables for East African populations

---

## Reflections

This project reinforced something fundamental about actuarial work: **the numbers are only as good as the assumptions behind them**. A pension fund that looks healthy under optimistic assumptions can be dangerously underfunded under realistic ones.

The discipline of stress-testing assumptions — and being transparent about uncertainty — is what separates actuarial analysis from simple financial forecasting.

---

*Next post: Introduction to SOC analytics — applying data skills to cybersecurity threat detection.*
