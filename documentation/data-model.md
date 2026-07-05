# Data Model

## Overview

The Business Intelligence solution is built on a **Star Schema** data model, which is the recommended modeling approach for Microsoft Power BI.

The model separates transactional data from descriptive information, resulting in improved performance, easier maintenance, and simplified DAX calculations.

---

# Model Architecture

The data model consists of one central fact table connected to multiple dimension tables.

```
                Products
                    │
                    │
                    ▼
              ┌───────────┐
              │   Sales   │
              └───────────┘
                    ▲
                    │
                    │
                 Stores

             Calendar
                 │
                 ▼

             Measures
```

The fact table stores transactional data, while the dimension tables provide descriptive attributes used for filtering and analysis.

---

# Fact Table

## Sales

The Sales table is the central fact table in the model.

It stores transactional sales records and serves as the foundation for all business calculations.

Typical information includes:

- Sales Amount
- Quantity Sold
- Product Reference
- Store Reference
- Transaction Date

---

# Dimension Tables

## Products

Contains descriptive information about products.

Typical attributes include:

- Product Name
- Product Category
- Product Cost
- Product Price

---

## Stores

Contains descriptive information about store locations.

Typical attributes include:

- Store Name
- Store Location
- Store Information

---

## Calendar

A dedicated Date table is used for time-based analysis.

It enables:

- Year Analysis
- Monthly Analysis
- Quarterly Analysis
- Time Intelligence
- Date Filtering

---

## Measures

Business calculations are stored in a dedicated Measures table.

Separating measures from data tables improves model organization and simplifies maintenance.

---

# Relationships

The model uses **One-to-Many** relationships between dimensions and the fact table.

```
Products ───────► Sales ◄────── Stores
                      ▲
                      │
                  Calendar
```

Relationship design follows Microsoft Power BI best practices.

---

# Design Principles

The model was designed using the following principles:

- Star Schema Architecture
- Single Source of Truth
- Minimal Data Redundancy
- High Query Performance
- Simple Relationship Structure
- Reusable Business Logic
- Scalable Model Design

---

# Benefits of the Star Schema

Using a Star Schema provides several advantages.

- Faster report performance
- Simplified DAX calculations
- Easier maintenance
- Better scalability
- Cleaner model design
- Improved readability
- Optimized filtering behavior

---

# Model Optimization

Several optimization techniques were applied during development.

These include:

- Appropriate data types
- Optimized relationships
- Reduced model complexity
- Efficient filtering
- Dedicated Measures table
- Clean table naming
- Business-oriented model organization

---

# Best Practices Applied

The data model follows Microsoft Power BI development recommendations.

Implemented best practices include:

- Fact and Dimension separation
- Dedicated Calendar table
- Dedicated Measures table
- Star Schema modeling
- Consistent naming conventions
- Minimal relationship complexity

---

# Summary

The semantic model provides a scalable and maintainable foundation for business reporting.

Its Star Schema architecture enables efficient filtering, optimized DAX calculations, and high-performance interactive dashboards while supporting future expansion of the solution.