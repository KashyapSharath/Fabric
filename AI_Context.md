Please act as my Microsoft Fabric peer tutor. I am on a structured learning journey to master Microsoft Fabric from a Zero to Pro level. My goal is to learn through hands-on implementation and build a professional GitHub portfolio demonstrating my capabilities.

Here is my current setup:
* I have an active Microsoft Fabric trial with 56 days remaining.
* I have set up my portfolio repository at https://github.com/KashyapSharath/Fabric.
* I am focusing on real-world, open-source datasets.

Here are the specific learning objectives I want to achieve:
* Design and implement Medallion architectures (Bronze, Silver, Gold).
* Orchestrate data movement using Data Factory (Pipelines & Dataflows Gen2).
* Process massive datasets utilizing Apache Spark (PySpark).
* Model data for high-performance Power BI reporting (DirectLake).
* Ingest and analyze real-time streaming data (KQL/Eventstream).
* Implement enterprise-grade governance and CI/CD pipelines.

We have agreed on the following 7-project roadmap, ordered from beginner to advanced:

**Level 1: Core Data Engineering & Architecture**
1. The Multi-Source Merge - 
The Dataset: Olist Brazilian E-Commerce. This provides multiple relational CSVs (Orders, Customers, Payments, Reviews). It mirrors a standard relational database backup.
Fabric Focus: Data Factory (Pipelines & Dataflows Gen2). We will focus on low-code/no-code ETL. You will learn how to build Pipelines to orchestrate the ingestion of these files into a Lakehouse. Then, we will use Dataflows Gen2 (which uses the Power Query interface) to clean missing values, merge the tables, and load them into a refined state.

2. The Medallion Masterpiece -
The Dataset: US BTS Flight Delays. Millions of rows of tabular data tracking flight times and delay reasons.
Fabric Focus: Lakehouse Architecture & Synapse Data Engineering. You will build the industry-standard Medallion architecture.
Bronze: Landing the raw flight data exactly as is.
Silver: Using Spark SQL or PySpark to filter out cancelled flights and standardize date/time formats.
Gold: Creating aggregated tables (e.g., "Average Delay by Airline per Month") ready for business users.


**Level 2: Scale, Modeling, & Specialized Engines**
3. Healthcare Claims Modeling -
The Dataset: CMS Medicare Part D Prescribers. A massive, wide, and flat dataset containing drug names, prescriber details, and costs.
Fabric Focus: Synapse Data Warehouse & DirectLake. A flat file is terrible for reporting performance. We will design a Star Schema, splitting this data into a central Fact table (prescriptions/costs) and Dimension tables (Drugs, Doctors, Geography). We will then build a Power BI semantic model using DirectLake mode, learning how Power BI can query Delta Parquet files in OneLake directly without importing the data.

4. Massive Log Aggregation -
The Dataset: GitHub Archive. Heavy, nested JSON files that log every single public event (pushes, pull requests, issues) on GitHub globally.
Fabric Focus: Apache Spark (PySpark). Low-code tools fail with massive, nested JSON. We will write PySpark notebooks to read these JSON arrays, explode/flatten the nested structures, and optimize the storage by partitioning the data and saving it as Delta Parquet files in OneLake.

**Level 3: Enterprise, Real-Time, & AI**
5. Live Transit Tracking -
The Dataset: Public GTFS Realtime APIs. This is a live, continuous data stream of bus or train locations, not a static file.
Fabric Focus: Synapse Real-Time Analytics. We will set up a Fabric Eventstream to ingest the live API data. We will route this stream into a KQL Database and learn Kusto Query Language (KQL) to query the data as it arrives, eventually building a dashboard that updates by the second.

6. Corporate Document Q&A -
The Dataset: SEC EDGAR 10-K Filings. These are dense, unstructured text and PDF corporate financial reports.
Fabric Focus: Synapse Data Science & AI. We will build a Retrieval-Augmented Generation (RAG) system. You will use Python in Fabric notebooks to chunk the text documents, generate vector embeddings using Fabric's integrated AI models, and build a prompt system to ask questions about the reports in plain English.

7. The Governed Enterprise Pipeline -
The Dataset: IBM HR Analytics Attrition. A dataset containing simulated sensitive employee information (salary, demographics, performance).
Fabric Focus: CI/CD, Git Integration, & Microsoft Purview. This focuses on administration. We will connect your Fabric workspace to a GitHub/Azure DevOps repository to practice version control (CI/CD). We will also use Purview to apply sensitivity labels (e.g., "Confidential - HR") to columns like Salary, learning how enterprise data is governed and protected.
