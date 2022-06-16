# Analysis of Amazon Vine Reviews

# Overview

Looking at the Amazon data from the Amazon Vine program, the project evaluates reviews by paying and non-paying members of the program.  The dataset was selected from Amazon Review Datasets, extracted into a DataFrame using Pyspark on Google Colab notebooks and then analyzed. 

# Review

Using the Shoes dataset from Amazon Review Dataset, the files were loaded into a Google Colab notebook and then into a dataframe, using Spark. Some assumptions were made of the Vine Program in order to get a dataset with a robust number of reviews: 
- The reviews table was filtered to only include rows were the total counts were equal to or greater than 20, as the greater number indicates a review that is more likely to be helpful. 
- The number of "helpful_votes" was dividied by the number of "total_votes" and filtered to include only those rows with a ratio that was equal to or greater than 50%. 
- Finally, the reviews were seperated into tables based on the paying status of the user (paid or unpaid) members. 

The results of the analysis indicate the following: 

![total_review](https://user-images.githubusercontent.com/98054953/174163834-4b079ae7-ad25-4165-b12a-0a474f40cc6b.png) ![paid_reviews](https://user-images.githubusercontent.com/98054953/174163876-017df9d1-c38d-49a9-a09b-a3b57b251fb6.png) ![unpaid_review](https://user-images.githubusercontent.com/98054953/174163908-8ad5c4bd-c0a2-44e4-875d-89ce1dbc9188.png)

1. Out of 27,009 reviews, 22 were Vine (paid) reviews and 26,987 were non-Vine (unpaid) reviews. 
2. For the Vine reviews, 13 out of 22 were five star reviews. For the non-Vine reviews, 14,475 out of 26,987 were five stars.
3. 59% of the Vine reviews were 5 stars and 54% of the non-Vine reviews were five stars.

# Summary

There are many more reviews that are non-paid (non-Vine) in the Amazon Review Dataset, given the assumptions of the number of reviews as well as using only those that were helpful at least 50% of the time.  Of the 27,009 reviews only 22 (or 0.08%) were paid.  The Vine reviews were slightly more positive (59% vs 54%) but probably within the margin of error.  It would be interested to look at all the reviews and see if there is a stronger bias in the Vine reviews where there is a smaller number of reviews per item or the reviews are deemed less helpful. 

