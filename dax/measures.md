# DAX Measures Reference

## Overview

This document provides a technical reference for the DAX measures used in the **PowerBI Toy Sales Analysis** project.

The measures are organized into logical categories and follow Microsoft Power BI best practices for readability, reusability, and performance.

---

# Sales Measures

## Total Revenue

```DAX
Total Revenue =
SUM('FCT Sales'[Total Revenue])
```

**Purpose**

Calculates the total revenue generated from all sales transactions.

---

## Quantity Sold

```DAX
Quantity Sold =
SUM('FCT Sales'[Quantity])
```

**Purpose**

Calculates the total quantity of products sold.

---

## Avg Revenue per Unit

```DAX
Avg Revenue per Unit =
DIVIDE(
    [Total Revenue],
    [Quantity Sold],
    0
)
```

**Purpose**

Calculates the average revenue generated for each unit sold.

---

## AVG Revenue per Store

```DAX
AVG Revenue per Store =
AVERAGEX(
    VALUES('DIM Stores'[Store_Name]),
    [Total Revenue]
)
```

**Purpose**

Calculates the average revenue generated across all stores.

---

# Financial Measures

## Total Cost

```DAX
Total Cost =
SUM('FCT Sales'[Total Cost])
```

**Purpose**

Calculates the total cost of all sales transactions.

---

## Total Profit

```DAX
Total Profit =
SUM('FCT Sales'[Profit])
```

**Purpose**

Calculates the overall profit generated from sales.

---

## Profit Margin

```DAX
Profit Margin =
DIVIDE(
    [Total Profit],
    [Total Revenue],
    0
)
```

**Purpose**

Calculates the profit margin as a percentage of total revenue.

---

## AVG Profit per Sale

```DAX
AVG profit per sale =
DIVIDE(
    [Total Profit],
    [Quantity Sold],
    0
)
```

**Purpose**

Calculates the average profit generated per sold unit.

---

## Avg Cost per Unit

```DAX
Avg Cost per Unit =
DIVIDE(
    [Total Cost],
    [Quantity Sold],
    0
)
```

**Purpose**

Calculates the average cost per unit sold.

---

# Time Intelligence Measures

## YTD Revenue

```DAX
YTD Revenue =
TOTALYTD(
    [Total Revenue],
    'DIM Dates'[Date]
)
```

**Purpose**

Calculates cumulative revenue from the beginning of the year to the selected date.

---

## Previous YTD Revenue

```DAX
Previous YTD Revenue =
CALCULATE(
    [YTD Revenue],
    SAMEPERIODLASTYEAR('DIM Dates'[Date])
)
```

**Purpose**

Returns the Year-to-Date revenue for the same period in the previous year.

---

## YOY Revenue

```DAX
YOY Revenue =
DIVIDE(
    [YTD Revenue] - [Previous YTD Revenue],
    [Previous YTD Revenue]
)
```

**Purpose**

Calculates the Year-over-Year (YoY) growth rate based on YTD revenue.

---

# Design Principles

The measures were developed according to the following principles:

- Reusable business logic
- Consistent naming conventions
- Use of measures instead of calculated columns whenever appropriate
- Safe division using `DIVIDE()`
- Modular calculations
- Time intelligence using dedicated Date table
- Performance-oriented implementation

---

# Summary

These DAX measures provide the analytical foundation of the dashboard by transforming transactional sales data into business KPIs, financial metrics, and time-based performance indicators.

Together, they enable interactive reporting, executive monitoring, and data-driven decision-making within the Power BI solution.