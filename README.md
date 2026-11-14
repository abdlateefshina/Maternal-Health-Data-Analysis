# Improving Maternal Health Insights Through Data Analysis

### A Python-Based Analysis of Maternal Healthcare Indicators in Nigeria

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?logo=pandas)

## Project Overview

Maternal health remains an important public health concern in Nigeria. Understanding patterns in maternal healthcare utilisation is essential for identifying service gaps and supporting evidence-informed healthcare planning.

**Improving Maternal Health Insights Through Data Analysis** is a collaborative Python-based project that explores maternal healthcare indicators in Nigeria using data from the 2024 Nigeria Demographic and Health Survey (NDHS).

The project focuses on assessing selected aspects of maternal health data quality and analyzing patterns in antenatal care utilisation, place of delivery, and Caesarean section deliveries.

Using Python, we performed data inspection, cleaning, preprocessing, exploratory data analysis, statistical analysis, complex survey-weighted estimation, and visualization to generate meaningful insights from the dataset.

The project was completed as the final project of the **Python Study Group (PSG)** organized by **SmartBizCrux Technologies**.

---

## Problem Statement

Effective maternal healthcare planning depends on the availability of reliable and properly managed health data.

However, incomplete records, missing responses, inconsistent entries, and limitations in data reporting can affect the quality of health information available for analysis and decision-making.

This project explores how Python can be used to prepare, assess, analyze, and visualize maternal health data to identify patterns in healthcare utilisation and provide insights that can support further investigation into maternal healthcare in Nigeria.

---

## Project Aim and Objectives

### Aim

To demonstrate how Python-based data cleaning, statistical analysis, and visualization can support better understanding and monitoring of maternal healthcare indicators in Nigeria.

### Objectives

- Examine the structure and quality of the selected maternal health dataset.
- Identify missing values, special response codes, and potential data inconsistencies.
- Extract and prepare relevant maternal healthcare variables.
- Analyze antenatal care utilisation and place of delivery.
- Examine differences in delivery patterns across demographic and socioeconomic groups.
- Incorporate DHS survey design information into statistical estimation.
- Generate visualizations and interpret findings.
- Provide recommendations for further maternal health research and data improvement.

---

## Data Source

**Dataset:** Nigeria Demographic and Health Survey (NDHS) 2024 Individual Recode Dataset.

**Dataset File:** `NGIR8BFL.dta`

**Format:** Stata (.DTA)

