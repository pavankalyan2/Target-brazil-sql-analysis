\# Day 1: BigQuery Environment Setup

This document details the setup of the BigQuery environment used for analyzing Target's operations in Brazil. It includes the steps for setting up a Google Cloud Project, configuring BigQuery, and preparing the workspace for data import and analysis.

\#\# 1\. Google Cloud Project Setup

To begin, we created a Google Cloud Project to host our BigQuery environment. The project is essential for organizing and managing resources such as datasets and tables.

\#\#\# Steps:  
1\. \*\*Create a Google Cloud Account\*\*: Sign up or log in at \[Google Cloud Console\](https://console.cloud.google.com/).  
2\. \*\*Create a New Project\*\*:  
   \- Navigate to the project selector in the top-left corner.  
   \- Click on "New Project" and provide a project name (e.g., \`target-brazil-analysis\`).  
   \- Note the project ID, which is unique and will be used to reference your project.

\#\# 2\. Enabling BigQuery API

BigQuery requires enabling the corresponding API within your Google Cloud Project to access its features.

\#\#\# Steps:  
1\. \*\*Enable BigQuery API\*\*:  
   \- Go to "APIs & Services" \> "Library".  
   \- Search for "BigQuery API" and click "Enable".

\#\# 3\. BigQuery Dataset and Table Setup

With BigQuery API enabled, we proceeded to create a dataset to store our data tables.

\#\#\# Steps:  
1\. \*\*Create a Dataset\*\*:  
   \- In the BigQuery console, click on your project name.  
   \- Click "Create Dataset" and provide a Dataset ID (e.g., \`target\_brazil\`).  
   \- Set the data location (e.g., \`us-central1\`) and other preferences as needed.

2\. \*\*Dataset Configuration\*\*:  
   \- Set default table expiration if desired, to automatically delete tables after a set period.  
   \- Configure data access controls by setting IAM permissions, ensuring only authorized users can access the data.

\#\# 4\. Google Cloud Storage (GCS) Setup

To facilitate data import, we set up a Google Cloud Storage (GCS) bucket to store raw data files.

\#\#\# Steps:  
1\. \*\*Create a GCS Bucket\*\*:  
   \- Navigate to "Storage" in the Google Cloud Console.  
   \- Click "Create Bucket" and name your bucket (e.g., \`target-brazil-data\`).  
   \- Ensure the bucket is in the same region as your BigQuery dataset for optimal performance.

2\. \*\*Upload Data to GCS\*\*:  
   \- Upload the CSV files or other data formats to the newly created bucket. These files will be imported into BigQuery for analysis.

\#\# 5\. Initial Data Import

We prepared for the initial data import by setting up the necessary permissions and ensuring the data formats are compatible with BigQuery.

\#\#\# Steps:  
1\. \*\*Set Up Permissions\*\*:  
   \- Ensure that the BigQuery service account has the necessary permissions to access the GCS bucket.  
   \- Adjust bucket permissions under "IAM & Admin" as needed.

2\. \*\*Data Import\*\*:  
   \- Use the BigQuery UI or CLI tools to load data from GCS into BigQuery tables.  
   \- For each CSV file, specify the schema manually or let BigQuery auto-detect the schema.

\#\# Conclusion

The setup of the BigQuery environment and GCS is a crucial first step in preparing for comprehensive data analysis. This setup ensures a secure and efficient workspace for storing and querying large datasets.

