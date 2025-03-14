# Spam Email Classification using PySpark and AWS

## Project Overview
This project aims to classify emails as spam or ham using PySpark and AWS cloud services. The dataset is acquired from Kaggle and contains essential email details such as sender, subject, and spam indicator. Various AWS services, including EMR, S3, and Cloud9, are utilized for data processing.

## Dataset
- **Source:** [Kaggle - Spam Email Dataset](https://www.kaggle.com/datasets/nanditapore/spam-email-dataset/code)
- **Size:** 6,000 rows and 16 columns
- **Key Columns:** Sender, Subject, Spam Indicator

## Installation and Setup
### **AWS EMR Cluster Setup**
1. Navigate to **AWS Management Console** and select **EMR** service.
2. Click on **Create Cluster** and provide a suitable cluster name.
3. Select required applications: **Hadoop, Pig, Hive, PySpark**.
4. Configure EC2 instances and specify an **EC2 key pair**.
5. Review the settings and click **Create Cluster**.
6. Update EC2 security group inbound rules to allow SSH access.

### **Uploading Dataset to Amazon S3**
1. Download the dataset from Kaggle.
2. Navigate to **AWS S3** and create a new bucket.
3. Provide a unique name and select a region.
4. Upload the dataset (`spam_email_dataset.csv`) to the bucket.

## Data Cleaning and Processing using PySpark
1. **Create a Cloud9 environment** and install PySpark (`pyspark`).
2. **Load dataset** from S3 using the S3 URI.
3. **Select necessary columns**: Sender, Subject, Spam Indicator.
4. **Tokenization**: Extract words from the subject column.
5. **Stopwords Removal**: Filter out common stopwords.
6. **Null Value Check**: Ensure no missing values in selected columns.

## Analyzing Spam and Ham Emails
1. Split the dataset into **spam and ham** categories using the Spam Indicator.
2. Extract **top 10 most frequently used words** in spam and ham emails.
3. Identify **top 10 spam and ham email accounts** based on word usage.

## TF-IDF Calculation using MapReduce
1. Extract **top 10 spam email senders and subjects**.
2. Tokenize subject lines into individual words.
3. Compute **Term Frequency (TF)** for each word.
4. Extract unique words from all emails.
5. Compute **Inverse Document Frequency (IDF)**.
6. Calculate **TF-IDF score** for each word.
7. Display **top 10 spam and ham email TF-IDF results**.

## Technologies Used
- **Cloud Services:** AWS S3, AWS EMR, AWS Cloud9
- **Big Data Processing:** Hadoop, PySpark, Hive, Pig
- **Programming Language:** Python
- **Libraries:** PySpark MLlib

## Results & Findings
- Identified the most commonly used words in spam and ham emails.
- Displayed the top 10 spam and ham email accounts.
- Computed TF-IDF scores to highlight significant words in email classification.

## Author
Sanjay Sathish Kumar

For inquiries, contact **sanjay.sathish0604@gmail.com**.

