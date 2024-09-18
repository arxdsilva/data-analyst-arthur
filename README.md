# Projects


# Project 1 - Graffiti Analysis of Vancouver City Areas

## Project Description:
Performing a descriptive data analysis on the Vancouver Graffiti dataset using AWS services to ingest and analyze data efficiently, uncovering the number of graffiti incidents in the Sunset and Renfrew-Collingwood areas.

## Understanding Graffiti in Vancouver: A Descriptive Analysis Using AWS

## Objective:
This project aimed to demonstrate how to ingest, process, and analyze Vancouver's graffiti dataset using AWS services. This analysis focuses on understanding the number of graffiti incidents across different areas. AWS services like S3 (Simple Storage Service), Glue (ETL), and Athena (SQL querying) were utilized to process and explore the dataset.

## Dataset:
The Vancouver Graffiti dataset contains information about graffiti incidents in Vancouver, including:
- **Count**: number of occurrences in a geo-location area.
- **Geo Local Area**: general area name of the occurrences.
- **Geom**: coordinates metadata of the area.
- **Geo_point_2d**: precise 2d coordinates of the area.

## Methodology:

### 1. Data Ingestion:
- **Data Storage**: Use AWS S3 to store the dataset securely. The data was uploaded manually.
- **Data Processing**: 
  - Used AWS Glue to create a data catalog and handle any data transformation tasks, such as correcting missing values, renaming columns, and standardizing formats.
  - Glue jobs will clean and prepare the dataset, making it ready for analysis.
- **Data Querying**: Use AWS Athena to query the data directly from S3 using SQL queries, enabling efficient exploration without needing to move the data elsewhere.

<glue image>

### 2. Descriptive Statistics:
- **Summary**:
  - Used Athena to run SQL queries that provide insights into the dataset.
- **Key Questions**:
  - How many graffiti are in Sunset and Renfrew-Collingwood?

### 3. Data Visualization:
- Trusted data after filtering from Glue processes was placed on a encrypted S3 bucket for later analysis with the following data:
  - **Area**: area that the graffiti is located in.
  - **Count**: Number of graffiti encountered in that area.
- Created a dashboard in Cloudwatch so cost can be visualised and managed by alerts with a SNS message alert.

### 4. Descriptive Analysis:
- **Neighborhood Breakdown**:
  - Analyzed graffiti reports across different neighborhoods in Vancouver to identify areas with high incident rates.
  - Use SQL queries in Athena to break down data by categories.
- **Trend Analysis**:
  - Explore the temporal trends in graffiti reporting, such as seasonal peaks.
  - Generate monthly and quarterly aggregates using SQL queries in Athena.

### 5. Insights and Findings:
- **Neighborhood Insights**: Summarize key findings such as which neighborhoods experience the most graffiti and potential reasons behind the trends.
- **Graffiti Type Patterns**: Highlight the most common types of graffiti (e.g., Tagging vs. Mural) and how they vary by location.
- **Property Type Impact**: Explore which property types (e.g., Commercial vs. Residential) are more frequently targeted and why.
- **Seasonality in Graffiti**: Identify any patterns of graffiti reporting over time, such as higher incidents during specific seasons or events.

## Tools and Technologies:
- **AWS S3**: For storing datasets securely and at scale.
- **AWS Glue**: For ETL (extract, transform, load) processes, data cleaning, and cataloging.
- **AWS Athena**: For querying data directly from S3 using SQL, enabling ad-hoc exploration and analysis.
- **AWS QuickSight**: For data visualization to present insights visually.
- **AWS SNS**: For alerting in case of a service going over the maximum spending limits.
- **AWS CloudWatch**: For systems visualisation and cost alerting.

## Deliverables:
- A documented analysis using AWS services that includes:
  - A clear process of data ingestion using S3.
  - Transformation and cleaning process using AWS Glue.
  - SQL queries used in Athena for descriptive statistics and data exploration.
- Visualizations summarizing key insights from the analysis.
- A final report or presentation showcasing descriptive analysis and insights derived from the graffiti dataset.
