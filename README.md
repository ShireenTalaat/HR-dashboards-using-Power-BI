# HR Analytics Power BI Dashboard

## Business Problem

Effective human resource management requires deep insights into workforce dynamics, employee performance, and factors influencing retention. Organizations often struggle with fragmented HR data, making it challenging to identify trends, predict attrition, and make data-driven decisions regarding talent management. This project addresses the need for a centralized, interactive analytics solution to transform raw HR data into actionable intelligence.

## Solution Overview

This Power BI project delivers a comprehensive HR analytics dashboard designed to provide HR professionals, managers, and decision-makers with a clear view of workforce composition, key HR metrics, and drivers of employee attrition. By integrating real-world HR datasets, the dashboard offers interactive visualizations and drill-through capabilities, enabling users to analyze employee distribution, track salary trends, monitor diversity, and identify critical factors impacting employee retention. The solution empowers organizations to develop proactive strategies for workforce optimization and talent management.

## Architecture

The HR Analytics Power BI Dashboard leverages a star schema data model to integrate various HR datasets. Data is extracted from Excel files, transformed using Power Query (M), and loaded into Power BI Desktop. DAX (Data Analysis Expressions) is utilized to create custom measures and calculated columns, enabling advanced analytics and interactive reporting. The dashboard is designed for intuitive navigation, allowing users to explore data from high-level KPIs down to granular employee details.

![HR Analytics Dashboard Architecture](hr_dashboard_architecture.png)

## Technologies Used

-   **Business Intelligence:** Power BI Desktop
-   **Data Transformation:** Power Query (M)
-   **Data Modeling & Analytics:** DAX (Data Analysis Expressions)
-   **Data Sources:** Microsoft Excel (.xlsx)

## Data Pipeline / Workflow

1.  **Data Extraction:** Raw HR data, including employee demographics, attrition records, and extended HR schema information, is extracted from Excel files.
2.  **Data Transformation (Power Query):** Power Query is used to clean, reshape, and transform the raw data. This involves handling missing values, correcting data types, and performing necessary aggregations to prepare the data for modeling.
3.  **Data Modeling (Power BI Desktop):** A star schema is implemented within Power BI, establishing relationships between fact tables (e.g., employee records) and dimension tables (e.g., department, job role). This optimized model supports efficient querying and analysis.
4.  **DAX Measures & Visualizations:** Custom DAX measures are created to calculate key HR KPIs (e.g., Attrition Rate, Average Salary, Gender Ratio). These measures drive interactive visualizations and dashboards.

## Key Features

-   **Interactive Dashboards:** Provides dynamic visualizations for workforce composition, HR KPIs, and attrition analysis.
-   **Comprehensive Metrics:** Tracks essential HR metrics such as employee count, average salary, tenure, job satisfaction, and gender diversity.
-   **Attrition Prediction & Analysis:** Identifies key drivers of employee attrition, enabling targeted retention strategies.
-   **Drill-Through Capabilities:** Allows users to delve into granular data details from high-level summaries.
-   **User-Friendly Interface:** Designed for intuitive navigation and ease of use by HR professionals and decision-makers.

## Results & Impact

This Power BI dashboard provides HR departments with a powerful tool for data-driven decision-making. It enables quick identification of critical HR trends, facilitates proactive talent management, and supports the development of effective retention strategies. By transforming complex HR data into clear, actionable insights, the project significantly enhances an organization's ability to optimize its human capital and improve overall business performance.

## Future Improvements

Future enhancements could include integrating additional data sources such as performance review data or training records to enrich the analysis. Implementing advanced analytics techniques, such as machine learning models for more accurate attrition prediction, could further enhance the dashboard's predictive capabilities. Exploring deployment options for the dashboard on Power BI Service would enable broader accessibility and collaboration within the organization.
