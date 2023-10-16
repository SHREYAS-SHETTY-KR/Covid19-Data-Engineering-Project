# Covid19-Data-Engineering-Project
## Project Overview

Welcome to the COVID-19 Data Engineering Project, an ambitious initiative designed to apply advanced data engineering principles and a suite of AWS tools to develop a comprehensive data engineering solution for the analysis of COVID-19 data.

At its core, this project follows the Extract, Transform, Load (ETL) approach, enabling users to seamlessly extract, load, and transform data, ultimately unlocking valuable insights. Our primary mission is to create an accessible and efficient data engineering project tailored for the analysis of COVID-19 data.

## Architecture
![Example Image](https://github.com/Shreyas-028/Covid19-Data-Engineering-Project/blob/main/Images/Data_Pipeline_Architecture.drawio.png)

## Important Prerequisites
To ensure the successful launch of your COVID-19 Data Engineering Project, there are several key prerequisites that need to be in place:

1.**IAM Role "s3-glue-role"** : This pivotal role is designed to empower AWS Glue with the permissions necessary to initiate AWS service calls on your behalf, ensuring a smooth data engineering process.

2. **Redshift Cluster Setup and VPC Security Configuration** : The setup of your Redshift cluster is the foundation of your project. Additionally, it's imperative to fine-tune the VPC security group by adding a new rule to allow inbound access from your IP address, creating a secure gateway for data.

3. **IAM Role "redshift_s3_access"** : This role is a linchpin in the project, as it grants Redshift the essential permissions required to access data stored in Amazon S3, fostering data integration and accessibility.

4. **Glue Environment Preparedness for Redshift Job** : Before you embark on creating a Glue job, make sure to download the essential external libraries, including the redshift-connector and boto3. Given that Glue has limited support for default libraries, bundle these libraries into a zip package and upload it to an S3 bucket. This will ensure your Glue environment is fully equipped for the job.

5. **Establish Python "redshift_connector" Connection to Redshift Cluster** : A successful project execution hinges on creating a robust Python 'redshift_connector' connection to your Redshift cluster, bridging the gap between your data and the cluster.

6. **VPC Endpoint Creation for Amazon S3** : The creation of a VPC endpoint for Amazon S3 is a pivotal step in establishing seamless connectivity between your Glue job's VPC and S3. This connection ensures uninterrupted and secure data transfer.

## Key steps

1. **Set Up the 'COVID-19 Data Lake on Amazon S3** : The project kicks off by putting the 'COVID-19 Data Lake' on Amazon S3, sourced from an Open Data Registry. This step lays the foundation for all data processing.
   
   Dataset - https://aws.amazon.com/blogs/big-data/a-public-data-lake-for-analysis-of-covid-19-data/

2. **Create Run Crawlers in Amazon Athena** : Following the initial data upload, the project takes a significant step by running crawlers within Amazon Athena. These smart crawlers carefully explore tables stored in Amazon S3 buckets. Their goal is to expertly extract organized data, making it easy for detailed analysis.
3. **Python-Powered Data Transformation** : The heart of the project is a Python-based ETL (Extract, Transform, Load) job. This critical job transforms the initial relational data model into an efficient dimensional data model using the STAR schema. It enhances data structure and accessibility, turning raw data into useful insights.
4. **Upload Transformed Data to Amazon S3** : After the ETL job is executed, the resulting DataFrame is converted into a CSV-formatted string representation. This transformed data is then uploaded back to an Amazon S3 bucket for storage and convenient access.
5. **Create, Configure VPC Networking, Connect, and Run ETL Job in AWS Glue** : In this step, we create and configure Virtual Private Cloud (VPC) networking. By establishing secure communication and connectivity, we can seamlessly run the ETL job in AWS Glue to create tables in Amazon Redshift.

## Tools and Technologies - Powering Your Data Pipeline

In crafting an end-to-end data pipeline for this project, we employ a set of versatile and robust tools and technologies:

- **Python** : A versatile programming language, Python plays a pivotal role in data extraction, transformation, and loading. It's a cornerstone of our data processing.

- **SQL** : SQL (Structured Query Language) serves as the foundation for querying and manipulating data within databases. It allows us to harness the full potential of our data.

- **Amazon Athena** : Athena takes center stage in running queries on our data stored in Amazon S3. With its standard SQL syntax, it empowers us to analyze both structured and semi-structured data effectively.

- **AWS Glue** : AWS Glue is the workhorse of our project, serving as an ETL (Extract, Transform, Load) service provided by AWS. It forms the core of our data transformation operations, allowing us to create and execute ETL jobs that seamlessly convert data between various formats and store it in the desired destinations.

- **Amazon Redshift** : Amazon Redshift, a fully-managed data warehousing service offered by AWS, steps in as our storage and querying solution for large-scale data analysis. It provides the solid foundation for data storage and retrieval.

- **Amazon S3** : Amazon S3, known as Simple Storage Service, acts as the bedrock for storing both raw and transformed data. It guarantees high durability, availability, and scalability for our data.

- **IAM (Identity and Access Management)** : IAM is our guardian for managing user access and permissions across various AWS resources. It ensures that data handling remains secure and well-controlled.

## Data Model Transformation

We're transforming our data model from a relational structure to a dimensional one by constructing a STAR schema.

**Before Data Modeling**:

<img src="https://github.com/Shreyas-028/Covid19-Data-Engineering-Project/blob/main/Images/Data_Model.drawio.png" width="1200" height="1400">


**After Data Modeling**:

![Example Image](https://github.com/Shreyas-028/Covid19-Data-Engineering-Project/blob/main/Images/Data_Model_STAR_Schema.png)

This transformation enhances our data's accessibility, making it easier to analyze and derive valuable insights. The STAR schema simplifies data relationships, ensuring that our data becomes a powerful resource for analysis and decision-making.

## Unlocking Insights through Visualization Tools

In addition to the data transformation, we have the opportunity to visualize our data using various powerful tools, including Tableau, Power BI, Looker, Amazon QuickSight, and several other visualization solutions.

![Example Image](https://github.com/Shreyas-028/Covid19-Data-Engineering-Project/blob/main/Images/COVID19_Viz.png)

These visualization tools provide the means to explore, analyze, and present data in visually informative formats. By leveraging these tools, we can enhance our project's capabilities and enable stakeholders to gain deeper insights from the data we've curated and transformed.

## Conclusion
The COVID-19 Data Engineering Project is a testament to the power of data engineering in transforming raw information into actionable insights. By leveraging a range of tools and technologies, we've created a robust data pipeline, simplified data relationships, and explored data visualization. This project not only showcases technical prowess but also underscores the impact data engineering can have in addressing real-world challenges. As we conclude, we recognize that data engineering is an ongoing journey of discovery and innovation, and we hope this project inspires others to harness the potential of data for positive change.



