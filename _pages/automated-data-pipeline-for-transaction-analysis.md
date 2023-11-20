---
permalink: /projects/automated-data-pipeline-for-transaction-analysis
title: "Automated Data Pipeline for Transaction Analysis"
author_profile: true
---

**Supervisor:** N/A  
**Type:** Personal Project (Data Engineering, Batch Data Processing)

## Overview
This project was designed to create an automated data pipeline for analyzing transaction data. The project involved setting up a pipeline using multiple cloud services and tools to process and analyze data efficiently.

## Methodology
The project implementation included the following steps:
1. **Data Collection and Storage:** Utilizing Snowflake to simulate a transaction database, data was collected and stored in an S3 bucket.
2. **Data Processing with EMR:** Employing AWS EMR to process the data using PySpark scripts.
3. **Workflow Automation with Airflow:** Setting up Apache Airflow on an EC2 instance to automate the workflow of the data pipeline.
4. **Lambda Functions and Cloudwatch:** Utilizing AWS Lambda functions, triggered by Cloudwatch, to check for new data and initiate the pipeline.
5. **Data Visualization with Metabase:** Implementing Metabase for data visualization and analysis.

## Evaluation
The project's success was evaluated based on:
- **Data Processing Efficiency:** How effectively EMR processed the data.
- **Workflow Automation:** The efficiency and reliability of Airflow in managing the pipeline.
- **Visualization and Insights:** The quality and depth of insights gained from the data through Metabase visualizations.

## Key Findings
- Demonstrated the capability to handle large datasets efficiently using cloud-based services.
- Effective automation of the data pipeline, reducing manual intervention and errors.
- Provided valuable insights through data visualization, aiding in better decision-making.

## Personal Contributions
- **Pipeline Design and Implementation:** Led the design and development of the entire data pipeline.
- **Cloud Services Integration:** Integrated multiple AWS services like S3, Lambda, EMR, and Airflow.
- **Data Processing and Analysis:** Wrote and optimized PySpark scripts for data processing and performed data analysis.
- **Visualization Setup:** Configured and utilized Metabase for visualizing the processed data.

## Conclusion
This project successfully demonstrated the use of cloud technologies and big data tools in creating an efficient and automated pipeline for transaction data analysis. It highlighted the power of cloud computing in handling and analyzing large datasets and provided a template for future data engineering projects.
