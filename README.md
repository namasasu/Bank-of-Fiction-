# Bank-of-Fiction-
Key insights and ETL pipeline for Bank of Fiction. Please refer note, the data used is fictitious.
Project Summary
Bank of Fiction Customer Analytics Platform - Databricks Unity Catalog

This is a production-ready customer churn analytics platform using Databricks with complete medallion architecture (Bronze/Silver/Gold layers). The platform processes 10K+ banking customer records with comprehensive data quality controls and business-ready analytics.

Technical Architecture:

Bronze Layer: Ingested raw customer data with two source tables (bank_churn and bank_churn_messy) containing demographic, financial, and behavioral attributes

Silver Layer: Implemented ETL transformations with sophisticated data cleansing including:

Type conversion (STRING to DOUBLE for financial data)
Geography standardization (consolidated 5 variants into 3 standardized values)
Currency symbol removal and numeric validation
NULL placeholder handling and data quality validation
Duplicate detection and referential integrity checks
Gold Layer: Created 3 pre-aggregated business analytics tables:

Customer demographics summary (age, gender, credit scores by geography)
Customer financial metrics (salary distributions, income segmentation)
Customer tenure analysis (loyalty cohorts, retention metrics)
Engineering Excellence:

Built reusable Python error handling utilities (DataOperationError exception class, safe table operations, validation functions)
Comprehensive exception handling across all operations (ParseException, AnalysisException)
Multi-step validation processes with rollback capability
Detailed logging with timestamps and status tracking
Graceful degradation patterns for production resilience
Key Metrics Delivered:

10,001 customer records across 3 geographic markets (France, Germany, Spain)
8 demographic and financial attributes per customer
3 gold layer analytics tables supporting executive dashboards
99.97% data quality (only 3 missing values across 10K records)
Technologies: Databricks Unity Catalog, PySpark, SQL, Python, Medallion Architecture, ETL, Data Quality Engineering

Business Impact: Enabled customer segmentation analysis, geographic market comparison, loyalty tracking, and churn prediction readiness through validated, analytics-ready datasets.

Dashboard and insights: https://dbc-ca9bcb57-4aa3.cloud.databricks.com/dashboardsv3/01f14965e79d11498290efb0fd9e3e79/published?o=7474656912461022
