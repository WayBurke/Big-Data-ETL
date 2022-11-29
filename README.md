# BIG DATA - Amazon Reviews

## Background
Amazon shoppers, including myself, rely on product reviews before making a purchase from the online retailer. Amazon collective datasets on reviews are quite large and can exceed the capacity of local machines. Using knowledge of big data, this project will work with Amazon dataset in the cloud. The ETL (Extract, Transform and Load) process will be done in the cloud and the dataframe will be uploaded to an RDS instance using PgAdmin/postgres.

The following two Amazon Review Datasets were selected from [Amazon Reviews Dataset](https://s3.amazonaws.com/amazon-reviews-pds/tsv/index.txt):
* Digital Video Download Reviews
* Home Improvement Reviews
  
## Steps Taken to accomplish assignment
1. Extract
   1. Read in each dataset
   2. Get the number of rows in the dataset
   
2. Tranform
   1. Create tables in pgAdmin for each table, using the schema.sql file provided with the assignment
   2. From the Dataset, created the following dataframe for each of the table in the schema
        * review_id_df with the appropriate columns and data types, as per the schema.
        * products_df  that drops the duplicates in the "product_id" and "product_title columns.
        * customers_df that groups the data on the "customer_id" by the number of times a customer reviewed a product.
        * vine_df with "review_id", "star_rating", "helpful_votes", "total_votes", and "vine" columns.
   
3. Load
    * Exported each DataFrame into the RDS instance to create four tables for each dataset.


