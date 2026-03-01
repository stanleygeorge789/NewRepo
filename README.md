# EDA Project – End-to-End Exploratory Data Analysis

## Project Overview

This project demonstrates a structured, business-aligned Exploratory Data Analysis (EDA) workflow.

The objective is not just to “analyze data,” but to transform raw, multi-sheet Excel data into a clean, validated, analysis-ready dataset that supports downstream reporting and decision-making.

The project follows a disciplined approach:

- Context framing  
- Data ingestion  
- Profiling and validation  
- Data modeling  
- Cleanup and standardization  
- Business rule enforcement  
- Final dataset handoff  

---

## 1. EDA Context and Framing (00:00 – 05:40)

### 1.1 EDA Introduction and Project Context
- Defined the scope of analysis  
- Identified key stakeholders and decision drivers  
- Clarified expected business outcomes  
- Positioned the project for portfolio and production relevance  

### 1.2 Problem Statement and Business Objective
- Framed the analytical objective in measurable terms  
- Identified revenue, profitability, and regional performance as core focus areas  
- Established clarity on how insights will drive business decisions  

This ensures the analysis is business-driven, not tool-driven.

---

## 2. Environment Setup and Data Loading (05:40 – 11:20)

### 2.1 Environment Setup
- Python environment configured  
- Core libraries initialized (pandas, numpy, matplotlib, etc.)  
- Structured project workflow  

### 2.2 Loading Multi-Sheet Excel Dataset
- Imported Excel workbook  
- Inspected available sheets  
- Validated structural consistency across sheets  
- Verified schema alignment  

Goal: Convert fragmented Excel structure into structured DataFrames.

---

## 3. Initial Data Profiling (11:20 – 21:30)

### 3.1 Assigning Sheets to DataFrames
- Separated sheets into logical entities  
  - Sales  
  - Customers  
  - Products  
  - Regions  
  - States  

### 3.2 Structural Validation
- Corrected header inconsistencies  
- Standardized column alignment  
- Checked data types  
- Performed early sanity checks  

### 3.3 Data Quality Assessment
- Null value analysis  
- Missing data patterns  
- Duplicate detection  
- Early anomaly identification  

This phase ensures analytical reliability before modeling.

---

## 4. Data Modeling and Integration (21:30 – 30:10)

### 4.1 Data Merging Strategy
- Identified primary and foreign keys  
- Defined entity relationships  
- Established merge hierarchy  

### 4.2 Entity Integration
Merged:
- Sales  
- Customers  
- Products  
- Regions  
- States  

Validated:
- Join integrity  
- Row counts before and after merge  
- Referential consistency  

Outcome: Unified analytical dataset.

---

## 5. Data Cleanup and Standardization (30:10 – 40:30)

### 5.1 Redundant Column Removal
- Identified duplicate attributes  
- Removed non-contributing fields  
- Reduced dataset dimensionality  

### 5.2 Naming Conventions
- Standardized column names  
- Applied consistent casing  
- Removed ambiguity  

### 5.3 Domain-Driven Feature Selection
- Retained only business-relevant fields  
- Eliminated noise variables  
- Ensured alignment with analysis objectives  

Result: Lean, structured dataset aligned with business questions.

---

## 6. Business Constraints and Final Dataset (40:30 – 45:40)

### 6.1 Budget Merge and Constraints
- Integrated budget data  
- Applied year-level filters  
- Enforced business rules  

### 6.2 Dataset Finalization
- Filtered records for 2017  
- Confirmed row consistency  
- Validated metric completeness  

Outcome: Analysis-ready dataset with business-constrained scope.

---

## 7. EDA Handoff (45:40 – 47:20)

- Final data validation  
- Schema confirmation  
- Readiness check for visualization or modeling  
- Clean transition to reporting phase  

---

## Tools Used

- Python  
- Pandas  
- NumPy  
- Excel  
- Matplotlib (for validation visuals)  

---

## Key Skills Demonstrated

- Business problem framing  
- Data profiling and validation  
- Multi-table data modeling  
- Data quality assessment  
- Feature engineering  
- Dataset standardization  
- Business-rule enforcement  

---

## Final Deliverable

A cleaned, validated, business-aligned dataset ready for:

- Power BI dashboarding  
- Statistical analysis  
- Predictive modeling  
- Executive reporting  