**Source:** [The Demographic and Health Surveys (DHS) Program](https://dhsprogram.com/)

### Original Dataset Overview

| Description | Value |
|---|---:|
| Country | Nigeria |
| Survey Year | 2024 |
| Original Records | 39,050 |
| Original Variables | 6,411 |
| Records in Maternal Analysis Dataset | 13,968 |

The original dataset contained thousands of variables. Relevant demographic and maternal healthcare variables were identified and extracted to create a smaller dataset for analysis.

### Selected Variables

The project focused on the following variables:

| Variable | Description |
|---|---|
| Age | Respondent's age |
| Residence | Urban or rural residence |
| Education | Highest educational attainment |
| Wealth Group | Household wealth index |
| Tetanus Category | Number of tetanus injections before birth |
| Antenatal Visits | Number of antenatal care visits |
| Delivery Group | Place of delivery |
| Caesarean Section | Whether delivery was by Caesarean section |

Additional survey-design variables were incorporated for weighted analysis.

**Data Access Note:** The original NDHS microdata is not included in this public repository because of applicable DHS data-use and redistribution conditions. Users should obtain authorized access directly from the DHS Program.

---

## Methodology and Workflow

The project followed a structured data analysis workflow.

### 1. Data Loading and Inspection
- Imported the Stata dataset using Pandas.
- Examined the dataset's dimensions, columns, and data types.
- Reviewed variable names and identified relevant maternal healthcare indicators.
- Consulted the dataset documentation and codebook.

### 2. Data Cleaning and Preparation
- Extracted relevant demographic and maternal healthcare variables.
- Investigated missing-value patterns.
- Examined special response codes and invalid values.
- Converted special "Don't know" responses into missing values where appropriate.
- Renamed variables for easier interpretation.
- Converted numerical codes into meaningful categorical labels.
- Validated the cleaned analysis dataset.

### 3. Exploratory Data Analysis (EDA)
- Examined respondents' demographic characteristics.
- Analyzed age, residence, education, and household wealth distributions.
- Explored antenatal care visits.
- Investigated delivery patterns across demographic and socioeconomic groups.

### 4. Statistical Analysis
- Conducted Chi-square tests of independence to examine associations between delivery location and selected demographic characteristics.
- Incorporated DHS sampling weights, primary sampling units, and strata.
- Applied survey-weighted statistical estimation using Samplics.
- Calculated weighted proportions, means, standard errors, and 95% confidence intervals.

### 5. Data Visualization
Created visualizations to communicate important findings, including:

- Overall distribution of delivery locations.
- Delivery patterns by residence.
- Delivery patterns by educational attainment.
- Delivery patterns by household wealth.
- Mean antenatal care visits with confidence intervals.

### 6. Interpretation and Reporting
- Interpreted the statistical results and visualizations.
- Identified patterns in maternal healthcare utilisation.
- Documented limitations.
- Developed recommendations for further investigation.

---

## Key Findings and Insights

The survey-weighted analysis revealed several important patterns.

### 1. Distribution of Place of Delivery

The analysis showed that home delivery accounted for the largest proportion of deliveries.

| Place of Delivery | Weighted Proportion |
|---|---:|
| Home | 57.2% |
| Public Health Facility | 27.0% |
| Private Health Facility | 14.4% |
| NGO Facility | 0.9% |
| Other | 0.5% |

**Key Insight:** Home delivery represented the majority of deliveries in the analyzed survey population.

### 2. Place of Delivery by Residence

Delivery patterns differed considerably between urban and rural women.

- Approximately 71.4% of rural deliveries occurred at home.
- Approximately 34.3% of urban deliveries occurred at home.
- Urban women recorded higher proportions of public and private facility deliveries.

**Key Insight:** Rural women had a substantially higher proportion of home deliveries than urban women.

### 3. Place of Delivery by Educational Attainment

The analysis revealed differences in delivery patterns across educational categories.

- Home delivery was approximately 82% among women with no formal education.
- Home delivery was approximately 10% among women with higher education.
- Facility deliveries were more prevalent among women with higher educational attainment.

**Key Insight:** Higher educational attainment was associated with a greater proportion of facility-based deliveries.

### 4. Place of Delivery by Household Wealth

Household wealth also showed considerable differences in delivery patterns.

- Home delivery decreased from approximately 83% among the poorest women to approximately 11% among the richest women.
- Private facility delivery increased from approximately 2% among the poorest women to approximately 43% among the richest women.

**Key Insight:** Delivery patterns varied substantially across household wealth groups.

### 5. Antenatal Care Utilisation

The survey-weighted mean number of antenatal care visits was:

**4.31 visits**

95% Confidence Interval: **4.16–4.45 visits**

This provides an overview of antenatal care utilisation among the eligible survey population.

### 6. Caesarean Section Deliveries

The weighted analysis showed:

- Caesarean section deliveries: 5.3%
- Non-Caesarean deliveries: 94.7%

These findings describe the distribution of delivery methods within the relevant survey population.

---

## Statistical Analysis

The project incorporated statistical techniques to explore relationships between maternal healthcare utilisation and selected demographic characteristics.

### Chi-square Test of Independence

Preliminary Chi-square tests examined associations between place of delivery and:

- Residence
- Educational attainment
- Household wealth

The results indicated statistically significant associations:

| Relationship | Chi-square Statistic | P-value |
|---|---:|---:|
| Residence and Delivery Location | 1739.48 | < 0.001 |
| Education and Delivery Location | 4363.94 | < 0.001 |
| Household Wealth and Delivery Location | 4161.77 | < 0.001 |

**Important:** These Chi-square tests were preliminary, unweighted analyses. They did not account for the complex DHS survey design and should not be interpreted as survey-adjusted significance tests.

### DHS Survey-Weighted Analysis

To account for the complex survey design, the project incorporated:

- Individual sampling weights (v005).
- Primary Sampling Units (v021).
- Sampling strata (v022).

The Samplics Python library was used to calculate survey-weighted estimates with Taylor-series variance estimation.

This approach helped account for the survey design when estimating proportions, means, standard errors, and confidence intervals.

---

## Tools and Technologies

The project utilized the following tools and Python libraries:

| Tool / Library | Application |
|---|---|
| Python | Programming and analysis |
| Jupyter Notebook | Development environment |
| Pandas | Data manipulation and cleaning |
| NumPy | Numerical operations |
| Matplotlib | Data visualization |
| Samplics | Complex survey statistical analysis |

Additional tools:

- Git
- GitHub

---

## Project Structure

```text
MATERNAL HEALTH ANALYSIS PROJECT/
│
├── IMAGES/
│   ├── 01_overall_place_of_delivery.png
│   ├── 02_delivery_by_residence.png
│   ├── 04_delivery_by_wealth.png
│   ├── 05_mean_antenatal_visits.png
│   ├── MHAP SS 1.png
│   ├── MHAP SS 2.png
│   ├── MHAP SS 6.png
│   ├── MHAP SS 7.png
│   ├── Picture2.png
│   └── Picture3.png
│
├── NOTEBOOK/
│   └── Maternal Health Analysis.ipynb
│
├── PROPOSAL/
│   ├── MATERNAL HEALTH ANALYSIS PROJECT METHODOLOGY.pdf
│   └── MATERNAL HEALTH ANALYSIS PROJECT PROPOSAL.pdf
│
├── REPORT/
│   ├── MATERNAL HEALTH ANALYSIS PROJECT CODEBOOK.pdf
│   └── MATERNAL HEALTH ANALYSIS PROJECT SOLUTION REPORT.pdf
│
├── README.md
├── requirements.txt
└── .gitignore
```

The original restricted NDHS dataset is intentionally excluded.

---

## Limitations of the Project

- The analysis is based on secondary data from the 2024 Nigeria Demographic and Health Survey.
- Some maternal health variables contain missing responses and special response codes.
- Different indicators have different eligible respondent populations and valid-response denominators.
- The analysis is limited to the selected variables available in the dataset.
- The Chi-square tests were not adjusted for the complex DHS survey design.
- Observed associations do not establish causation.
- The findings should not be interpreted as clinical recommendations or individual-level predictions.

---

## Recommendations and Future Improvements

The project provides a foundation for further investigation.

Potential areas for future work include:

1. Conducting survey-adjusted regression analysis to investigate factors associated with delivery location.
2. Examining geographical differences in maternal healthcare utilisation across Nigerian states and regions.
3. Investigating antenatal care utilisation across residence, education, and wealth groups.
4. Performing survey-adjusted statistical tests.
5. Exploring missing-data patterns and their implications for maternal health analysis.
6. Developing more comprehensive visualizations and interactive dashboards.
7. Exploring additional maternal healthcare indicators where suitable data are available.

---

## Project Contributors

This project was collaboratively completed by:

- **AbdLateef Shina**
- **Chukwuemeka Somtochukwu Promise**

---

## Project Background

**Industry:** Healthcare

**Project Type:** Collaborative Project

**Approach:** Python-Based Maternal Health Data Analysis

---

## Conclusion

This project demonstrated how Python can be applied to maternal health data preparation, quality assessment, statistical analysis, and visualization.

By analyzing the 2024 Nigeria Demographic and Health Survey, we identified notable differences in maternal healthcare utilisation across residence, educational attainment, and household wealth groups.

Beyond the technical experience, this project strengthened our understanding of the importance of reliable health data in identifying patterns, supporting research, and informing healthcare planning.

**Better data. Better insights. Better-informed healthcare decisions.**

---

Thank you for visiting our project repository!
