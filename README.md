# Hospital Operations & Financial Performance Analysis

### Interactive Healthcare Analytics Dashboard | Microsoft Excel | 2020–2025

This project presents an interactive Microsoft Excel dashboard developed to analyse hospital admissions, operational efficiency, departmental activity, billing patterns, insurance coverage, and financial performance.

The analysis integrates multiple hospital management datasets using Excel XLOOKUP functions and uses PivotTables, PivotCharts, slicers, and a timeline to support interactive exploration of hospital operations.

The project demonstrates practical skills in **data integration, data validation, exploratory data analysis, dashboard development, and communicating healthcare business insights**.

## Dashboard Preview

![Hospital Operations & Financial Performance Dashboard](hospital_dashboard.png)

## 1. Project Overview

Hospitals generate large volumes of operational and financial data relating to patient admissions, inpatient care, departmental activities, and billing transactions. Analysing these records can help identify patterns in hospital activity, resource utilisation, and financial performance.

The objective of this project was to develop an interactive Excel dashboard that brings together operational and financial indicators into a single reporting interface.

### Project Objectives

- Analyse hospital admission volumes and trends across the reporting period.
- Compare patient admissions across hospital departments.
- Identify the most frequently recorded disease categories.
- Examine average hospital length of stay.
- Evaluate departmental and monthly billing patterns.
- Compare insurance-covered and patient-payable billing amounts.
- Assess recorded billing status and itemised charges.
- Enable interactive exploration using Excel slicers and a timeline.

The analysis covers **45,000 hospital admissions from 2020 to 2025**.

## 2. Data Source

