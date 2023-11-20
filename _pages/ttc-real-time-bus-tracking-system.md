---
permalink: /projects/ttc-real-time-bus-tracking-system
title: "TTC Real-Time Bus Tracking System"
author_profile: true
---

**Supervisor:** N/A  
**Type:** Personal Project (Data Engineering, Real-time Data Processing)

## Overview
This project aimed to develop a real-time application for tracking buses using GPS data streamed by IoT devices. The project utilized a range of technologies including Apache NiFi, CDC(Debezium), Kafka (MSK), Spark Structural Streaming, Docker, and MySQL. The primary data source was the TTC bus data from the open API called Rest Bus.

## Methodology
The project methodology encompassed several key steps:
1. **Data Ingestion:** Leveraging Apache NiFi to extract GPS data from the bus API and store it in a MySQL database.
2. **Change Data Capture (CDC):** Implementing Debezium for CDC to capture new data from the MySQL database and send it to downstream processes.
3. **Data Streaming:** Using Kafka to handle streaming data and Spark Structural Streaming for data processing.

## Evaluation
The evaluation involved:
- **Functionality Testing:** Ensuring real-time data tracking and accuracy in GPS data representation.
- **Performance Assessment:** Evaluating the system's ability to handle continuous data streams effectively.

## Key Findings
- Successfully integrated various technologies to achieve real-time tracking of bus locations.
- Demonstrated effective use of CDC with Debezium for capturing and streaming live data updates.

## Personal Contributions
- **System Design and Implementation:** Took a leading role in designing the system architecture and implementing the solution.
- **Data Pipeline Construction:** Built and configured the data ingestion and processing pipelines using Apache NiFi and Kafka.
- **Database and Streaming Integration:** Integrated MySQL with Debezium for CDC and managed data flow through Kafka.

## Conclusion
This project effectively demonstrated the integration of various data engineering tools to create a real-time bus tracking system. It highlighted the potential of combining IoT data with modern data processing to enhance real-time operational capabilities in public transportation systems.
