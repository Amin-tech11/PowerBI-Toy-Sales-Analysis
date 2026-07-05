# DAX Measures Documentation

## Overview

The dashboard uses **Data Analysis Expressions (DAX)** to implement business logic, calculate KPIs, and support interactive analysis.

Measures are preferred over calculated columns whenever possible to improve model efficiency and maintainability.

---

# Objectives

The DAX layer was designed to:

- Calculate business KPIs
- Aggregate sales information
- Measure financial performance
- Rank products and stores
- Support time-based analysis
- Enable interactive reporting

---

# Measure Categories

The report includes several categories of DAX measures.

## Sales Measures

These measures summarize sales activity across the business.

Examples include:

- Total Sales
- Total Orders
- Total Quantity Sold
- Average Sales

---

## Financial Measures

Financial measures evaluate business profitability.

Examples include:

- Total Profit
- Profit Margin
- Average Order Value

---

## Product Measures

Product measures support product-level analysis.

Examples include:

- Product Revenue
- Product Profit
- Product Ranking
- Category Performance

---

## Store Measures

Store measures evaluate operational performance.

Examples include:

- Store Revenue
- Store Profit
- Store Ranking

---

## Time Intelligence Measures

Time Intelligence enables trend analysis across different periods.

Typical calculations include:

- Month-to-Date (MTD)
- Quarter-to-Date (QTD)
- Year-to-Date (YTD)
- Running Total
- Period Comparison

---

# DAX Design Principles

The measures were developed following Microsoft Power BI best practices.

Applied principles include:

- Reusable measures
- Descriptive naming conventions
- Measure reuse instead of duplication
- Readable expressions
- Optimized performance
- Business-oriented calculations

---

# Organization

Business calculations are stored inside a dedicated **Measures** table.

This improves:

- Model readability
- Maintenance
- Scalability
- Navigation

---

# Performance Considerations

The DAX implementation focuses on efficient report performance.

Optimization techniques include:

- Reusing existing measures
- Minimizing unnecessary calculations
- Keeping filter context simple
- Avoiding redundant logic
- Separating calculations from source tables

---

# Business Value

The DAX layer transforms raw transactional data into meaningful business information.

It enables users to:

- Monitor KPIs
- Compare business performance
- Analyze profitability
- Track sales trends
- Evaluate products
- Compare stores

---

# Summary

The DAX implementation provides the analytical foundation of the dashboard.

By combining reusable business measures with optimized calculation logic, the report delivers accurate, interactive, and scalable business insights.