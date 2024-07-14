# Home_Sales
Challenge 22
## 1. Setup and Installation
- Installed Apache Spark and Java.
- Set environment variables for Spark and Java.
- Initialized a Spark session.
## 2. Read Data
- Read the home sales data from an AWS S3 bucket into a Spark DataFrame.
- Displayed the schema and first few rows to ensure data was loaded correctly.
## 3. Create Temporary View
- Created a temporary view of the DataFrame for SQL querying.
- Verified the creation of the temporary view by running a simple query.
## 4. Perform SQL Queries
- **Query 1**: Calculated the average price for a four-bedroom house sold per year, rounded to two decimal places.
- **Query 2**: Calculated the average price of a home for each year it was built, for homes with 3 bedrooms and 3 bathrooms, rounded to two decimal places.
- **Query 3**: Calculated the average price of a home for each year it was built, for homes with 3 bedrooms, 3 bathrooms, two floors, and at least 2,000 square feet, rounded to two decimal places.
- **Query 4**: Calculated the average price of a home per "view" rating, for homes with an average price greater than or equal to $350,000, rounded to two decimal places. Measured the runtime for this query.
## 5. Caching
- Cached the temporary table `home_sales`.
- Verified that the table was cached.
## 6. Run Cached Query
- Ran the same query from step 4 using the cached data.
- Measured the runtime and compared it to the uncached runtime.
## 7. Partition Data and Save as Parquet
- Partitioned the data by the `date_built` field and saved it as Parquet files.
## 8. Read Parquet Data
- Read the Parquet formatted data.
- Created a temporary table for the Parquet data.
## 9. Run Query on Parquet Data
- Ran the same query from step 4 using the Parquet data.
- Measured the runtime and compared it to the cached runtime.
## 10. Uncache Table
- Uncached the `home_sales` temporary table.
- Verified that the table was no longer cached.
## Conclusion
This project demonstrates how to efficiently perform data analysis using PySpark, including leveraging caching and data partitioning to optimize query performance.
