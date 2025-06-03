# Azure ETL & BI Migration Project — Real-World Experience (Documented from Memory)

This document describes a real-world enterprise project I contributed to as a Senior SQL BI Developer. While I no longer have access to company assets, it reflects my direct responsibilities and contributions in detail. While I no longer have access to the original systems due to company policies, this write-up reflects my real contribution in detail.

---

## Team & Structure

- Role: Senior SQL BI Developer in Cloud Data Team
- Team Composition: Solution Architect, 2 Team Leads, 6 Senior/Junior Developers, PM, BA, QA Tester
- Project Scope: End-to-end backend & BI migration from on-premise infrastructure to Microsoft Azure

---

## Technologies Used

- Database & Scripting: Microsoft SQL Server, T-SQL, Stored Procedures, UDFs, Triggers
- Cloud & ETL: Azure Data Factory, Azure Synapse Dedicated SQL Pool, Blob Storage, SharePoint, Azure VMs
- Reporting: Power BI Service
- Version Control: Git, Azure DevOps

---

## 🔍 Project Highlights

- Migrated enterprise data platform from Informatica to Azure cloud stack
- Integrated 6+ data sources into a centralized warehouse
- Designed high-performance backend structures and data marts
- Delivered clean and report-ready data for enterprise-wide Power BI usage


---

## Project Overview

My team was responsible for migrating legacy on-prem systems and ETL pipelines (originally built on Informatica) into the Microsoft Azure ecosystem.  
The end goal was to centralize all analytics data into a single Data Warehouse and deliver it through interactive BI dashboards to upper management.

---

## Architecture (Described in Words)

- Multiple data sources (SQL Server from Azure VMs, Blob Storage files, SharePoint, etc.)
- Ingested into staging tables using ADF pipelines (Copy and Data Flow)
- Data transformations were implemented using both full and incremental load strategies, with watermarking logic based on `modified_at > @last_run_time`
- The target system was a centralized Azure Synapse Dedicated SQL Pool, 
where:
  - Dimension tables (`dim_member`, `dim_provider`, etc.)
  - Fact tables (`fact_claims`, `fact_utilization`)
- Final data was consumed by Power BI dashboards for different business units

---

## My Responsibilities
As part of the Cloud Data Team, I worked across all phases of the project — from backend schema redesign to ETL pipeline development and reporting layer integration.

### 1. OLTP Data Modeling
- Designed and built backend database structure for an upgraded internal application
- Created complex T-SQL scripts for:
  - Tables, constraints, indexes
  - Stored procedures, user-defined functions, triggers

### 2. ETL Pipeline Development
- Created ADF pipelines from scratch
- Designed logic for both **initial full loads** and **incremental delta loads**
- Integrated data from 5–6 different source systems
- Applied watermarking for performance and idempotency

### 3. Data Warehouse Design
- Designed and implemented dimensional models
- Created ETL logic for `dim_` and `fact_` tables
- Ensured referential integrity and optimization for Power BI consumption

### 4. Power BI Reporting Support
- Enabled reporting across departments
- Reports visualized KPIs like:
  - Sales volume
  - Cost metrics
  - Operational performance
  - Productivity by pipeline
- Reports served upper management (CEO, VPs, Directors)

---

## Why This Project Is Documented in Markdown

Due to NDA and policy constraints, I do not have access to source code, diagrams, or dashboards. This Markdown file is a **professional and ethical** representation of my role and the technical complexity of the project I delivered as part of a team.

