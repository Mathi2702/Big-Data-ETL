# Big-Data-ETL
Big Data ETL process and analysis using PySpark or SQL to perform a statistical analysis of selected data


  The dataset alone contains over 1.5 million rows. First, to perform the ETL process completely in the cloud and upload a DataFrame to an RDS instance
  using PySpark and hadoop.
  
  Tha data for amazon review is collected from S3 using "https://s3.amazonaws.com/amazon-reviews-pds/tsv/index.txt" descripition. 
  
  The selected datasets are for toys review and video games review.
  
  # ETL process in RDS instance
  
  ## Extract the Data

  Read in each dataset using the correct header and sep parameters.

  Get the number of rows in the dataset.

  ## Transform the Data
  
  Create a databse in the RDS instance and connect it to the pgadmin using the endpoint in the database created in the RDS instance.
  
  Two seperated file is added to the google colab to run the toys review data and video games review data
  
  To each file, create the four DataFrames as follows:

  Create the "review_id_df" DataFrame with the columns "review_id", "customer_id", "product_id", "product_parent".

  Create the "products_df" DataFrame that drops the duplicates in the "product_id" and "product_title columns.

  Create the "customers_df" DataFrame that groups the data on the "customer_id" by the number of times a customer reviewed a product.

  Create the "vine_df" DataFrame that has the "review_id", "star_rating", "helpful_votes", "total_votes", and "vine" columns.

 ## Load the Data into an RDS Instance
 
  Create a two new database for the different database
  
  using the schema.sql create the required table in the databases created seperately for the toys review and video games review

  Export each DataFrame into the RDS instance to create four tables for each dataset using google colab.
  
  
