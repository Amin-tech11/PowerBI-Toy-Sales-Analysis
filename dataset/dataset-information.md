# Dataset Information

## Overview

This project uses three CSV datasets representing a toy retail business.

The datasets contain transactional sales data together with product and store information used to build the Business Intelligence solution.

---

# Dataset Files

| File | Description |
|------|-------------|
| sales.csv | Sales transactions |
| products.csv | Product information |
| stores.csv | Store information |

---

# Dataset Structure

The data follows a relational model where transactional records are connected to descriptive business entities.

The datasets are imported into Power BI and combined through relationships to create a semantic model.

---

# Data Source

The project uses CSV files as the primary data source.

CSV files were selected because they are:

- Lightweight
- Easy to maintain
- Widely supported
- Suitable for demonstration purposes
- Compatible with Power BI

---

# Data Preparation

Before building the dashboard, the datasets were prepared using Power Query.

The preparation process included:

- Importing CSV files
- Data type conversion
- Data cleaning
- Removing unnecessary columns
- Renaming columns
- Handling missing values
- Preparing relationships

---

# Data Model Integration

Each dataset plays a specific role in the semantic model.

## Sales

Acts as the central transactional table used for business calculations.

---

## Products

Provides descriptive information for product analysis.

---

## Stores

Provides descriptive information for store analysis.

---

# Business Usage

The datasets support multiple business scenarios, including:

- Sales analysis
- Product analysis
- Store comparison
- Revenue reporting
- Profitability analysis
- KPI monitoring
- Trend analysis

---

# Data Quality

Basic data quality checks were performed before loading the data into the model.

These checks included:

- Data type validation
- Duplicate inspection
- Missing value handling
- Consistent column naming
- Relationship verification

---

# Limitations

This dataset is intended for educational and portfolio purposes.

It demonstrates Business Intelligence concepts and dashboard development techniques rather than representing a real commercial database.

---

# Summary

The datasets provide a clean and structured foundation for building a complete Business Intelligence solution in Microsoft Power BI.

Combined with Power Query, DAX, and a Star Schema model, they enable interactive reporting and business performance analysis.