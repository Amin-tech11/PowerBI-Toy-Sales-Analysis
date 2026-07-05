# Power Query Transformations

## Overview

Power Query was used to perform the Extract, Transform, and Load (ETL) process before loading the data into the Power BI data model.

The objective was to prepare clean, consistent, and analysis-ready datasets while keeping the semantic model efficient and maintainable.

---

# ETL Workflow

The data preparation process followed these stages:

```
CSV Files
      │
      ▼
Import into Power Query
      │
      ▼
Data Cleaning
      │
      ▼
Data Transformation
      │
      ▼
Data Validation
      │
      ▼
Load into Data Model
```

---

# Import Process

The project imports multiple CSV files into Power Query.

Imported datasets include:

- Sales
- Products
- Stores

Each dataset is loaded independently before being transformed.

---

# Data Cleaning

The following data cleaning operations were performed:

- Correcting data types
- Removing unnecessary columns
- Renaming columns
- Standardizing column names
- Checking missing values
- Validating imported data

---

# Data Transformation

Power Query was used to prepare the datasets for analytical reporting.

Transformation tasks include:

- Data type conversion
- Column formatting
- Data normalization
- Table preparation
- Relationship readiness

---

# Data Validation

Before loading the data model, validation checks were performed to improve data quality.

Validation activities include:

- Reviewing imported records
- Verifying column formats
- Inspecting null values
- Checking table consistency

---

# Loading Strategy

Only transformed datasets were loaded into the semantic model.

This approach helps improve:

- Report performance
- Model maintainability
- Data consistency

---

# Benefits of Using Power Query

Using Power Query provides several advantages:

- Reusable transformation steps
- Automated data preparation
- Improved data quality
- Easier maintenance
- Reduced manual work
- Better reporting consistency

---

# Best Practices Applied

The ETL process follows Microsoft Power BI recommendations.

Applied practices include:

- Keeping transformations inside Power Query
- Preparing clean datasets before modeling
- Using descriptive query names
- Maintaining consistent column naming
- Minimizing unnecessary processing

---

# Summary

Power Query serves as the foundation of the data preparation process.

By transforming raw CSV files into clean, structured datasets, it enables the creation of an efficient semantic model and supports reliable Business Intelligence reporting.