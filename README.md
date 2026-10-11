# Citi Bike Data Engineering Pipeline

## Project Overview
A PySpark-based data engineering pipeline that processes January 2020 Jersey City Citi Bike trip data. The project demonstrates data ingestion, data cleaning, data quality validation, Parquet storage, Amazon S3 integration, partitioning, and basic trip analytics.

## Technology Stack
- **Programming Language:** Python
- **Data Processing:** PySpark
- **Processing Engine:** Apache Spark
- **Cloud Storage:** Amazon S3
- **Storage Format:** Apache Parquet
- **Development Environment:** Google Colab

## Project Pipeline
1. Download the source CSV dataset.
2. Load the raw data into a Spark DataFrame.
3. Convert timestamps and calculate trip duration in minutes.
4. Filter trips outside the selected 1–240 minute range.
5. Create readable gender labels and remove records with missing essential station names.
6. Perform data quality validation.
7. Save cleaned data in Parquet format.
8. Upload raw CSV and processed Parquet files to Amazon S3.
9. Demonstrate partitioning by year and month.
10. Analyze trip activity, popular starting stations, user types, and gender categories.

## Business Analysis Questions
1. During which hours of the day are Citi Bike trips most frequent?
2. Which are the top 10 most popular starting stations?
3. What is the average trip duration for each user type?
4. How are trips distributed across gender categories?
5. Which hour has the highest number of trips?
6. Which starting station has the highest trip volume?
7. Which stations appear among the 10 most frequently used starting stations?
8. How does average trip duration vary by user type?
9. Which gender category accounts for the largest number of trips?
10. How does trip activity vary throughout the day?

## Results
- **Raw records:** 26,020
- **Cleaned records:** 25,997
- **Records removed:** 23
- **Cleaned columns:** 17
- **Duplicate rows detected:** 0
- **Invalid trip-duration records:** 0
- **Invalid timestamp records:** 0
- **Partition demonstrated:** Year 2020, Month 1

## Amazon S3 Storage
- **Raw data:** `s3://citi-bike-project-127463484766-us-east-1-an/Raw_data/`
- **Processed dataset:** `s3://citi-bike-project-127463484766-us-east-1-an/processed_data/citibike_jan_2020/`

## How to Run
1. Open the notebook `Citi-Bike-data-pipeline.ipynb` in Google Colab.
2. Run the notebook cells in order.
3. When prompted, provide valid AWS credentials with the required S3 permissions.
4. The notebook downloads the source dataset, processes it, validates the results, and uploads the raw and processed data to Amazon S3.

**Requirements:** A Google account, internet access, and an AWS account with appropriate S3 permissions.

## Project Structure
```text
citi-bike-data-engineering/
├── Citi-Bike-data-pipeline.ipynb
└── README.md
```

## Author
**Devesh Yadav**
