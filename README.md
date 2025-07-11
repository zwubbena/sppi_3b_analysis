# SPPI 3B Multi-Level Reading Proficiency Analysis

This repository contains Python-based analyses and Excel workbooks examining **State Performance Plan Indicator (SPPI) 3B**, which measures reading proficiency among students with Individualized Education Programs (IEPs) in Texas. The analysis is based on the State of Texas Assessments of Academic Readiness (STAAR®) for English Language Arts (ELA) in Grades 4 and 8 and the English I End-of-Course (EOC) exam in High School, covering school years 2020–21 through 2023–24.

## Notebooks

- `sppi_3b_multi_level_state_analysis.ipynb`  
  Analyzes statewide SPPI 3B proficiency trends among students with IEPs, including breakdowns by grade and accommodation status.

- `sppi_3b_multi_level_region_analysis.ipynb`  
  Provides a comparative analysis of SPPI 3B proficiency trends for each Education Service Center (ESC) region relative to the statewide average.

Each notebook exports an Excel workbook with structured worksheets and visualizations.

---

## Analysis Structure

The workbook output from each program is organized into **four analytical levels**:

- **Level 1**: Proficiency rates by individual grade  
- **Level 2**: Combined proficiency rates across all grades  
- **Level 3**: Grade-level breakdown of proficiency by accommodation status (with vs. without accommodations)  
- **Level 4**: Combined accommodation breakdown across all grades  

This tiered structure supports a clear, step-by-step interpretation of statewide and regional trends in reading proficiency among students with IEPs.

---

## Worksheet Descriptions

| Worksheet | Description |
|-----------|-------------|
| `Data` | Contains the raw STAAR assessment data for students with IEPs, including proficiency and accommodation status across multiple school years. |
| `Data Dictionary` | Definitions and descriptions of each variable used in the analysis. |
| `Level 1 Grade 4` | Grade 4 ELA proficiency rates for students with IEPs statewide (with data table and trend graph). |
| `Level 1 Grade 8` | Grade 8 ELA proficiency rates for students with IEPs statewide (with data table and trend graph). |
| `Level 1 High School` | High School English I proficiency rates for students with IEPs statewide (with data table and trend graph). |
| `Level 2 Combined` | Combined proficiency rates across all three grades (Grades 4, 8, and HS) from 2020–21 to 2023–24. |
| `Level 3 Grade 4` | Grade 4 proficiency breakdown by accommodation status (with vs. without) among proficient IEP students. |
| `Level 3 Grade 8` | Grade 8 proficiency breakdown by accommodation status (with vs. without) among proficient IEP students. |
| `Level 3 High School` | High School proficiency breakdown by accommodation status (with vs. without) among proficient IEP students. |
| `Level 4 Combined` | Combined accommodation breakdown across all grades for proficient IEP students. |

---

## Key Terminology

| Term | Definition |
|------|------------|
| `ELA` | English Language Arts |
| `EOC` | End of Course |
| `IEP` | Individualized Education Program – Students with disabilities who receive special education services with IEPs. |
| `Level 1 & 2` | Y-Axis Label: % of IEP Students Proficient; What It Measures: Out of all IEP students, what % are proficient |
| `Level 3 & 4` | Y-Axis Label: % of Proficient Students with IEPs; What It Measures: Out of proficient IEP students, what % used/didn’t use accommodations |
| `Proficient` | Students who have met or exceeded the grade-level standards on the statewide assessment. |
| `STAAR` | State of Texas Assessments of Academic Readiness |
| `With Accommodations` | Students with IEPs who used testing accommodations and met or exceeded grade-level standards. |
| `Without Accommodations` | Students with IEPs who did not use testing accommodations and met or exceeded grade-level standards. |
| `Accommodations` | A student is considered to have received accommodations if they have a value of `1 = Yes` for both the `Special-Education-Code` variable and the `Accommodation(s)` variable on the STAAR ELA tests (Grade 4, Grade 8, or English I EOC). These data are sourced from the Consolidated Accountability File (CAF), which combines STAAR, STAAR Spanish, STAAR Alternate 2, TELPAS, and TELPAS Alternate data into a single record per student per year. [CAF Data File Format PDF](https://tea.texas.gov/texas-schools/accountability/academic-accountability/performance-reporting/2024-consolidated-accountability-file-data-file-format.pdf) |

---

## Data Dictionary

| Variable | Label | Description |
|----------|-------|-------------|
| `YEAR_FLAG` | Determination Year | The year the SPP/APR determination was issued (e.g., 2025). |
| `FFY` | Federal Fiscal Year | The federal fiscal year associated with the determination (e.g., YEAR_FLAG = 2025 is based on FFY 2023). |
| `SCHOOL_YEAR` | School Year | The academic year of the data submission (e.g., SY 2023–24). |
| `GROUP` | Administrative Level | The ESC region or statewide grouping reported. |
| `GRADE_LEVEL` | Grade Level | Grade 4, Grade 8, or High School. |
| `SUBJECT` | Subject Area | ELA for Grades 4 and 8; English I for High School. |
| `TOT_IEP_CNT` | Total IEP Students | Count of IEP students tested on STAAR. |
| `TOT_PROFICIENT_CNT` | Total Proficient Students | Count of IEP students scoring at or above grade level. |
| `TOT_PROFICIENT_PCT` | Total Proficient (%) | Percent of IEP students scoring at or above grade level. |
| `R_WITH_CNT` | Regular STAAR with Accommodations (Count) | Count of IEP students with accommodations scoring proficient on regular STAAR. |
| `R_WITH_PCT` | Regular STAAR with Accommodations (%) | Percent of IEP students with accommodations scoring proficient on regular STAAR. |
| `A_WITH_CNT` | Advanced STAAR with Accommodations (Count) | Count of IEP students with accommodations scoring proficient on advanced STAAR. |
| `A_WITH_PCT` | Advanced STAAR with Accommodations (%) | Percent of IEP students with accommodations scoring proficient on advanced STAAR. |
| `R_WOUT_CNT` | Regular STAAR without Accommodations (Count) | Count of IEP students without accommodations scoring proficient on regular STAAR. |
| `R_WOUT_PCT` | Regular STAAR without Accommodations (%) | Percent of IEP students without accommodations scoring proficient on regular STAAR. |
| `A_WOUT_CNT` | Advanced STAAR without Accommodations (Count) | Count of IEP students without accommodations scoring proficient on advanced STAAR. |
| `A_WOUT_PCT` | Advanced STAAR without Accommodations (%) | Percent of IEP students without accommodations scoring proficient on advanced STAAR. |
| `TOT_RA_WITH_CNT` | Total Proficient with Accommodations (Count) | Total IEP students scoring proficient (regular + advanced STAAR) with accommodations. |
| `TOT_RA_WITH_PCT` | Total Proficient with Accommodations (%) | Percent of IEP students scoring proficient (regular + advanced STAAR) with accommodations. |
| `TOT_RA_WOUT_CNT` | Total Proficient without Accommodations (Count) | Total IEP students scoring proficient (regular + advanced STAAR) without accommodations. |
| `TOT_RA_WOUT_PCT` | Total Proficient without Accommodations (%) | Percent of IEP students scoring proficient (regular + advanced STAAR) without accommodations. |
| `DATE_PROCESSED` | Processing Date | The date the data were processed for analysis. |

---

## Source

Texas Education Agency  
[Data and Reporting Team](https://tea.texas.gov/academics/special-student-populations/special-education/data-and-reports)

