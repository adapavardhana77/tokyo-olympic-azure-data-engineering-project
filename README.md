# tokyo-olympic-azure-data-engineering-project

🏅 Tokyo Olympic Azure Data Engineering Project
📘 Project Overview

This project demonstrates an end-to-end Azure Data Engineering pipeline built using the Tokyo Olympic dataset.
The goal is to extract, transform, and analyze Olympic data to gain insights such as Medal counts by Country, Athlete performance, and Team participation.

1. Data Source

Raw CSV files containing Olympic data (Athletes, Coaches, Teams, Medals, etc.) are stored in Azure Blob Storage.

These files represent the raw data layer in the data lake.

2. Data Integration (Ingestion Layer)

Azure Data Factory (ADF) is used to orchestrate data movement from Blob Storage.

Pipelines and Copy Data activities are created to move data into the Raw Zone of the Data Lake.

This ensures that all source data is available in Azure for further transformation.

3. Data Transformation

Azure Databricks is used for data cleaning, preprocessing, and transformation.

Removes duplicates, handles missing values, and merges multiple datasets.

Converts raw data into structured and analysis-ready format.

The transformed data is stored back in Azure Data Lake (Clean Zone).

ADF Data Flows can also be used for light transformations such as type conversion or column renaming.

4. Data Storage (Analytical Layer)

The cleaned and transformed data is loaded into Azure Synapse Analytics.

Synapse provides a dedicated SQL pool for optimized query performance.

This acts as the central analytical data warehouse.

5. Data Analysis

Using SQL scripts in Synapse, analytical queries are performed to derive key insights such as:

Medal count by country

Top-performing athletes

Sports-wise participation and performance trends

6. Visualization (Dashboard Layer)

Power BI is connected to Synapse for visualization.

Interactive dashboards are created to visualize:

Medal count by country

Gender-based participation

Year-wise performance trends

Athlete and coach statistics

7. Monitoring & Automation

Pipelines are scheduled and monitored in Azure Data Factory.

Logs and alerts help ensure smooth data refresh and end-to-end automation.

This workflow clearly represents your image:

Blob Storage → ADF → Databricks → Synapse → Power BI

🧱 Tech Stack

Azure Data Factory

Azure Synapse Analytics

Azure Data Lake Gen2

Power BI

SQL

📂 Project Structure
tokyo-olympic-azure-data-engineering-project/
│
├── data/
│   ├── Athletes.csv
│   ├── Coaches.csv
│   ├── EntriesGender.csv
│   ├── Medals.csv
│   └── Teams.csv
│
└── README.md

📊 Key Insights

Total Medals by Country

Gender-wise Participation

Top Performing Teams

Coaches per Team

Athletes by Sport


