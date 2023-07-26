# Real-Estate-Aggregator
Connecticut Real Estate Sales

Absolutely, here's a summary and the step-by-step guide for your project:

**Project Summary:**  
The goal of your project is to perform an ETL process on real estate sales data from the state of Connecticut, which is available on data.gov. You'll extract the data, load it into an AWS-based data warehouse, and then visualize the data for analysis.

**Step-by-Step Guide:**

**Step 1: Download the Dataset**  
Navigate to the relevant page on data.gov and download the dataset for real estate sales in the state of Connecticut. The dataset will likely be in the form of a CSV file.

**Step 2: Set Up Your Development Environment**  
Ensure that Python and necessary libraries like pandas and boto3 (for AWS interactions) are installed in your development environment. You might also want a visualization library like Matplotlib or Seaborn.

**Step 3: Explore and Clean the Data**  
Load the CSV data into a pandas DataFrame and inspect it. You may need to clean the data by handling missing values, removing duplicates, changing data types, or performing other cleaning operations to ensure the data is ready for analysis.

**Step 4: Set Up Your AWS Account and S3 Bucket**  
If you haven't already, sign up for an AWS account. Create an S3 bucket where you'll upload your cleaned CSV file.

**Step 5: Upload Cleaned Data to S3**  
Using boto3 in your Python script, upload the cleaned CSV file from your local system to the S3 bucket.

**Step 6: Set Up AWS RDS Database Instance**  
Create a new database instance in AWS RDS. This will act as your data warehouse. Note down the details like endpoint, username, and password, as you'll need these to connect to the database.

**Step 7: Load Data into RDS**  
Using pandas, read the CSV file from the S3 bucket, then use the `to_sql` function to write the DataFrame into the database in your RDS instance. You'll need to use SQLAlchemy to create an engine for the database connection.

**Step 8: Verify Your Data**  
Check the database in your AWS RDS instance to ensure the data was loaded correctly. You can run SELECT queries to view the data and check if it matches what you expect.

**Step 9: Visualize the Data**  
Read the data from your RDS instance back into a pandas DataFrame. Then use Matplotlib or Seaborn to create plots that provide insights into the real estate sales data. You might create plots showing the number of sales over time, the distribution of sales prices, or any other analyses that you find interesting.

