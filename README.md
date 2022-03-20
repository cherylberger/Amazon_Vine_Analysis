# Amazon_Vine_Analysis
### Cheryl Berger
## Data Analytics Module 16 - Big Data

### Overview
This project analyzes customer reviews by members of the paid Amazon Vine program and determines if there is a bias toward favorable reviews from Vine members.  
The analysis uses PySpark to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, load the transformed data into pgAdmin for generate 4 seperate tables of the customer data.  We will use PySpark to calculate various metrics and determine if there is a bias toward favorable reviews for Vine members.  This analysis will focus on US reviews for shoes gathered from amazonaws.com.

### Resources
Software: Google Colab Notebook, PostgreSQL 11.9, pgAdmin 4, AWS
Data Source: https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Shoes_v1_00.tsv.gz

### Results

#### Deliverable 1

Perform a cloud based ETL on Amazon Product Reviews using AWS RDS database and upload the DataFrames into tables in PgAdmin.

 - Extract the Amazon Review dataset as a DataFrame
 
 ![image](https://user-images.githubusercontent.com/94234511/159126987-1bc8b808-dec7-40b5-ac9c-430e4fb74222.png)

 - Transform the extracted dataset into four seperate DataFrames.  The images of the DataFrame from Google Colab Notebook are shown below. 
 
 #### Review ID Table DataFrame
 
 #### Customers Table DataFrame
 
 #### Products ID Table DataFrame
 
 #### Vine Table DataFrame 
 
 
 - Load all four DataFrames into their respective tables in PgAdmin/  The images below reflect the output of the SQL query used to verify that the data was loaded into teach table 
 - 
 #### Review ID Table 
 
 #### Customers Table 
 
 #### Products ID Table
 
 #### Vine Table 


#### Deliverable 2

Using PySpark determine if there is any bias toward the reviews written as part of the Vine program. Discuss if having a paid Vine review makes a difference in the percentage of 5-star reviews.

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

- The results of the analysis show a slight positvity bias for the paid reviews. 

- The data set used was small as it was filtered on reviews that were deemed helpful by other users. The same metrics could be applied to the one of the other DataFrames to eliminate this bias.  

- It may be useful to determine the average star rating from the Vine and Non-vine reviewers to confirm the slight bias seen with the analysis of 5 star ratings only.  
