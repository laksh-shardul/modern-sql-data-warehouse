# SQL Data Warehouse Project  
End-to-End Data Warehouse Implementation Using SQL Server

This repository contains an end-to-end implementation of a **modern SQL-based data warehouse**, built by following a structured project plan covering **architecture design, ETL development, dimensional modeling, and analytical querying**.  
The project demonstrates how raw data from multiple source systems can be transformed into a **clean, analytics-ready star schema** suitable for reporting and decision support.

---

## Project Scope & Objective

The objective of this project is to gain hands-on experience in:
- Designing a data warehouse architecture
- Implementing ETL pipelines using SQL
- Applying dimensional modeling principles
- Organizing a real-world analytics project using version control and documentation

The focus is on **correct implementation of industry-standard patterns**, not on ad-hoc querying.

---

## Project Structure & Architecture

### High-Level Data Flow

Source Systems  
→ Bronze Layer (Raw Ingestion)  
→ Silver Layer (Cleaned & Conformed Data)  
→ Gold Layer (Dimensional Model)  
→ Analytical Queries

This layered approach ensures data quality, traceability, and separation of concerns.

---

## Architecture Design Decisions

- **Layered Architecture (Bronze / Silver / Gold)**  
  Used to progressively refine data from raw ingestion to analytics-ready structures.

- **SQL-First ETL**  
  All transformations are implemented using SQL to demonstrate strong relational reasoning.

- **Star Schema in Gold Layer**  
  Chosen for simplicity, query performance, and suitability for analytical workloads.

- **Stored Procedures for Loading Logic**  
  Used to encapsulate ETL logic and enable repeatable execution.

---

## Technologies Used

- SQL Server
- T-SQL
- Git & GitHub for version control
- Draw.io for architecture diagrams
- Notion for project planning and requirement analysis

---

## Implementation Breakdown

### 1. Project Planning & Requirement Analysis
- Defined project scope and objectives
- Analyzed source systems and data structures
- Planned architecture and workflow using Notion

### 2. Repository & Database Setup
- Established naming conventions
- Initialized Git repository
- Created database schemas for each layer
- Committed incremental changes following logical milestones

---

### 3. Bronze Layer – Raw Data Ingestion
- Analyzed source system structures
- Created DDL scripts for raw tables
- Developed SQL load scripts
- Implemented stored procedures for ingestion
- Documented data flow

Purpose: preserve raw data with minimal transformation.

---

### 4. Silver Layer – Data Cleaning & Transformation
- Explored and understood source data
- Cleaned and standardized customer, product, sales, and ERP datasets
- Handled nulls, formatting issues, and inconsistencies
- Created transformation logic using SQL
- Implemented stored procedures
- Documented refined data flow

Purpose: produce clean, conformed datasets suitable for modeling.

---

### 5. Gold Layer – Dimensional Modeling
- Applied dimensional modeling concepts
- Evaluated star schema vs snowflake schema
- Identified business objects
- Built:
  - Customer Dimension
  - Product Dimension
  - Sales Fact Table
- Established relationships and keys
- Constructed the final star schema
- Created a basic data catalog
- Documented analytical data flow

Purpose: enable efficient analytical queries and reporting.

---

## Analytical Outcomes

The final model supports:
- Time-based analysis
- Customer and product-level slicing
- Sales performance analysis
- Consistent metric calculation across dimensions

---

## Documentation & Version Control

- Data flow documented at each layer
- Clear folder structure and naming conventions
- Logical Git commits reflecting development stages
- Architecture diagrams included for clarity

---

## Learning Outcomes

Through this project, I gained practical experience in:
- Data warehouse architecture design
- ETL development using SQL
- Dimensional modeling fundamentals
- Organizing analytics projects professionally
- Translating raw data into analytics-ready structures

---

## Limitations & Future Enhancements

**Current Limitations**
- Static datasets
- Manual execution of ETL processes

**Future Improvements**
- Incremental loading strategies
- Performance optimization (indexing, partitioning)
- Automation using orchestration tools
- Expanded analytical use cases

---

## Why This Repository Matters

This project demonstrates the ability to:
- Follow a structured analytics engineering workflow
- Implement a complete data warehouse lifecycle
- Apply theoretical concepts in a practical setting
- Write clean, organized, and maintainable SQL

It reflects a **strong foundation for data analytics and analytics engineering roles**.
