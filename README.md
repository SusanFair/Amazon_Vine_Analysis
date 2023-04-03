# Amazon Vine Analysis

## Overview of the analysis: Explain the purpose of this analysis.
This analysis was an ercisie in using Big Data with AWS RDS, postgreSQL, pgAdmin and Google Collabary.

RDS: <br> 
A database was created in RDS and linked to pgAdmin
![Alt text](https://github.com/SusanFair/Amazon_Vine_Analysis/blob/main/Resources/RDS_activity.PNG)

pgAdmin: <br>
Tables were created in PgAdmin for analysis
![Alt text](https://github.com/SusanFair/Amazon_Vine_Analysis/blob/main/Resources/review_id_table.PNG)

![Alt text](https://github.com/SusanFair/Amazon_Vine_Analysis/blob/main/Resources/products_table.PNG)

![Alt text](https://github.com/SusanFair/Amazon_Vine_Analysis/blob/main/Resources/customers_table.PNG)

![Alt text](https://github.com/SusanFair/Amazon_Vine_Analysis/blob/main/Resources/vine_table.PNG)

Collabary: <br>
Data was imported and loaded up into pgAdmin.
As well the analysis performed using PySpark in the Colab workbook to gather the final stats.


## Results: 
A cleaned data set was used containing votes where helpfull votes over total votes was greater than 50%.

After data cleaning there were a total of 48,283 reviews in our dataset.

#### Vine reviews vs non-Vine reviews?
* Of the paid Vine reviews there was a total of 580 reviews
* Of the non-paid reviews there was a total of 47,703 reviews

#### How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?
* Paid vine reviews that were greater than or equal to 5 stars were 246 out of the 580 total paid reviews
* Unpaid reviews greater than or equal to 5 stars were 23837 out of the total 47703 unpaid reviews

#### What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?
* Paid vine review >= 5 stars were 42% of the total paid vine reviews
    ![Alt text](https://github.com/SusanFair/Amazon_Vine_Analysis/blob/main/Resources/paid_vine_stats.PNG)

* Unpaid reviews >= 5 stars were 50% of the total unpaid reviews

    ![Alt text](https://github.com/SusanFair/Amazon_Vine_Analysis/blob/main/Resources/Unpaid_stats.PNG)


## Summary: 

Based on the analysis performed there does not seem to be any positivity bias for reviewers in the Vine program.  The 5 star review ratio within the vine program was actually lower at 42% than the unpaid reviews with those reviewers giving a 5 or greater rating 50% of the time.

#### Further Analysis Options:
To evaluate the successfulness of the program I would look at two different statistics.

* Do paid Vine users give more reviews that unpaid shoppers?  In particular do they give more viable or helpful reviews that their counterparts.

* Also what is the percentage of paid Vine reviews who actually made a verified purchase.  To really review a product hands on testing is the real key ingredients in the value of the review.  This analysis might be performed by filtering on Vine "Y" reviews & verified purchse and comparing that dataset with the Vine "N" reviews & verified purchase.




In your summary, state if there is any positivity bias for reviews in the Vine program. Use the results of your analysis to support your statement. Then, provide one additional analysis that you could do with the dataset to support your statement.