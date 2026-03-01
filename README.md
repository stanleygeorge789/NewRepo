# EDA Project – End-to-End Exploratory Data Analysis

## 1. Executive Summary

This project demonstrates a production-oriented Exploratory Data Analysis workflow applied to a multi-entity Excel dataset containing transactional and master data.

The objective was to transform fragmented, loosely structured operational data into a validated, relational, business-constrained analytical dataset suitable for dashboarding, KPI monitoring, and advanced modeling.

The emphasis of this project is on:

- Data integrity
- Relational modeling
- Business rule enforcement
- Analytical readiness

This is not visualization-first analysis. It is structure-first analytics.

---

## 2. Business Context and Analytical Objective

The dataset represents operational sales data enriched with customer, product, geographic, and budget information.

Primary analytical goals:

- Evaluate revenue and profitability performance
- Compare regional performance
- Align actual performance against budget
- Enable year-specific performance tracking (2017 focus)

Key business questions addressed:

- Which regions drive the highest revenue and profit?
- How do product categories contribute to total margin?
- Where do actuals deviate from budget?
- Are there structural data quality issues that distort KPIs?

---

## 3. Data Sources and Structure

### 3.1 Source Format

Multi-sheet Excel workbook containing:

- Sales transactions
- Customer master
- Product master
- Regional mapping
- State mapping
- Budget data

Each sheet was structurally independent and required relational modeling before meaningful analysis.

### 3.2 Initial Challenges Identified

- Inconsistent headers
- Mixed data types
- Redundant columns across entities
- Potential null-heavy attributes
- Absence of enforced relational integrity

---

## 4. Methodology

### 4.1 Environment Setup

Environment configured using:

- Python
- Pandas
- NumPy
- Matplotlib

Structured workflow followed:

1. Load
2. Inspect
3. Profile
4. Clean
5. Model
6. Validate
7. Constrain

---

### 4.2 Data Ingestion

- Imported workbook using pandas
- Enumerated sheet names
- Assigned sheets to logical DataFrames
- Inspected schema consistency
- Verified column naming and structural alignment

Focus: Prevent silent structural corruption.

---

### 4.3 Structural Validation

Performed:

- Header normalization
- Column trimming and formatting
- Data type correction
- Date parsing validation
- Numeric coercion where required

This ensured type consistency for joins and aggregations.

---

### 4.4 Data Profiling and Quality Assessment

Conducted systematic profiling:

- Null value distribution analysis
- Duplicate record detection
- Cardinality inspection
- Outlier surface checks
- Row-level consistency validation

Identified and resolved:

- Missing key values
- Structural inconsistencies
- Non-business-relevant fields

Objective: Eliminate analytical distortion before modeling.

---

### 4.5 Relational Modeling and Entity Integration

Defined relational architecture:

- Identified primary keys in dimension tables
- Validated foreign keys in transaction table
- Established merge hierarchy

Merge sequence:

1. Sales + Customers
2. Sales + Products
3. Sales + Region
4. Sales + State
5. Sales + Budget

Validation performed after each merge:

- Row count comparison
- Join type evaluation
- Null propagation analysis
- Referential integrity checks

Outcome: Single unified analytical dataset with relational coherence.

---

### 4.6 Cleanup and Feature Optimization

Performed dimensional refinement:

- Removed duplicate attributes from joins
- Eliminated redundant columns
- Applied consistent naming conventions
- Reduced dimensional noise
- Retained only business-aligned variables

This reduced analytical complexity and improved clarity.

---

### 4.7 Business Constraint Enforcement

Applied business logic constraints:

- Integrated annual budget data
- Filtered dataset to 2017
- Validated metric completeness post-filter
- Rechecked row-level integrity

Ensured final dataset aligns strictly with defined reporting scope.

---

## 5. Validation and Readiness Checks

Final verification included:

- Aggregate revenue cross-check
- Profit recalculation validation
- Record count confirmation
- Schema final review

The dataset was confirmed ready for:

- Power BI reporting
- KPI dashboarding
- Statistical modeling
- Forecasting workflows

---

## 6. Technical Stack

- Python
- Pandas
- NumPy
- Excel
- Matplotlib

---

## 7. Core Competencies Demonstrated

- Business-aligned analytics design
- Data profiling discipline
- Relational data modeling
- Join strategy and validation
- Data quality governance
- Feature selection logic
- Analytical constraint enforcement
- Production-style dataset preparation

---

## 8. Deliverable

A clean, validated, relational dataset optimized for analytical consumption and executive reporting.

This dataset supports performance tracking, variance analysis, and region-level strategic decision-making.