**Dataset:** Hospital HMIS Dataset for Healthcare Analytics  
**Creator:** shalakagangurde  
**Source:** [Kaggle — Hospital HMIS Dataset for Healthcare Analytics](https://www.kaggle.com/datasets/shalakagangurde/hospital-hmis-dataset-for-healthcare-analytics/data)

The project uses a synthetic Hospital Management Information System (HMIS) dataset obtained from Kaggle.

According to the dataset creator, the data is entirely synthetic and does not contain real patient or hospital records. It is intended for educational, research, and demonstration purposes.

The dataset consists of multiple related tables containing hospital admissions, patient information, departments, wards, diseases, billing records, and other healthcare operational information.

Relevant tables were integrated into a consolidated Excel dataset for analysis.

## 3. Tools and Technologies

| Tool / Technique | Application |
|---|---|
| Microsoft Excel | Data preparation, analysis, and dashboard development |
| XLOOKUP | Combining information from related datasets |
| DATEDIF | Calculating hospital length of stay |
| Excel Tables | Organising and managing structured data |
| PivotTables | Aggregating admissions and financial measures |
| PivotCharts | Visualising operational and financial trends |
| Slicers | Interactive filtering by admission type, department, and disease category |
| Timeline | Filtering records by admission date |
| Excel Formulas | Calculating and validating performance indicators |

## 4. Data Preparation and Validation

The original dataset contained multiple related CSV files. Relevant information was combined into a consolidated admission-level analytical dataset using Microsoft Excel.

### Data Integration

XLOOKUP functions were used to retrieve information from related hospital tables using their corresponding identifiers.

The integrated dataset included:

- Admission and discharge dates
- Admission type and admission status
- Patient identifiers
- Department and ward information
- Disease names and categories
- Length of stay
- Total billing amounts
- Insurance-covered amounts
- Patient-payable amounts
- Payment status and payment method
- Billing dates

This integration enabled hospital operational and financial information to be analysed together.

### Data Transformation

Length of stay was calculated using admission and discharge dates.

The following Excel formula was used:

`=DATEDIF([@[admission_date]],[@[discharge_date]],"D")`

The calculated field represents the number of days between admission and discharge.

### Data Validation

Several checks were performed to support the accuracy of the analysis:

- Verified that the consolidated dataset contained 45,000 admission records.
- Checked that each admission ID appeared only once.
- Reviewed the integrated dataset for missing values.
- Validated the total billing amount against the original billing data.
- Confirmed that the dashboard's total billing matched the source billing total of **£1,684,246,109**.
- Checked that the KPI calculations were consistent with the underlying data.

PivotTables were subsequently created to aggregate the data for dashboard visualisations.

## 5. Key Performance Indicators

The dashboard presents four principal performance indicators for the full reporting period.

| KPI | Value |
|---|---:|
| Total Hospital Admissions | 45,000 |
| Average Length of Stay | 5.2 days |
| Total Recorded Billing | £1,684,246,109 |
| Average Billing per Admission | £37,428 |

These indicators provide a high-level summary of hospital activity, inpatient utilisation, and recorded billing performance.

## 6. Dashboard Analysis

The dashboard is organised around hospital operational performance and financial activity.

### 6.1 Hospital Admissions by Department

A column chart compares total admissions across six departments:

- Emergency
- Intensive Care Unit (ICU)
- Internal Medicine
- Orthopedics
- Pediatrics
- Surgery

This analysis identifies differences in admission volumes and highlights departments with relatively higher or lower patient activity.

### 6.2 Monthly Admissions Trend

A line chart displays monthly hospital admissions from 2020 to 2025.

The analysis examines changes in admission volumes over time, helping identify fluctuations in hospital activity and possible periods of increased demand.

### 6.3 Admissions by Disease Category

A horizontal bar chart compares admission volumes across disease categories, including infectious, surgical, respiratory, cardiac, pediatric, neurological, and other conditions.

This analysis highlights the relative contribution of different disease categories to overall hospital admissions.

### 6.4 Average Length of Stay

Average length of stay was calculated using the difference between admission and discharge dates.

The resulting KPI provides an overall measure of the duration of hospital stays.

Length of stay is relevant to hospital operations because prolonged admissions may affect inpatient capacity, resource requirements, and patient flow.

### 6.5 Total Billing by Department

A horizontal bar chart compares total recorded billing across hospital departments.

This analysis identifies departments associated with the largest billing amounts and supports comparisons of financial activity across clinical services.

### 6.6 Monthly Billing Trend

A line chart displays monthly billing amounts across the reporting period.

The analysis examines fluctuations in recorded billing activity over time.

### 6.7 Insurance-Covered vs Patient-Payable Billing

A stacked column chart compares the amounts covered by insurance providers and the amounts payable by patients across hospital departments.

This provides an overview of how recorded billing responsibilities are distributed between insurance and patients.

### 6.8 Billing Status: Paid vs Pending

A doughnut chart compares billing amounts classified as paid and pending.

This analysis provides an overview of the recorded payment status of hospital bills.

### 6.9 Itemised Charges by Type

A column chart examines itemised billing amounts across the following categories:

- Room charges
- Procedure charges
- Diagnostic test charges
- Drug charges

This analysis identifies the categories contributing most to itemised billing activity.

### 6.10 Interactive Dashboard Features

The dashboard includes:

- An admission-date timeline
- Admission-type slicer
- Department slicer
- Disease-category slicer

These controls enable users to filter the dashboard and explore hospital activity and financial performance for selected periods and categories.

## 7. Key Findings and Insights

### 7.1 Hospital Admissions

The dataset contains **45,000 hospital admissions** across the 2020–2025 reporting period.

Monthly admission volumes remained relatively stable overall, although fluctuations were observed throughout the reporting period.

Surgery recorded the highest number of admissions among the six departments, while ICU recorded the lowest.

These findings illustrate differences in patient activity across hospital services.

### 7.2 Average Length of Stay

The overall average length of stay was **5.2 days**.

This provides a summary of inpatient stay duration across the dataset.

Further departmental analysis would be required to determine whether particular services experience longer hospital stays.

### 7.3 Departmental Financial Performance

Total recorded billing amounted to **£1,684,246,109**, with an average billing amount of approximately **£37,428 per admission**.

Surgery recorded the highest total departmental billing at approximately **£377.2 million**, followed by Pediatrics at approximately **£315.7 million**.

ICU recorded the lowest total departmental billing at approximately **£149.4 million**.

These differences may reflect variations in admission volumes, service types, and the complexity of care delivered.

### 7.4 Disease Category Distribution

Infectious diseases accounted for the largest admission volume among the disease categories displayed.

Surgical conditions represented the second-largest category.

These findings highlight the relative distribution of recorded hospital admissions across disease groups.

### 7.5 Billing and Payment Status

The dashboard recorded approximately:

- **£833.0 million** in bills classified as paid.
- **£851.2 million** in bills classified as pending.

Pending bills represented approximately **50.5%** of the total recorded billing amount.

This indicates that a slightly larger proportion of the billing value was classified as pending than paid.

However, payment status does not necessarily establish whether the corresponding funds have been received.

### 7.6 Itemised Billing Charges

Room charges accounted for the largest amount among the itemised billing categories displayed, followed by procedure charges.

Diagnostic test and drug charges contributed smaller amounts.

This highlights the relative composition of recorded itemised charges.


## 8. Limitations

This is a descriptive analysis of the available hospital records. Differences in departmental billing may reflect admission volumes, patient complexity, or service types.

Billing amounts represent recorded charges and should not automatically be interpreted as collected revenue or hospital profit.

## How to Explore the Dashboard

Download the Excel workbook from this repository and open it in Microsoft Excel.

Use the interactive slicers and timeline to explore admission types, departments, disease categories, and reporting periods.
