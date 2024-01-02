# MLOps with Amazon Reviews Data

## Data Ingestion

### Copy Data from Public S3 to Private S3

```
aws s3 mb s3://ds-learning-aws
aws s3 cp --recursive s3://dsoaws/amazon-reviews-pds/tsv s3://ds-learning-aws/amazon-reviews-pds/tsv/ --exclude "*" --include "amazon_reviews_us_*"
```

### Querying with Amazon Athena.

- Create Database ```CREATE DATABASE dsoaws;```
- Create Table
```
CREATE EXTERNAL TABLE IF NOT EXISTS dsoaws.amazon_reviews_tsv(
marketplace string, 
customer_id string, 
review_id string, 
product_id string, 
product_parent string, 
product_title string, 
product_category string, 
star_rating int, 
helpful_votes int, 
total_votes int, 
vine string, 
verified_purchase string, 
review_headline string, 
review_body string, 
review_date string
) ROW FORMAT DELIMITED FIELDS TERMINATED BY '\t'
LINES TERMINATED BY '\n'
LOCATION 's3://ds-learning-aws/amazon-reviews-pds/tsv'
TBLPROPERTIES ('compressionType'='gzip', 'skip.header.line.count'='1');
```
- Query Table to check
```
SELECT *
FROM dsoaws.amazon_reviews_tsv
WHERE product_category = 'Digital_Video_Download' LIMIT 10;
```
- Create a Parquet-based table in Athena.
```
CREATE TABLE IF NOT EXISTS dsoaws.amazon_reviews_parquet
WITH (format = 'PARQUET', external_location = 's3://ds-learning-aws/amazon-reviews-pds/parquet', partitioned_by = ARRAY['product_category']) AS
SELECT marketplace,
         customer_id,
         review_id,
         product_id,
         product_parent,
         product_title,
         star_rating,
         helpful_votes,
         total_votes,
         vine,
         verified_purchase,
         review_headline,
         review_body,
         CAST(YEAR(DATE(review_date)) AS INTEGER) AS year,
         DATE(review_date) AS review_date,
         product_category
FROM dsoaws.amazon_reviews_tsv
```
- Load Parquet Partitions
```
MSCK REPAIR TABLE amazon_reviews_parquet
```