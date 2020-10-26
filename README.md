# Wrangle and Analyze Data
Udacity Data Analyst Nanodegree - Project 4

## Project Overview
#### Introduction
The dataset that I will be wrangling (and analyzing and visualizing) is the tweet archive of Twitter user @dog_rates, also known as WeRateDogs. WeRateDogs is a Twitter account that rates people's dogs with a humorous comment about the dog. These ratings almost always have a denominator of 10. The numerators, though? Almost always greater than 10. 11/10, 12/10, 13/10, etc. Why? Because "they're good dogs Brent." WeRateDogs has over 6 million followers and has received international media coverage.

WeRateDogs downloaded their Twitter archive and sent it to Udacity via email exclusively to use in this project. This archive contains basic tweet data (tweet ID, timestamp, text, etc.) for all 5000+ of their tweets as they stood on August 1, 2017. 

#### What do we need to install?

We need to be able to work in a Jupyter Notebook

The following packages (libraries) need to be installed.
- pandas
- NumPy
- requests
- tweepy
- json

## Project Details

Following were the tasks of this project:

- Gathering Data
- Assessing Data
- Cleaning Data

### Gathering Data

The data for this project consists of three different datasets that were obtained as following:

1. **Twitter archive file:** The *twitter_archive_enhanced.csv* file was provided by Udacity and was downloaded manually.
2. **The tweet image predictions:** The *image_predictions.tsv* file has information about what breed of dog is present in each tweet according to a neural network. This file is hosted on Udacity's servers and was downloaded programmatically using the Requests library and the given URL.
3. **Twitter API & JSON:** By using the tweet IDs in the WeRateDogs Twitter archive file, I queried the Twitter API for each tweet's JSON data using Python's Tweepy library and stored each tweet's entire set of JSON data in a file called *tweet_json.txt* file. I read this .txt file line by line into a pandas dataframe with tweet ID, favorite count, retweet count, followers count, friends count, source, retweeted status and url.

### Assessing Data

After gathering each of the above pieces of data, I assessed the data as following:

1. **Visually:** The above pieces of data were assessed visually by printing the three entire dataframes separate in Jupyter Notebook.
2. **Programmatically:** The above pieces of data were assessed programmatically by using different methods (e.g. info, value_counts, sample, duplicated, groupby, etc). 

Then I separated the issues encountered in quality issues and tidiness issues.

### Cleaning Data
Before starting the cleaning process, I made a copy of each dataframe. All of the cleaning operations were conducted on this copy so we can still view the original dirty and/or messy dataset later. This part of Data Wrangling was divided in three parts: Define, Code, and Test the code.

These three steps were performed on each of the issues described while assessing the data. First the Quality and Tidiness issues were solved on each dataframe and then all these dataframes were merged to form one single dataframe.

This dataframe is exported to csv as *twitter_archive_master.csv*. This dataframe was eventually used for analyzing and visualizing the data.

## Conclusion
At the end of the gathering, assessing and cleaning process, we get high quality and tidy master pandas DataFrame which is stored as *twitter_archive_master.csv* which was further used for analysis and visualization.
