# Projects


# Project 1 - Graffiti Analysis of Vancouver City Areas

## Project Description:
Performe a descriptive data analysis on the Vancouver Graffiti dataset using AWS services to ingest and analyze data efficiently, uncovering the number of graffiti incidents in the Sunset and Renfrew-Collingwood areas.

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

<img width="1713" alt="image" src="https://github.com/user-attachments/assets/0762610a-52d2-4d9f-b84e-5fe16842dcd6">

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

<img width="1701" alt="image" src="https://github.com/user-attachments/assets/e09c2d83-78cb-4d5e-9ce5-3a6cf4c73d13">

### 4. Descriptive Analysis:
- **Neighborhood Breakdown**:
  - Analyzed graffiti reports across different neighborhoods in Vancouver to identify areas with high incident rates.
  - Use SQL queries in Athena to break down data by categories.
- **Trend Analysis**:
  - Explore the trends of graffiti in different areas.
  - Generate monthly and quarterly aggregates using SQL queries in Athena.

### 5. Insights and Findings:
- **Neighborhood Insights**: Summarize key findings such as which neighborhoods experience the most graffiti and potential reasons behind the trends.
- **Property Type Impact**: Explore which areas the graffiti could impact the properties.
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


# Project 2 - Building an AWS Data Analytics Platform for the City of Vancouver

## Project Description:
Designing a data analytics platform for the City of Vancouver that uses AWS services, focused on allowing the ingestion, processing, replicating and analysis of various public datasets to generate actionable insights. This platform will allow handling datasets related to various city services, such as transportation, public safety, environmental data, and infrastructure.

## Objective:
The goal of this project is to implement a scalable AWS-based platform that can ingest, store, process, and analyze large datasets from various city departments. AWS services such as S3 (data storage), Glue (ETL), Athena (SQL querying), KMS, and CloudWatch (data visualization) will be utilized for this platform.

## Datasets:
The platform was ingested with the Vancouver's graffiti dataset described in Project 1.

## Methodology:

### 1. Data Ingestion:
- **Data Storage**: AWS S3 was used as the centralized repository for storing the dataset. Data can be uploaded manually or through automated pipelines from city data portals.
- **Data Processing**:
  - AWS Glue was used for ETL (Extract, Transform, Load) processes, where raw datasets are transformed, cleaned, and cataloged.
  - The Glue Data Catalog will keep metadata and ensure all datasets are properly indexed for future querying.
- **Encryption Management**: KMS (Key Management Service) was used to create and manage keys that encrypted S3 data.
- **Data Querying**: Use AWS Athena to query datasets directly from S3 using SQL. This will enable analysts to explore the datasets efficiently without having to transfer data.

### 2. Descriptive Statistics:
- **Summary Statistics**:
  - Use Athena to run SQL queries that provide summary statistics for the various datasets, such as:
    - Average daily public transit ridership.
    - Monthly traffic flow counts at key intersections.
    - Average emergency response time by neighborhood.
  - Generate frequency distributions for categorical features, such as transit mode or crime type.
- **Key Questions**:
  - What are the busiest transit routes and times of day for public transport?
  - Which neighborhoods report the most public safety incidents?
  - How does air quality vary across different seasons and areas?

### 3. Data Visualization:
- Use AWS QuickSight or local Python libraries (Matplotlib, Seaborn) to create visualizations based on insights from the data.
  - **Line Charts**: To show trends in daily or monthly ridership and traffic flows.
  - **Bar Charts**: To visualize public safety incidents by neighborhood or type.
  - **Heatmaps**: To display correlations between air quality and traffic volume.
  - **Pie Charts**: To visualize the distribution of public transport types (e.g., Bus, SkyTrain).
  
### 4. Insights and Findings:
- **Data protection**: It was possible to create users with AWS IAM (Identity Access Management) to control the resources access to all data for Vancouver city data platform.
- **Data Governance**: AWS Glue was used to detect sensitive data and evaluate data quality, utilising its built-in capabilities according to Canada's laws.
- **Replication**: S3 data was replicated to lower tier storages as they age to reduce costs.

<img width="1769" alt="image" src="https://github.com/user-attachments/assets/8a8bc219-0dcd-425e-bc48-c00907976fcf">
<img width="1756" alt="image" src="https://github.com/user-attachments/assets/c2315eae-e565-4f71-a146-200d7914456f">
<img width="1757" alt="image" src="https://github.com/user-attachments/assets/e1b5e17d-fdac-4461-a4c5-58823653d224">

## Tools and Technologies:
- **AWS S3**: For scalable and secure data storage.
- **AWS Glue**: For ETL (Extract, Transform, Load) operations and building the data catalog.
- **AWS Athena**: For running SQL queries to explore and analyze datasets directly from S3.
- **AWS CloudWatch**: For usage visualisation and alerting via SNS.
- **AWS SNS**: For alerting if services outgrow its usage limits.
- **AWS IAM**: user management for the platform data access.

## Deliverables:
- A fully implemented AWS data analytics platform capable of ingesting, processing, and analyzing datasets from multiple city services.
  - The platform includes a clear data ingestion process using S3.
  - Automated data transformation using AWS Glue.
  - SQL queries in Athena to explore datasets and generate descriptive statistics.
  - Visual dashboards in CloudWatch for stakeholders to monitor key platform metrics.

## Benefits to the City of Vancouver:
- **Real-Time Insights**: The platform will provide real-time access to data from multiple services, enabling city departments to make data-driven decisions.
- **Scalability**: AWS’s infrastructure allows the platform to scale as new datasets and services are added.
- **Cost-Effectiveness**: By leveraging serverless tools like Athena and Glue, the city can process large amounts of data without needing extensive hardware infrastructure.


