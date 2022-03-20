# Amazon_Vine_Analysis
### Cheryl Berger
## Data Analytics Module 16 - Big Data

### Overview
This project analyzes customer reviews by members of the paid Amazon Vine program and determines if there is a bias toward favorable reviews from Vine members. The analysis uses PySpark to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, load the transformed data into pgAdmin for generate 4 seperate tables of the customer data.  We will use PySpark to calculate various metrics and determine if there is a bias toward favorable reviews for Vine members.  This analysis will focus on US reviews for shoes gathered from amazonaws.com.

### Resources
- Software: Google Colab Notebook, PostgreSQL 11.9, pgAdmin 4, AWS
- Data Source: https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Shoes_v1_00.tsv.gz

### Results

#### Deliverable 1

Perform a cloud based ETL on Amazon Product Reviews using AWS RDS database and upload the DataFrames into tables in PgAdmin.

https://github.com/cherylberger/Amazon_Vine_Analysis/blob/main/Amazon_Reviews_ELT.ipynb

 - Extract the Amazon Review dataset as a DataFrame
 
 ![image](https://user-images.githubusercontent.com/94234511/159126987-1bc8b808-dec7-40b5-ac9c-430e4fb74222.png)

 - Transform the extracted dataset into four seperate DataFrames.  The images of the DataFrame from Google Colab Notebook are shown below. 
 
 #### Review ID Table DataFrame
 ![image](https://user-images.githubusercontent.com/94234511/159149385-a7b7c21e-0bfd-4c7a-97c2-ec4be187bd55.png)

 #### Customers Table DataFrame
 ![image](https://user-images.githubusercontent.com/94234511/159149360-22d28ef1-5511-41f9-a523-9b1116dafafd.png)

 #### Products ID Table DataFrame
 ![image](https://user-images.githubusercontent.com/94234511/159149378-01527f60-d4a0-467f-beb7-a260737a2762.png)

 #### Vine Table DataFrame 
 ![image](https://user-images.githubusercontent.com/94234511/159149392-07790811-ce00-422f-84a8-495f6fb53427.png)

 - Load all four DataFrames into their respective tables in PgAdmn.  The schema.sql file was used to create the tables in the Postgres/AWS_Shoes_Database opened in PgAdmin.
 - https://github.com/cherylberger/Amazon_Vine_Analysis/blob/main/challenge_schema.sql

 - The images below reflect the output of the SQL query used to verify that the data was loaded into each table 

![image](https://user-images.githubusercontent.com/94234511/159149730-906ff874-5a78-4178-a5dc-1042be862184.png)

 #### Review ID Table 
 https://github.com/cherylberger/Amazon_Vine_Analysis/blob/main/Images/review%20id%20table.png
 
 #### Customers Table 
 https://github.com/cherylberger/Amazon_Vine_Analysis/blob/main/Images/customers%20table.png
 
 #### Products ID Table
 https://github.com/cherylberger/Amazon_Vine_Analysis/blob/main/Images/product%20id%20table.png
 
 #### Vine Table 
https://github.com/cherylberger/Amazon_Vine_Analysis/blob/main/Images/vine%20table.png


#### Deliverable 2

Using PySpark determine if there is any bias toward the reviews written as part of the Vine program. Discuss if having a paid Vine review makes a difference in the percentage of 5-star reviews.

https://github.com/cherylberger/Amazon_Vine_Analysis/blob/main/Vine_Review_Analysis.ipynb

![image](https://user-images.githubusercontent.com/94234511/159149796-5880d6fa-d373-463b-b3aa-7f8e2d4a9b63.png)

![image](https://user-images.githubusercontent.com/94234511/159148146-5d79c6b1-7846-4de4-a321-d87ba4db9641.png)
![image](https://user-images.githubusercontent.com/94234511/159148173-896e0dbc-f5c1-404f-9af1-960133b00774.png)
![image](https://user-images.githubusercontent.com/94234511/159148195-23f7879a-9a48-4ed7-b63e-8d9e8e98c5f1.png)

#### How many Vine reviews and Non-vine reviews were there? 
   - There were 22 Vine reviews and 26,987 Non-vine reviews.
 
#### How many Vine reviews were 5 stars?  How many Non-vine reviews were 5 stars?
   - There were 13 Vine reviews with 5 star ratings.  There were 14,475 Non-vine reviews with 5 star ratings. 

#### What percentage of Vine reviews were 5 stars?  What percentage of Non-vine reviews were 5 stars?
   - Of the total Vine reviews, 59.09% had 5 star ratings while the Non-vine reviews had slightly less, 53.64% 5 star rated reviews.

### Summary

- The results of the analysis show a slight positve bias for the paid reviews. The rate of 5 star reviews was about 5.5% higher for the Vine program participants. 

- The data set used was small as it was filtered on reviews that were deemed helpful by other users. The same metrics could be applied to the one of the other DataFrames to eliminate this bias.  

- It may be useful to determine the average star rating from the Vine and Non-vine reviewers to confirm the slight bias seen with the analysis of 5 star ratings only.  
