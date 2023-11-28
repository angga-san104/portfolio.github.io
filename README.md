# About the Project

_This project is about how to analyze and predict various stocks from the IDX (Indonesia Stock Exchange) use GCP (Google Cloud Platform). Four primary step is focusing on are as follows :_
- Downloading data for preparation 
- Ingesting and load data to BigQuery using python
- Analytic data stock on BigQuery 
- Make prediction model using Vertex AI

# Project overview

## Downloading data stock

Explore how to obtain stock data from the Yahoo Finance API using python. Yahoo Finance provides a wealth of information on a wide range of stocks, making it a valuable resource for our analysis and predictions. On this section we will demonstrate how to access this data programmatically, ensuring we have the most up-to-date information. With Yahoo Finance library for Python, we can conveniently retrieve data for the specific stocks we are interested in and prepare it for further processing.

## Ingesting data using python

After successfully downloading data using python we will explore how to use Python to ingest the downloaded data. On this section we will do Ingesting data transforming it into a suitable format, and organizing it for efficient storage. Python provides a wide array of libraries and tools that make this process smooth and efficient. By the end of this section, this project will have a clean and well-organized dataset ready for analysis, and you'll be well-prepared for the subsequent stages of this project.

## Analytic data using BigQuery 

With dataset successfully ingested and structured time to uncover meaningfull pattern and discovered some insight, analytic is using BigQuery to run complex queries, generate reports, and visualize data. We'll explore SQL-based analysis and how to leverage BigQuery speed and scalability to handle large datasets. By the end of this section, project well-equipped to extract valuable insights from your dataset.

## Prediction using Vertex AI 

On this section we will doing data preprocessing and model selection to build an accurate prediction model. Vertex AI's robust machine learning capabilities will help you harness the power of deep learning and traditional machine learning algorithms to make predictions with confidence.

***What are We Use***

_On this project we use GCP (Google Cloud Platform) as cloud storage, computing, and data analytic. VS Code (Visual Studio Code) for source code editor._

## What is GCP (Google Cloud Platform)

GCP is a public cloud vendor that offers a suite of computing services to do everything from data management to delivering web and video over the web to AI and machine learning tools. 
Why we choose GCP for CI/CD this project. First, we've utilized GCP's versatile and high-performing storage solutions for efficient data storage, ensuring that we can securely manage the vast amount of stock market data we acquire. BigQuery, one of GCP's data warehousing services, is pivotal in our project as it allows us to perform advanced analytics and queries on massive datasets, all in real-time.

![Alt text](image.png)

Not all of service on GCP are used for this project, only some service where suitable for build this project, what service GCP are we used to build this project are follow as:
- Bigquery
- Cloud Function
- Cloud Schedular
- Vertex AI

Then what is service GCP above for ?  here is with explanation

## BigQuery

BigQuery is Google Cloud's fully managed data warehouse that enables super-fast SQL queries and interactive analysis of large datasets. It's used for storing, querying, and analyzing vast amounts of data quickly. With its serverless architecture, BigQuery is particularly well-suited for business intelligence, data analytics, and machine learning tasks.
At this project BigQuery was used for storing data stock and doing analytical using sql queryng, after ingesting data from API yahoo finance to dataset on BigQuery, we are doing analytic use sql queries and schedule it at spesific time.

## Cloud Function

Cloud Functions is an event-driven serverless compute platform. Cloud Functions allows you to write your code without worrying about provisioning resources or scaling to handle changing requirements.
In this project, we leverage Cloud Functions to efficiently gather financial data from Yahoo Finance through Python's API. The serverless nature of Cloud Functions makes it the perfect choice for running event-triggered tasks like web scraping. Our Python script accesses Yahoo Finance's API to collect real-time data, which is then transformed and seamlessly ingested into BigQuery. With BigQuery's powerful data warehousing capabilities, we ensure that the acquired financial information is stored securely and made readily available for analysis. This integrated approach spans web scraping, data ingestion, and cloud-based data warehousing, laying the foundation for data-driven insights and comprehensive analytics.

## Cloud Schedular

Cloud Scheduler is a fully managed enterprise-grade cron job scheduler. It allows you to schedule virtually any job, including batch, big data jobs, cloud infrastructure operations, and more.
One of cloud schedular function are used on this project is for schedule at some spesific time for run some function on cloud function.

***Downloading data from API***
Downloading data from API Yahoo Finance use python library yfinance
