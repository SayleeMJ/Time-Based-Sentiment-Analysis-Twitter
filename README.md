# Time Based Sentiment Analysis Twitter
Allows the user to analyze Twitter sentiment based on selected time events  and visualizes  the results

## 1. Introduction:

Allow the user to provide a hashtag as input and gather all the data related to the given hashtag (E.g. #GunReform). Perform sentiment analysis on extracted tweets and plot them in time series format.  Along with Time series data plotting, plot Geolocation data, Devices used for tweeting, and information like count of unique users, tweet likes, re-tweets, etc.

As part of dynamic implementation, a user can select a date. According to the date selected by the user ‘before-and-after sentiment analysis graph’ will be updated. The main purpose of this implementation is to determine how people have reacted to specific events (such as the Parkland mass shooting), to what extent they used Twitter to express their thoughts, and how the response has been formed over time. Also, information like several tweets, likes, unique tweets, etc. can help us to have a good visualization on many technical aspects.


## 2. How to run:

Step 1: Specify user authentication data in the auth_dict file.
Step 2: Install dependencies if required.
Step 3: You can run the entire project as we have provided a pre-trained classifier as well as a sample database for the ‘gunreform’ hashtag.
Step 4: Select the date against which you would like to analyze tweets and accordingly graph will be updated.
Step 5: At the end of Jupiter notebook we have given code to gather data for new hashtags and a way to download sample_tweets data set to retrain the classifier. 

## 3. Dependencies:

[Note: We are using bokeh version 0.12.7 on our system for development]

Installing dependencies using conda (install conda if required):

``` bash
python -m bokeh info
conda uninstall bokeh
conda install bokeh=0.12.7
conda install NumPy
conda install blaze
conda install dask
conda install pandas
```

Installing dependencies using pip:


```  bash 
pip install jsonpickle
pip install tweepy
pip install -U nltk
```

## 4. How the project works:

#### 1. User Enters Hashtag
We have provided a text box where the user can input all the hashtags on which he wants to perform time-based analysis.

#### 2. Gathering information from Twitter and performing sentiment analysis 
Once we have all the hashtags users want to search for, we will query Twitter using Tweepy API to get all tweets related to hashtags.

#### 3. Preprocess data and sentiment analysis
Once we have all the information related to hashtags we will extract the following fields from it:

----
Tweet_Ids, User_Ids, Date, ReTweet_Count, Location, Likes, TweetSource, Actual tweets
----


Then we will perform sentiment analysis on tweets and we will store all information along with tweet sentiment in the database for further analysis and visualization.

#### 4. Acceptance of analysis date from the user
We have provided a drop-down list for user from which user can select a date on which user want to divide tweets. This division of tweets will be used to analyze the effect of selected date on tweets and user sentiment.

#### 5. Visualize results
Once we have all the processed information we can visualize the results based on the date entered by the user using graphs such as time series, geo-plot, sentiment analysis bar graph, etc.

## 5. Results

![Graph1](https://github.com/SayleeMJ/Time-Based-Sentiment-Analysis-Twitter/blob/main/results/graph1.png)
![Graph2](https://github.com/SayleeMJ/Time-Based-Sentiment-Analysis-Twitter/blob/main/results/graph2.png)
![Graph3](https://github.com/SayleeMJ/Time-Based-Sentiment-Analysis-Twitter/blob/main/results/graph3.png)
![Graph4](https://github.com/SayleeMJ/Time-Based-Sentiment-Analysis-Twitter/blob/main/results/graph4.png)
![Graph5](https://github.com/SayleeMJ/Time-Based-Sentiment-Analysis-Twitter/blob/main/results/graph5.png)
![Graph6](https://github.com/SayleeMJ/Time-Based-Sentiment-Analysis-Twitter/blob/main/results/graph6.png)

