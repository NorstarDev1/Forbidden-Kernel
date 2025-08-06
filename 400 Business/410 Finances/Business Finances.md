---
tags: dashboard/finances/business
---
# Business Finances Overview

This dashboard provides an overview of business income, expenses, and invoice tracking.

**Expected Note Format (from Alfonso or manual entry):**
```yaml
date: YYYY-MM-DD
amount: 123.45
type: income # or expense
category: Sales # e.g., Marketing, Software, Salary
description: Brief description of transaction
invoice-id: INV-2025-001 # Optional, for invoices
status: paid # Optional, for invoices (paid, pending, due)
```

## All Business Transactions
```dataview
TABLE date, description, amount, type, category, invoice-id, status
FROM "400 Business/410 Finances"
SORT date DESC
```

## Business Income Summary
```dataview
TABLE date, description, amount, category
FROM "400 Business/410 Finances"
WHERE type = "income"
SORT date DESC
```

## Business Expense Summary
```dataview
TABLE date, description, amount, category
FROM "400 Business/410 Finances"
WHERE type = "expense"
SORT date DESC
```

## Business Invoices
```dataview
TABLE date, invoice-id, amount, status, description
FROM "400 Business/410 Finances"
WHERE invoice-id
SORT date DESC
```
