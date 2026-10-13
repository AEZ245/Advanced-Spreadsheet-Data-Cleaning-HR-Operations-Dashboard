# Portfolio Project 2: Advanced Spreadsheet Data Cleaning & HR Operations Dashboard

## Executive Summary
This project takes a raw, messy operational/financial human resources ledger and transforms it into an automated, stakeholder-ready reporting workbook. Built entirely using advanced spreadsheet formulas, data cleaning pipelines, custom conditional formatting, dynamic multi-table Pivot structures, and a global synchronized Slicer dashboard architecture.

---

## Technical Implementation & Steps Taken

### 1. Data Cleaning & Pipeline Setup
* **Raw Data Ingestion:** Handled raw operational/financial employee ledgers containing inconsistent text casing, spacing, and unformatted types.
* **Text Manipulation & Standardization:** Cleaned operational entries using text functions (`TRIM`, etc.) to ensure uniform categorization across departments, regions, and performance tiers.
* **Pipeline Structure:** Maintained a strict separation of concerns within the workbook architecture:
  * `Raw_Data`: Untouched source data to preserve data integrity.
  * `Clean_Data`: Automated transformation and staging layer.
  * `Summary_Dashboard`: Stakeholder-ready executive reporting layer.

### 2. Executive KPI Summary Layer
* Built a dedicated top-level executive KPI banner utilizing dynamic summary calculations (`COUNTIFS`, `SUMIFS`, and aggregations) to immediately surface high-level metrics without requiring manual lookup:
  * **Total Payroll:** $84,814,436.17
  * **Average Salary:** $85,155.06
  * **Total Headcount:** 1,020 employees

### 3. Advanced Dashboard Architecture & Pivot Tables
* **Multi-Table Grid Layout:** Designed a 2-column executive dashboard grid on the `Summary_Dashboard` sheet to eliminate vertical scrolling and present a clean "10-foot view" for leadership.
* **Department Breakdown:** Evaluated headcount and payroll distribution across organizational units (Admin, Cloud Tech, DevOps, Finance, HR, Sales).
* **Region Breakdown:** Analyzed geographical expense concentration and headcount footprints across regional markets (California, Florida, Illinois, Nevada, New York, Texas).
* **Performance Tier Breakdown:** Mapped salary distribution against performance ratings (Excellent, Good, Average, Poor) to ensure compensation alignment with merit.
* **Formatting & Professional Polish:**
  * Replaced default Excel table headers (`Row Labels`, `Sum of Salary`) with clean, professional labels (`Department`, `Region`, `Performance Rating`, `Headcount`, `Payroll`).
  * Enforced a unified **grayscale monochrome theme** across all tables, KPI cards, and slicers to maintain visual hierarchy.
  * Locked column widths by disabling *“Autofit column widths on update”* in Pivot Table Options to prevent layout scrambling during refreshes.

### 4. Interactive Global Slicer Control
* Inserted a dynamic **Remote Work** Slicer (`TRUE`/`FALSE`).
* Configured **Report Connections** so that a single click on the Slicer instantly and synchronously filters *all* operational Pivot Tables across the entire dashboard.
* Styled the Slicer to match the monochrome grayscale palette for a seamless UI experience.

---

## Workbook Structure
* `Raw_Data`: Raw source records.
* `Clean_Data`: Standardized data pipeline.
* `Summary_Dashboard`: Executive interface housing KPI cards, multi-table Pivot grid, and the global Slicer control panel.
