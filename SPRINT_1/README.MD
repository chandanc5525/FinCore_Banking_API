# Sprint SQ1: Banking Data Warehouse Architecture & Schema Engineering

---

# Objective

```
Design, provision, and validate the enterprise-grade foundational schema for FinCoreDW, the central Banking Data Warehouse. This architecture uses a Kimball dimensional modeling approach (Star/Snowflake schemas) optimized for high-performance analytical processing (OLAP), historical tracking, and comprehensive cross-channel reporting.
```
---

# Core Tasks

```
1. Database Provisioning
Initialize the core analytical repository: FinCoreDW.

Establish optimal configuration settings for storage, indexing strategy, and logging protocols.

2. Dimension Modeling (Dim_)
Implement structural dimensions with system-invariant surrogate keys, source-system natural keys, operational attributes, and ETL audit metadata.

- Dim_Customer: Consolidates customer demographics, credit profiles, and risk-segmentation metrics.

- Dim_Account: Captures life-cycle milestones, operational statuses, and product categorization across core banking systems.

- Dim_Branch: Maps geographic and hierarchical organizational structures of the physical branch network.

- Dim_Date: Provides a standardized, pre-calculated temporal framework for cross-fact time-series analysis and financial reporting periods.

- Dim_Employee: Tracks organizational structures, reporting lines, and personnel roles (e.g., loan officers, tellers).

- Dim_Channel: Segregates transaction touchpoints into digital, physical, and automated modalities (e.g., ATM, Mobile, In-Branch).

- Dim_Transaction_Type: Standardizes the ledger classification system, mapping operational events to precise debit/credit indicators.

- Dim_Loan_Product: Catalogs commercial and retail lending offerings alongside base-rate frameworks.

- Dim_Card: Maintained as a secure dimension for tracking card-instrument profiles, tiers, and statuses using tokenized representations for compliance.

3. Fact Table Architecture (Fact_)
Construct multi-directional fact tables containing numeric, additive metrics and grain-specific foreign key constraints mapping back to the dimensions.

- Fact_Transaction: Captures high-frequency core banking transaction streams, tracking ledger balances post-execution.

- Fact_Loan: Employs an accumulating snapshot model to trace the performance, origination values, and principal outstandings of loan facilities.

- Fact_Card_Transaction: Tracks localized transaction records, merchant classifications, and processing indicators for card portfolios.

- Fact_Fixed_Deposit: Captures term-deposit liabilities, yield metrics, and maturity horizons.

4. Schema Validation & Integrity Testing
- Execute script-level verifications to validate structural presence and accurate database compilation.

- Enforce referential integrity checks via primary/foreign key matrix mappings.

- Profile data types to ensure consistent scale and precision for financial metrics (e.g., currency, interest calculations).
```

---
