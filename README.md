# Amazon_Vine_Analysis
## Overview
Performed an analysis on Amazon’s Vine Review Program using review data of Outdoor product purchases from Amazon. The Vine Program was an incentive offered by sellers wherein users that gave Vine reviews were provided with free products. The purpose of this analysis was to determine whether there was a bias from the Vine verses non-Vine reviewers.
## Resources
Dataset: 

-	https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Outdoors_v1_00.tsv.gz

Applications/Technologies:

-	Google Colab (to run PySpark)
-	Jupyter Notebook (for Pandas/Python)
-	AWS RDS
-	PosgreSQL

## Results

To determine if there was a bias, the reviews were first filtered so that only products with over 20 total votes were analyzed.

![total_votes_over_20](https://user-images.githubusercontent.com/101822948/182985210-eea57283-7692-47ae-89dc-abf114259e63.png)

The data was further filtered by creating a new dataframe that reflected a 50% or greater relationship of helpful votes vs total votes. This filtered dataframe was then used to create two additional dataframes: one of paid Vine reviewers and another of nonpaid Non-Vine reviews.

![Vine_vs_NonVine](https://user-images.githubusercontent.com/101822948/182985256-bd048dc6-a848-4631-82a1-76f005a372a7.png)


I determined the total number of reviews, the number of 5-star reviews, and the percentage of 5-star reviews for both paid Vine reviewers and unpaid non-Vine reviewers.

The results from the analysis were as follows:

For paid Vine reviews:

-	Total reviews: 107
-	Number of 5-star reviews: 56
-	Percentage of 5-star Vine reviews: 52.3%

For nonpaid non-Vine reviews:

-	Total reviews: 39,869
-	Number of 5-star reviews: 21,005
-	Percentage of 5-star non-vine reviews: 52.7

## Summary

Based on the analysis, there does not appear to be a bias among the Vine reviewers for outdoor products compared to the non-Vine. The percentage of 5-star reviews for both groups was 52%, with the non-Vine reviewers showing a slightly higher percentage of 5-star reviews (52.7% compared to 52.3% of Vine reviews). 

Additional analyses is likely required to determine if there is a bias from the Vine reviewers. Some additional analyses that could be used might include using Natural Language Processing on the actual comments to determine if any appear to be form-based or non-product specific. Other analysis might include using 4 and 5 star reviews since some people will not give 5 star reviews unless the product exceeds expectations. 
