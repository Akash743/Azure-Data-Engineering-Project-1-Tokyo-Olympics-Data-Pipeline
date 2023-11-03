# Azure-data-engineering-project-tokyo-olympics

![Data Pipeline](https://github.com/Akash743/azure-data-engineering-project-tokyo-olympics/assets/57750483/dc6d4bcd-3311-4286-9ab7-7085fadf0d81)


In this poject, we will prepare Olympic data available for analysis and dashboarding using various Azure tools, including Azure Data Factory, Data Lake Gen 2, Synapse Analytics, and Azure Databricks

Pipeline is as follows:
**Data Source:** 5 files related to Olympics data(Athletes, Medals, Coaches, Participation) are present in **Github** repo in csv format. 

**Data Ingestion:** This step involves bringing the files from Github into the Azure system. Will use **Azure Lake Storage Gen 2** to store the Raw files.

**Data Transformation:** Will read data from Lake Storage and will perform transform operations using **Pyspark in Databricks**. After transforming, will store the transformed data into new directory in Lake Storage Gen 2.

**Querying the data:** Will use Azure **Synapse** to query the data stored in Lake Storage to get useful insights from the data. Can also use charts to visualize the data.

**Visualization**: We can use Azure Synapse for charting and visualization. Later, it can also be connected to Dashboarding tools like PowerBI and Tableau


**Azure Data Lake Storage Gen2 (ADLS)** is a cloud-based repository for both structured and unstructured data. For example, you could use it to store everything from documents to images to social media streams. Data Lake Storage Gen2 is built on top of Blob Storage. This gives you the best of both worlds

**Azure Data Factory** is a cloud-based data integration service that allows you to create data-driven workflows in the cloud for orchestrating and automating data movement and data transformation.ADF does not store any data itself. It allows you to create data-driven workflows to orchestrate the movement of data between supported data stores and then process the data using compute services in other regions or in an on-premise environment. It also allows you to monitor and manage workflows using both programmatic and UI mechanisms.

**Azure Databricks**: Simply put, Databricks is the implementation of Apache Spark on Azure. With fully managed Spark clusters, it is used to process large workloads of data and also helps in data engineering, data exploring and also visualizing data using Machine learning.

**Synapse Analytics**: Its a cloud based analytics service which combines big data and data wharehousing into a single integrated platform


**Steps** 

1. Create Storage Account. Create new Resource Group for this
2. Create Container in Storage Account to store data. Add directories here to store Raw Data and Transformed Data
3. Create Data Factory: To pull data from our source(Github). WHile creatig, attach it to the same Resource Group. Go to Author and create Pipeline for Data Ingestion. Use copy data option and use the csv file links from Github using HTTP data store option to create the pipeline. Copied data sink is the Raw data folder which we created in Step 2 and Linked Service would be the Storage account. On successfully running the pipeline, we would have data available in Raw Data directory in Storage.
4. Create Azure Databricks workspace: Attach same Resouce Group 


