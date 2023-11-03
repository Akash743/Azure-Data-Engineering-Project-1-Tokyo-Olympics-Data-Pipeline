# Azure-data-engineering-project-tokyo-olympics

![Data Pipeline](https://github.com/Akash743/azure-data-engineering-project-tokyo-olympics/assets/57750483/dc6d4bcd-3311-4286-9ab7-7085fadf0d81)


In this poject, we will prepare Olympic data available for analysis and dashboarding using various Azure tools, including Azure Data Factory, Data Lake Gen 2, Synapse Analytics, and Azure Databricks

Pipeline is as follows:
**Data Source:** 5 files related to Olympics data(Athletes, Medals, Coaches, Participation) are present in **Github** repo in csv format. 

**Data Ingestion:** This step involves bringing the files from Github into the Azure system. Will use **Azure Lake Storage Gen 2** to store the Raw files.

**Data Transformation:** Will read data from Lake Storage and will perform transform operations using **Pyspark in Databricks**. After transforming, will store the transformed data into new directory in Lake Storage Gen 2.

**Querying the data:** Will use Azure **Synapse** to query the data stored in Lake Storage to get useful insights from the data. Can also use charts to visualize the data.
Later it can also be connected to Dashboarding tools like PowerBI and Tableau
