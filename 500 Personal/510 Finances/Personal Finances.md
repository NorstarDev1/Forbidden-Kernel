---
tags: dashboard/finances/personal
---
# Personal Finances Overview

This dashboard provides an overview of personal income and expenses.

**Expected Note Format (from Alfonso or manual entry):**
```yaml
date: YYYY-MM-DD
amount: 123.45
type: income # or expense
category: Salary # e.g., Groceries, Rent, Entertainment
description: Brief description of transaction
```

## All Personal Transactions
```dataview
TABLE date, description, amount, type, category
FROM "500 Personal/510 Finances"
SORT date DESC
```

## Personal Income Summary
```dataview
TABLE date, description, amount, category
FROM "500 Personal/510 Finances"
WHERE type = "income"
SORT date DESC
```

## Personal Expense Summary
```dataview
TABLE date, description, amount, category
FROM "500 Personal/510 Finances"
WHERE type = "expense"
SORT date DESC
```
