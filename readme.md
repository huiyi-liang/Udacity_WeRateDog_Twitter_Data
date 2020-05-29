# Udacity Project: Wrangle WeRateDogs Twitter Data

## Project Overview
Project is part of Udacity Data Analyst Nanodegree program to wrangle WeRateDogs Twitter data to create interesting and trustworthy analyses and visualizations. WeRateDogs is a Twitter account that rates people's dogs with a humorous comment about the dog. Ratings have denominator of 10 with numerators that can exceed 10.

## Outline of Analysis
* Gathering data from the sources listed below 	
* Assessing data both visually and programmatically for quality and tidiness issues
* Cleaning data to produce a  high quality and tidy master pandas DataFrame
* Storing, analyzing, and visualizing Data
* Reporting insights (found on pdf)

## The Data
Three different data sources were used to generate the master dataset: 
1.	Enhanced Twitter Archive csv file provided by WeRateDogs for basic Tweet information (Tweet ID, timestamp, and data extracted from the Tweet content) 
2.	Image Prediction File produced from a neural network to classify the Tweet’s dog breed found on [url link](https://d17h27t6h515a5.cloudfront.net/topher/2017/August/599fd2ad_image-predictions/image-predictions.tsv)
3.	Twitter’s API for additional information (e.g. retweet and favorite counts)

Note: The API data gathering consist of requesting API access, creating a JSON file on the Twitter data found for Tweets listed in the Archive file, and loading the JSON data into a dataframe in Jupyter Nto assess the data. 

Below code is needed to access Twitter API data once acccess token keys are provided. This code was removed from Jupyter notebook due to security purposes. 
```
import tweepy

consumer_key = 'YOUR CONSUMER KEY'
consumer_secret = 'YOUR CONSUMER SECRET'
access_token = 'YOUR ACCESS TOKEN'
access_secret = 'YOUR ACCESS SECRET'

auth = tweepy.OAuthHandler(consumer_key, consumer_secret)
auth.set_access_token(access_token, access_secret)

api = tweepy.API(auth, parser = tweepy.parsers.JSONParser(), wait_on_rate_limit=True,wait_on_rate_limit_notify=True)
```
