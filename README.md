# EDA Project – End-to-End Exploratory Data Analysis

## 1. Executive Overview

The objective was to transform fragmented operational records into a validated, relational, business-constrained analytical dataset suitable for KPI tracking, dashboard development, and downstream statistical modeling.

The approach prioritizes:

- Structural correctness
- Referential integrity
- Data quality governance
- Business rule enforcement
- Analytical readiness validation

This project reflects production-style dataset preparation rather than exploratory visualization.

---

## 2. Business Context

The dataset represents commercial sales operations enriched with:

- Customer master information  
- Product master attributes  
- Geographic hierarchy (Region, State)  
- Annual budget allocations  

The business required a unified dataset to:

- Measure revenue and profit performance
- Compare regional contribution
- Analyze product-level profitability
- Evaluate budget vs actual variance
- Isolate performance for reporting year 2017

The primary challenge was structural fragmentation across multiple sheets with no enforced relational schema.

---

## 3. Data Architecture

### 3.1 Source Structure

Multi-sheet Excel workbook containing:

1. Sales (transactional fact table)
2. Customers (dimension)
3. Products (dimension)
4. Regions (dimension)
5. States (dimension)
6. Budget (fact table at yearly aggregation)

The Sales sheet serves as the central transactional entity.

### 3.2 Data Modeling Strategy

Target design:

Fact Table:
- Sales transactions enriched with customer, product, and geography attributes

Dimension Tables:
- Customer
- Product
- Region
- State

Supporting Fact:
- Budget integrated at year-level granularity

Goal: Flatten into a single denormalized analytical dataset while preserving referential consistency.

---

## 4. Implementation Methodology

### Phase 1: Data Ingestion

- Loaded Excel workbook using pandas
- Enumerated sheet names
- Loaded each sheet into independent DataFrames
- Verified row counts for ingestion accuracy
- Checked column uniqueness within each sheet

Control Objective:
Ensure no structural corruption during import.

---

### Phase 2: Schema Normalization

Performed systematic standardization:

- Trimmed whitespace in column headers
- Converted column names to consistent case format
- Removed special characters
- Standardized date formats
- Enforced numeric types for revenue, cost, and quantity fields
- Ensured categorical fields were correctly cast

Validation:
- Confirmed dtype alignment
- Ensured no object-type numeric leakage

---

### Phase 3: Data Profiling

Profiling included:

1. Null Value Analysis  
   - Calculated null percentage per column  
   - Identified mandatory key fields  
   - Assessed impact of null-heavy attributes  

2. Duplicate Detection  
   - Checked full-row duplicates  
   - Verified uniqueness of primary keys in dimension tables  

3. Cardinality Assessment  
   - Evaluated distinct counts  
   - Verified foreign key distributions  

4. Range and Consistency Checks  
   - Validated revenue and profit ranges  
   - Ensured no negative quantities where business logic disallowed  

Objective:
Eliminate structural and logical inconsistencies before modeling.

---

### Phase 4: Relational Integration

Merge strategy followed controlled sequence:

1. Sales joined with Customers on Customer_ID  
2. Sales joined with Products on Product_ID  
3. Sales joined with State on State_ID  
4. State joined with Region  
5. Budget merged based on Year and relevant dimensions  

After each merge:

- Compared pre- and post-merge row counts  
- Verified no unintended row expansion  
- Assessed null propagation in join columns  
- Confirmed referential match completeness  

Join Types:
- Primarily left joins to preserve transactional integrity  

Outcome:
Unified analytical dataset with enriched dimensional context.

---

### Phase 5: Dimensional Refinement

Post-merge cleanup included:

- Removal of duplicate key columns
- Elimination of intermediate join attributes
- Consolidation of redundant descriptors
- Column renaming for clarity
- Reordering fields for analytical usability

Feature Optimization:
- Retained revenue, cost, quantity, margin, geography, product category, and customer segment
- Removed low-signal or redundant metadata columns

Result:
Reduced dimensional noise and improved interpretability.

---

### Phase 6: Business Rule Enforcement

Applied explicit constraints:

- Filtered dataset to reporting year 2017
- Validated revenue totals before and after filtering
- Recalculated derived metrics (Profit = Revenue − Cost)
- Cross-checked budget alignment for completeness

Ensured:
- No metric distortion post-filter
- Aggregates matched expected totals

---

## 5. Final Dataset Characteristics

The final dataset:

- Is fully denormalized
- Contains only validated business-relevant attributes
- Has enforced referential integrity
- Is scoped strictly to 2017 reporting year
- Is free of duplicate primary keys
- Contains consistent data types across all metrics

This dataset is optimized for:

- Power BI modeling
- KPI dashboarding
- Variance analysis
- Forecasting and regression modeling
- Executive performance reporting

---

## 6. Validation Controls Implemented

- Row count reconciliation after each merge
- Aggregate revenue validation
- Profit recomputation check
- Null distribution review post-cleanup
- Schema consistency verification
- Dimensional uniqueness checks

This ensures analytical reliability and audit traceability.

---

## 7. Technical Stack

- Python
- Pandas
- NumPy
- Excel
- Matplotlib (profiling validation)

---

## 8. Competencies Demonstrated

- Business problem translation into data architecture
- Structured EDA methodology
- Multi-entity relational modeling
- Referential integrity enforcement
- Data quality governance
- Dimensional optimization
- Business constraint application
- Production-ready dataset preparation

---

## 9. Deliverable

A validated, relational, business-aligned analytical dataset prepared for enterprise-grade reporting and advanced analytics workflows.
