# EDA Project – End-to-End Exploratory Data Analysis

## Executive Summary

This project demonstrates a production-style Exploratory Data Analysis workflow applied to a multi-entity Excel dataset.

The objective was to convert fragmented operational data into a clean, relational, business-constrained analytical dataset suitable for reporting, dashboarding, and modeling.

The workflow emphasizes data integrity, business alignment, and structural correctness over superficial visualization.

---

## Business Objective

The analysis was designed to support:

- Revenue performance evaluation  
- Profitability tracking  
- Regional performance comparison  
- Budget vs actual alignment  

The final dataset enables downstream decision-making in reporting tools such as Power BI or statistical modeling environments.

---

## Data Scope

Source: Multi-sheet Excel workbook containing independent entities:

- Sales transactions  
- Customer master data  
- Product catalog  
- Regional mapping  
- State-level information  
- Budget allocation data  

The sheets were structurally independent and required modeling before analysis.

---

## Methodology

### 1. Context Framing

- Defined analytical scope and constraints  
- Identified decision metrics  
- Aligned technical workflow with business intent  

This prevented tool-driven exploration and ensured measurable outcomes.

---

### 2. Data Ingestion and Structural Validation

- Imported all sheets into pandas DataFrames  
- Inspected schemas and structural inconsistencies  
- Corrected header issues and formatting errors  
- Standardized data types  

Objective: Establish structural reliability before transformation.

---

### 3. Data Profiling and Quality Assessment

- Performed null value analysis  
- Evaluated duplicate records  
- Conducted early anomaly detection  
- Validated row-level integrity  

This phase reduced risk of downstream metric distortion.

---

### 4. Data Modeling and Integration

- Identified primary and foreign keys  
- Defined relational structure  
- Executed staged merges across entities  
- Verified referential integrity post-merge  
- Validated row counts and join accuracy  

Outcome: Unified relational analytical dataset.

---

### 5. Cleanup and Feature Optimization

- Removed redundant attributes  
- Standardized naming conventions  
- Reduced dimensional noise  
- Retained domain-relevant variables only  

This improved analytical clarity and performance efficiency.

---

### 6. Business Rule Enforcement

- Integrated budget data  
- Applied year constraints  
- Filtered dataset to 2017 records  
- Revalidated metric completeness  

The final dataset strictly reflects business-defined scope.

---

## Final Output

A validated, analysis-ready dataset prepared for:

- Power BI dashboard development  
- KPI performance tracking  
- Statistical modeling  
- Forecasting workflows  

---

## Technical Stack

- Python  
- Pandas  
- NumPy  
- Excel  
- Matplotlib  

---

## Competencies Demonstrated

- Business-driven analytics  
- Data profiling and validation  
- Relational data modeling  
- Join strategy and integrity verification  
- Data quality governance  
- Feature engineering discipline  
- Business constraint implementation  
