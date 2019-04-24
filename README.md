# Project 3 - Reddit Web APIs & Binary Classification

## Objective : 
 
Our goal is two-fold:
1. Using Reddit's API, collect posts from two subreddits of choosing.
2. Use NLP to train a classifier on which subreddit a given post came from, which is a binary classification problem.

## Executive Summary

Data gathering by Scraping the data using Reddit API
Identify two Subreddits - Jokes & DataScience
Collect the Subreddit posts in to two dataframes  
Concat, create a final dataframe, prepare a CSV
Data cleaning & EDA
Data Modelling
Conclusions and Takeaways

## Data gathering by Scraping the data using Reddit API
A Reddit API named pushshift API was used to scrape the Reddit Posts. Response Data is returned in JSON format, results are collected and stored in a data frame, which is later appended into a custom list. Timestamp library has been used to convert the created_utc which is in epoch time to regular date and time format. 


## Identify two Subreddits - Jokes & DataScience
Identified two Subreddits of choice, which are 'jokes' and 'datascience'. Using the above mentioned scraping method, data for the two subreddits have been collected by searching the Reddit posts for the two subreddit submissions for the past 150 days.


## Collect the Subreddit posts in to two dataframes 
Once the data has been collected for the two subreddits of choice, in our case, the subreddits are 'jokes' and 'datascience', the data has been stored in to two separate dataframes 'jokes_df' and 'data_df'. Searching and collecting data for the past 150 days resulted in the collection of 2491 rows for 'jokes' and '1828' rows for 'datascience' subreddits.


## Concat, create a final dataframe, prepare a CSV
Both the jokes_df and data_df were concatenated to a final_df, which now has a shape of (4319, 9). The results were stored into a csv named 'reddit.csv' for further reference and use.
All the steps listed above were listed, data has been executed and captured in the 'Reddit-Scraping.ipynb'. 


## Data cleaning & EDA 
Data from the 'reddit.csv' has been loaded into a new dataframe 'final_df'. Nulls in the data have been looked into and dropped. A new df 'final_df_2' has been created by excluding '[removed]' and '[deleted] content from the dataframe. Two new columns were added to the new dataframe which are 'is_datascience' and 'title_text' for further use. These results were stored into a csv named 'reddit_EDA.csv' for further reference and use.
Steps taken for data cleaning and EDA were listed in the 'Reddit-EDA.ipynb'.


## Data Modelling
Data from the 'reddit_EDA.csv' has been loaded into a new dataframe 'final_df_2', which now contains 3523 rows and 11 columns after the data cleaning and EDA.

Used two modelling techniques 'Logistic Regression' and 'Multinomial Naive Bayes Classifier'.
Multinomial Naive Bayes classifier worked best for me with the Test Score - 0.987887963663891 and Train Score - 0.9750283768444948
Steps taken for modelling the data were listed in the 'Reddit-Modelling.ipynb'.


## Conclusions and Takeaways

Need to consider subreddits that are closely related to get better prediction 
● Test with other models 
● Explore new features 
● More cleaning needed, especially dealing with social media(links, #tags,emojis etc;).



 
