# HR Dashboards using Power BI 📊

> *Interactive HR Analytics Dashboard for Workforce Insights & Employee Attrition Analysis*

[![Power BI](https://img.shields.io/badge/Power-BI-F2C811?style=flat&logo=microsoftpowerbi&logoColor=black)](https://powerbi.microsoft.com)

---

## 🎯 Project Overview

This Power BI project delivers a comprehensive HR analytics dashboard designed to help HR professionals, managers, and decision-makers analyze workforce composition, track key HR metrics, and identify factors influencing employee attrition. Built with real-world HR datasets, this dashboard transforms raw employee data into actionable visual insights.

**📁 Dashboard File:** `HRByShireen.pbix`  
**👤 Created by:** Shireen Talaat

---

## 📋 Business Objectives

This dashboard addresses critical HR questions:

### 👥 Workforce Composition
- Analyze employee distribution by department, job role, education field, gender, and age group
- Track salary trends and compensation equity across roles and demographics
- Monitor gender diversity and inclusion metrics

### 📈 Key HR KPIs
- Employee Count & Headcount Trends
- Average Salary, Monthly Payroll & Salary Hikes
- Average Age & Tenure Metrics
- Job Satisfaction Scores
- Gender Ratio & Diversity Metrics

### 🔍 Employee Attrition Analysis
- Identify attrition rates by department, job role, and demographics
- Analyze impact of factors like:
  - Work-life balance & job satisfaction
  - Business travel frequency
  - Monthly income & salary levels
  - Marital status & age groups
- Compare attrition patterns across Sales, R&D, and HR departments
- Support data-driven retention strategy development

---

## 🗂️ Data Sources

| File | Description |
|------|-------------|
| `Employeesx.xlsx` | Core employee demographic and employment data |
| `HR-Employee-Attritionx.xlsx` | Employee attrition records with reasons and contextual factors |
| `oracle_hr_schema_extendedx.xlsx` | Extended HR schema reference data (departments, jobs, locations) |
| `HRByShireen.pbix` | **Main Power BI report file** with data model, DAX measures, and visualizations |

---

## 📊 Dashboard Features

### 🎛️ Interactive Filters (Slicers)
- Department | Education Field | Business Travel Frequency
- Gender | Job Role | Age Group | Marital Status

### 📈 Key Visualizations

#### 🏠 Overview Page
- **KPI Cards**: Employee Count, Avg. Salary, Avg. Age, Gender Ratio, Job Satisfaction
- Employee Distribution by Department & Education Field
- Salary Trends by Age Group & Job Role
- Headcount Trends Over Time

#### 📉 Attrition Analysis Page
- Attrition Rate Gauge Charts by Department
- Attrition Drivers: Job Satisfaction, Work-Life Balance, Monthly Income
- Attrition by Business Travel Frequency & Age
- Comparative Attrition: Job Roles & Demographics

#### 🔎 Drill-Through Capability
- Click any visual to explore employee-level details
- Filter context preserved across pages for seamless exploration

---

## ⚙️ Technical Implementation

### 🛠️ Tools Used
- **Power BI Desktop** – Report development & data modeling
- **Power Query (M)** – Data extraction, cleaning, and transformation
- **DAX (Data Analysis Expressions)** – Custom metrics and calculated columns
- **Excel** – Source data preparation

### 🗄️ Data Modeling
- Star schema design with fact and dimension tables
- Relationships established between employee, attrition, and reference tables
- Optimized for performance with appropriate cardinality settings

### 💻 Key DAX Measures (Examples)

```dax
// Attrition Rate
Attrition Rate = 
DIVIDE(
    CALCULATE(COUNTROWS(Employees), Employees[Attrition] = "Yes"),
    COUNTROWS(Employees),
    0
)

// Average Salary by Department
Avg Salary by Dept = 
AVERAGE(Employees[MonthlyIncome])

// Gender Ratio (% Female)
Gender Ratio = 
DIVIDE(
    CALCULATE(COUNTROWS(Employees), Employees[Gender] = "Female"),
    COUNTROWS(Employees),
    0
) * 100

// Active Employee Count
Active Employees = 
CALCULATE(
    COUNTROWS(Employees),
    Employees[Attrition] = "No"
)

