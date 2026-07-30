# Data Cleaning Report

## Overview

The dataset was reviewed to identify data quality issues that could affect the accuracy and reliability of the analysis.

The cleaning process was completed using **Power Query in Power BI**, with each transformation documented to ensure transparency and reproducibility.

---

# Data Quality Assessment

## Dataset Summary

| Attribute | Result |
|-----------|--------|
| Total Records | 23,486 |
| Duplicate Records | 0 |
| Empty Columns | 3 |
| Missing Values | Present in selected fields |

---

# Data Cleaning Summary

| Issue Identified | Action Taken | Reason |
|------------------|-------------|--------|
| Three empty columns (`Unnamed: 11`, `Unnamed: 12`, `Unnamed: 13`) | Removed | Columns contained no data and added no analytical value. |
| `Unnamed: 0` column | Renamed to **Review ID** | Improved readability and identified each review uniquely. |
| Missing values in **Title** | Retained | Review titles are optional and do not affect the analysis. |
| Missing values in **Review Text** | Retained | Ratings and recommendations remain valuable even without review text. |
| Missing values in **Division Name**, **Department Name**, and **Class Name** | Removed affected records | Product categorization was required for meaningful analysis. |
| Duplicate records | Checked | No duplicate records were found. |
| Data types | Verified | Ensured all fields used appropriate data types before analysis. |
| Text fields | Trimmed and cleaned | Removed unnecessary leading/trailing spaces and non-printable characters. |

---

# Data Transformations

The following calculated fields were created to support analysis and reporting:

| Calculated Field | Purpose |
|------------------|---------|
| Age Group | Group customers into age ranges for demographic analysis. |
| Rating Category | Categorize ratings into descriptive groups for reporting. |
| Recommendation Status | Replace binary values (0/1) with descriptive labels. |
| Review Length | Measure review length for additional analysis. |

---

# Data Quality Outcome

Following the cleaning process:

- Empty and unnecessary columns were removed.
- Duplicate records were eliminated (none found).
- Missing values were handled appropriately based on their business relevance.
- Text fields were standardized.
- Data types were validated.
- Additional analytical fields were created to support reporting and visualization.

The resulting dataset was considered analysis-ready and used for all subsequent exploratory analysis and dashboard development.
