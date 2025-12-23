# Financial Data Warehouse: Automated ERP-to-Analytics Pipeline

## 🎯 Project Overview
This repository contains a full-stack implementation of a **Modern Data Warehouse (MDW)** designed to transform fragmented financial source data into an audit-conscious **Star Schema**. 

As a **Chartered Accountant (CA)** transitioning into Data Engineering, my objective was to build a system that prioritizes **data integrity, idempotency, and reconcilability**. This project demonstrates the technical bridge between complex financial logic and scalable SQL architecture.

---

## 🏗 Architecture & Design Philosophy
The system follows a **Modular Layered Architecture** to ensure a "Single Version of Truth" (SVOT).

* **Bronze (Raw Ingestion):** Immutable storage of source system extracts. Minimal transformation to preserve data lineage.
* **Silver (Conformed Layer):** Data cleansing, type-casting, and standardization. This layer acts as the **Audit Layer**, where data is scrubbed of inconsistencies that would otherwise lead to financial misstatements.
* **Gold (Curated Dimensional Model):** A high-performance Star Schema optimized for BI tools (Tableau/Power BI). 

### Key Technical Decisions
* **Stored Procedure Encapsulation:** All ETL logic is encapsulated in Stored Procedures to allow for modularity and future orchestration (e.g., Airflow/dbt).
* **Idempotent Loading:** Scripts are designed to be repeatable; re-running the pipeline does not result in duplicate records or corrupted totals.
* **Referential Integrity:** Strict enforcement of Primary and Foreign Keys to ensure that financial reports never contain orphaned transactions.

---

## 🛠 Tech Stack
* **Engine:** SQL Server / T-SQL
* **Modeling:** Dimensional Modeling (Kimball Methodology)
* **Design:** Draw.io (ERDs) & Notion (Requirement Analysis)
* **Version Control:** Git (Feature-branch workflow)

---

## 💎 Financial Integrity Considerations:

1.  **Data Type Precision:** Implementation of precise numeric types (Decimal/Numeric) for financial values to prevent rounding errors common in float-based systems.
2.  **Null-Handling Logic:** Defensive SQL logic to prevent `NULL` values from aggregating incorrectly, which would mask missing revenue or expenses.
3.  **Schema Consistency:** Unified naming conventions across all layers to ensure that a "Customer ID" in the source is easily traceable to the final "Fact_Sales" table for reconciliation.

---

## 🚀 Implementation Milestones

### 1. Requirement Analysis
* Identified core business objects (Customers, Products, Sales).
* Mapped grain requirements for analytical queries (Time, Geography, Category).

### 2. ETL Development (Silver & Gold)
* Standardized disparate date formats into a unified ISO standard.
* Built **Dimension Tables** (SCD Type 1 logic) to maintain entity attributes.
* Engineered the **Sales Fact Table** to handle high-volume transactional data.

### 3. Analytical Readiness
* Verified the Star Schema against a series of complex analytical queries to ensure sub-second response times for business users.

---

## 📈 Outcomes & Future Roadmap
**Current State:**
* Successfully transforms raw ERP data into a query-optimized Gold layer.
* Full documentation of data flow and entity relationships.

**Roadmap:**
* **Incremental Loading:** Implementing Delta-load logic to reduce processing overhead.
* **Automated Reconciliation:** Developing a "Validation View" that automatically compares Bronze totals vs. Gold totals to flag discrepancies.

---

## 📚 References & Methodology
This project was implemented following industry-standard architectural patterns. The logic was manually implemented and extended to demonstrate mastery of the end-to-end SDLC in an analytics engineering context.

---

## 👔 Why This Repository Matters
This repository demonstrates:
1.  **Code with a Purpose:** SQL is used as a tool to solve the "Messy Data" problem in finance.
2.  **Architect for Scale:** The Star Schema is built with scalability and analytical consistency in mind.
3.  **Ensure Accuracy:** My CA background ensures that the data is not just "moving," but is **correct and reconcilable.**
