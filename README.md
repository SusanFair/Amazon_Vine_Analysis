# Amazon Vine Analysis

## Overview of the analysis: 
This analysis was an exercise in using Big Data with AWS RDS, postgreSQL/pgAdmin and Google Colabratory.

#### RDS: <br> 
A database was created in RDS and linked to pgAdmin<br>
![Alt text](https://github.com/SusanFair/Amazon_Vine_Analysis/blob/main/Resources/RDS_activity.PNG)

#### pgAdmin: <br>
A new server instance and database were created in pgAdmin.  
Tables were created to match the dataframes created in Colabratory. <br>

![pdAdmin Tables](https://github.com/SusanFair/Amazon_Vine_Analysis/blob/main/Resources/pgAdmin_tables.PNG)

Data was loaded into each tabelfrom Colab:<br>
    ![customers_table](https://github.com/SusanFair/Amazon_Vine_Analysis/blob/main/Resources/customers_table.PNG)

    ![products_table](https://github.com/SusanFair/Amazon_Vine_Analysis/blob/main/Resources/products_table.PNG)

    ![review_id_table](https://github.com/SusanFair/Amazon_Vine_Analysis/blob/main/Resources/review_id_table.PNG)

    ![vine_table](https://github.com/SusanFair/Amazon_Vine_Analysis/blob/main/Resources/vine_table.PNG)

#### Colabratory: <br>
Data was imported from AmazonAWS. The data was cleaned and analysis performed using PySpark in the Colab workbook to gather the final stats.  The output migrated to the RDS database with the newly created dataframes matching the tables that had been created in pgAdmin.

Two workbooks were created:<br>
* Amazone_Reviews_ETL - used to build the database contents
* Vine_Review_Analysis - used to performa Analysis on the Vine users and their affect on reviews.

## Results: 
A cleaned data set was used containing votes where helpfull votes over total votes were greater than 50%.

After data cleaning there were a total of 48,283 reviews in our dataset.

#### Vine reviews vs non-Vine reviews?
* Of the paid Vine reviews there was a total of 580 reviews
* Of the non-paid reviews there was a total of 47,703 reviews

#### How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?
* Paid vine reviews that were greater than or equal to 5 stars were 246 out of the 580 total paid reviews
* Unpaid reviews greater than or equal to 5 stars were 23837 out of the total 47703 unpaid reviews

#### What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?
* Paid vine reviews >= 5 stars were 42% of the total paid vine reviews
    ![Alt text](https://github.com/SusanFair/Amazon_Vine_Analysis/blob/main/Resources/paid_vine_stats.PNG)

* Unpaid reviews >= 5 stars were 50% of the total unpaid reviews

    ![Alt text](https://github.com/SusanFair/Amazon_Vine_Analysis/blob/main/Resources/Unpaid_stats.PNG)


## Summary: 

Based on the analysis performed there does not seem to be any positivity bias for reviewers in the Vine program.  The 5 star review ratio within the vine program was actually lower at 42% than the unpaid reviews with those reviewers giving a 5 or greater rating 50% of the time.

#### Further Analysis Options:
To evaluate the successfulness of the program I suggest two different statistics.

* Do paid Vine users give more reviews that unpaid shoppers?  In particular do they give more viable or helpful reviews that their counterparts.

* Also what is the percentage of paid Vine reviews who actually made a verified purchase.  To really review a product, hands on testing is the real key ingredient in the value of the review.  This analysis might be performed by filtering on Vine "Y" reviews & verified purchases and comparing that dataset with the Vine "N" reviews & verified purchases.

