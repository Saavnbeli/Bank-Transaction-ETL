# Bank-Transaction-ETL

## Optimizing Customer Satisfaction: A Deep Dive into Spar Nord Bank ATM Transactions

## Project Overview

This project aims to optimize ATM usage patterns and management for Spar Nord Bank by analyzing ATM transaction data. By leveraging various AWS services, we constructed a batch ETL pipeline to extract, transform, and load transactional data for in-depth analysis. This analysis helps in uncovering patterns and trends in customer behavior, leading to enhanced operations, improved security, and optimized customer service.

## Project Goals and Objectives

- **Enhance Customer Experience:** By understanding customer behavior and optimizing ATM placements, network design, and cash management.
- **Increase Security:** Detect fraudulent activities and propose measures to mitigate risks.
- **Resource Utilization:** Efficiently manage ATM operations to reduce costs and improve service availability.

## Technologies Used

- **AWS S3:** Data lake for storing raw transactional data.
- **AWS Glue:** Fully managed ETL service for extracting, transforming, and loading data.
- **Amazon Redshift:** Data warehousing solution for performing data analytics.
- **PySpark:** Data preprocessing, cleaning, and transformation.
- **Tableau:** Data visualization tool for presenting insights and patterns.

## Data Overview

The dataset consists of over 2.5 million records of ATM transactions conducted by customers of Spar Nord Bank, obtained from Kaggle. Each transaction includes details such as date, time, amount, location, transaction type, and more.

### Data Cleaning and Preparation

1. **Schema Definition:** Specified column names, data types, and null value allowance.
2. **Data Merging:** Combined two CSV files into a single dataframe.
3. **Data Validation:** Checked for missing values, duplicates, and inconsistencies.
4. **Feature Engineering:** Created derived attributes such as 'full_date_time' for timestamp formatting.

## Architecture and Project Flow

1. **Extract Data:**
   - Utilized **Sqoop** to extract transactional data from RDS into PySpark.
   - Initial data cleaning and preprocessing performed in PySpark.
   
2. **Transform Data:**
   - Stored cleaned data in an S3 bucket.
   - Used AWS Glue to perform ETL operations, transforming data for analysis.
   
3. **Load Data:**
   - Loaded transformed data into Amazon Redshift.
   - Performed analytical queries using Redshift Query Editor.

4. **Data Visualization:**
   - Created visualizations in Tableau to present insights on customer behavior and ATM usage patterns.
   - Hosted the Tableau dashboard on a web application for easy access.

## Data Analytics and Insights

- **Inactive ATMs:** Identified top 10 ATMs with the highest percentage of inactive transactions.
- **Weather Impact:** Analyzed the correlation between weather conditions and ATM failures.
- **Usage Patterns:** Determined peak usage hours and optimal times for ATM maintenance and refilling.
- **Card Usage:** Analyzed the types of cards used and their transaction volumes.

## Conclusion and Future Work

### Conclusion

Our analysis provided valuable insights into optimizing the ATM network for Spar Nord Bank. By identifying peak usage times, popular card types, and the impact of weather conditions, we offered recommendations for improving customer satisfaction and operational efficiency.

### Future Work

- **Feature Analysis:** Investigate the impact of ATM features such as deposit capabilities, language options, and accessibility.
- **Demographic Study:** Incorporate demographic data to better understand customer preferences and tailor ATM services accordingly.
