---
title: "How I Improved Financial Data Accuracy by 20% at NSSF Kenya"
date: 2025-10-15 10:00:00 +0300
categories: [Projects, Finance]
tags: [excel, sql, reconciliation, nssf, data-quality]
---

## Context

During my internship at the **National Social Security Fund (NSSF) Kenya**, I was embedded in the Finance & Data Analytics unit. One of the first things I noticed was that manual reconciliation processes were slow, error-prone, and heavily dependent on individual analyst knowledge.

## The Problem

> Pension contribution records were being reconciled manually across multiple Excel sheets with no standardised validation logic.

This led to:
- Inconsistent record formats across departments
- Duplicate or missing member entries
- High rework rate before monthly reporting deadlines

## My Approach

### Step 1 — Understand the Data Flow

I mapped the end-to-end contribution data pipeline:

```
Member Registration → Contribution Deduction → Payment Register → NSSF Database
```

Each handoff introduced potential discrepancies. The reconciliation needed to catch errors at each stage.

### Step 2 — Build a SQL Validation Query

I wrote SQL queries to cross-validate member IDs, contribution amounts, and payment dates:

```sql
SELECT
    m.member_id,
    m.full_name,
    c.contribution_amount,
    p.payment_date,
    CASE
        WHEN c.contribution_amount != p.expected_amount THEN 'MISMATCH'
        WHEN p.payment_date IS NULL THEN 'MISSING PAYMENT'
        ELSE 'OK'
    END AS validation_status
FROM members m
LEFT JOIN contributions c ON m.member_id = c.member_id
LEFT JOIN payments p ON c.contribution_id = p.contribution_id
ORDER BY validation_status;
```

### Step 3 — Automate the Excel Reconciliation Template

Using **Power Query** and structured tables, I built a reusable template that:
- Automatically flagged mismatches on import
- Colour-coded rows by validation status (green/amber/red)
- Produced a one-click summary for the finance manager

## Results

| Metric | Before | After | Change |
|---|---|---|---|
| Data accuracy rate | ~78% | ~94% | **+20%** ✅ |
| Reconciliation prep time | ~6 hours/month | ~4 hours/month | **-30%** ✅ |
| Records validated | Manual spot-check | 5,000+ systematic | **Full coverage** ✅ |

## Lessons Learned

1. **Understand the business process first** — technical tools are only as good as your understanding of the workflow they support.
2. **Automation is not just speed** — it removes human inconsistency, which is the bigger win.
3. **Document everything** — a handover-ready template outlived my internship.

---

*Next post: Pension Sustainability Analysis — applying actuarial methods to demographic projections.*
