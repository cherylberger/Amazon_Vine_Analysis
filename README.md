# Amazon_Vine_Analysis
### Cheryl Berger
## Data Analytics Module 16 - Big Data

### Overview

### Resources


https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Shoes_v1_00.tsv.gz

### Results

#### Deliverable 1
Perform a cloud based ETL on Amazon Product Reviews using AWS RDS database and upload the DataFrames into tables in PgAdmin
 - Extract the Amazon Review dataset as a DataFrame
 - ![image](https://user-images.githubusercontent.com/94234511/159126987-1bc8b808-dec7-40b5-ac9c-430e4fb74222.png)


 - Transform the extracted dataset into four seperate DataFrames
 
 - Load all four DataFrames into their respective tables in PgAdmin

#### Deliverable 2
Using PySpark determine if there is any bias toward the reviews written as part of the Vine program. Discuss if having a paid Vine review makes a difference in the percentage of 5-star reviews.
- How many Vine reviews and Non-vine reviews were there?
- How many Vine reviews were 5 stars?  How many Non-vine reviews were 5 stars?
- What percentage of Vine reviews were 5 stars?  What percentage of Non-vine reviews were 5 stars?

### Summary
The results of the analysis show a slight positvity bias for the paid reviews. 
The data set used was small as it was filtered on reviews that were deemed helpful by other users. The same metrics could be applied to the one of the other DataFrames to eliminate this bias.  It may be useful to determine the average star rating from the Vine and Non-vine reviewers to confirm the slight bias seen with the analysis of 5 star ratings only.  
