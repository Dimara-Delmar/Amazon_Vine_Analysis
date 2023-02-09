# Amazon Vine Analysis

## Overview of the Project

### Purpose
The Amazon Vine Program is a service that allows manufacturers to pay for reviews on their products. In this analysis, we will be given access to amazon review datasets to use the ETL process (extract, transform, and load) to connect to an AWS RDS instance, and view the data in pgAdmin. Once the data is loaded into pgAdmin, we will then use Pandas to determine if there is a bias towards favorable reviews given by Vine members or not. 

## Resources
- Data Source: [Amazon Video Game Review dataset](https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Video_Games_v1_00.tsv.gz), `vine_table.csv`
- Software used: Google collab, AWS, Pandas, Jupyter Notebook, SQL and PySpark

## Results

Using Pandas to run an analysis on the Vine data table, these are the following results: 

<img width="379" alt="number_of_reviews" src="https://user-images.githubusercontent.com/108738297/217693468-c08c5d72-f02c-43d4-bb32-8f689c9d3b5a.png">

-	The total number of Vine (paid) reviews is 94.
-	The total number of non-Vine (unpaid) reviews is 40,471.

<img width="379" alt="5_star_reviews" src="https://user-images.githubusercontent.com/108738297/217693831-fca8af48-9555-4b9c-81f0-269e8d7542b8.png">

-	The total number of Vine 5-star reviews is 48.
-	The total number of non-Vine 5-star reviews is 15,663.

<img width="378" alt="5_star_percent" src="https://user-images.githubusercontent.com/108738297/217693952-4ff9553c-aabf-410c-849c-28bf5ca8ba0c.png">

-	The total percentage of Vine 5-star reviews is 51.0%.
-	The total percentage of non-Vine 5-star reviews is 39.0%.

## Summary

Based on the results of the analysis, it’s safe to admit that there is a positive bias towards the reviews in the Vine program. The program provides an incentive for positive reviews since it pays their reviewers to evaluate the product. There are much fewer total vine program reviews (94) when compared to non-Vine reviews (40,471), and of those Vine reviews, more than half (51%) were rated as 5-stars, when compared to the lower percentage of non-Vine 5-star reviews (39%).  

For further analysis, we could create summary statistics to compare the average amount of 5-star reviews between Vine and non-Vine members.  
