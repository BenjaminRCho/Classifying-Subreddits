# Classifying Subreddits

### This Repo Contains:

1. Subreddit to CSV
    - This notebook covers the scrapping Reddits through their API and saving the data to a CSV
2. Reddit Prediction Project
    - This notebook covers classifying the first pair of subreddits that are unrelated to each other
3. Other Reddit Predictions
    - This notebook covers classifying the second pair of subreddits where the two cover the same topic
4. Other Reddit Predictions 2
    - This notebook covers classifying the third pair of subreddits where one subreddit is a subcategory of the other subreddit
5. Data
    - The required CSVs to run the code
    

## Executive Summary

One of the widely used natural language processing task in business problems is text classification. The goal of this project is to take a look at how accurately we can predict what posts belong in which subreddit with the features on the site. By scrapping data from Reddit’s API, features from targeted classes Jokes and Talesfromtechsupport were gathered. 


After collecting the data, preprocessing of the text documents was required in order for models to be built. There were two methods for converting the data into numbers. The first way was to count the frequency of each word, plain and simple. The other also looked at the term frequency but adjusted that to the account for words that are rare or very common. Once this was completed, models were built on these features separately: title, post, and both title and post. Logistic Regression, Random Forest Classifier and Multinomial NB were the three different classification models used for my data. 


As a result, the Logistic Regression model performed the best with a 99% probability of accurately predicting posts with subreddits. By looking at the highest coefficients of the model, the most important words were distinguished in determining which posts came from which subreddit. The main reason this model outperformed others is due to the two classes being very different from each other and that makes it linearly separable. 


Although the model performed fantastic, we need to consider the limitations of this model. Two other pairs of datasets were explored to confirm whether selecting the data can have a dramatic influence on how well the model does. When the models were tested on two subreddits that are very similar, the accuracy results of each model were extremely poor. However, when the models were tested on two subreddits where one was a subset topic of the other one, the Random Forest model result was noticeably better than the models for the first pair. 


All in all, the model is adept at predicting what posts belong to which subreddit when they are very different from each other. However, the model can be further improved to consider the relationship between the classes we are trying to predict. 
