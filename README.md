# Wrangle_Act
In this project, we gathered data from the WeRateDogs Twitter archive. The goal for this project is to wrangle WeRateDogs Twitter data to create interesting and trustworthy analyses and visualizations.
# Requirement
Create a 300-600 word written report called wrangle_report.pdf or wrangle_report.html that briefly describes your wrangling efforts. This is to be framed as an internal document.

This involves the analysis of WeRateDogs. This data was presented from udacity for students to work on as our second project. The data sets are in three files.

The first one is the twitter_archive which includes more than 5000+ retweets. The second one was gotten by using neursl network to predict if the images present are dogs and with what probability. The third data will be gotten by students where we will query twitter retweet count and favorite count using the twitter id present.

The steps involved in the analysis of this projects includes:

Gathering data
Accessing data
Cleaning data
Storing data
# Gathering data
Three data are used here which are "twitter_archive_enhanced.csv", "image_predictions.tsv" and "tweet_json.txt" which was read line by line into a dataframe.

- twitter-archive-enhanced.csv
Downloaded the WeRateDogs Twitter archive from the link give in the instructions by Udacity. Once I manually downloaded the twitter-archive-enhanced.csv file to my computer I placed it in the notebook project directory. Once I started the notebook, I imported to the notebook using the read_csv command with utf-8 encoding.

- image-predictions.tsv
I then proceeded to programmatically download the image-predictions/image-predictions.tsv file using the Request Library from the URL provided by Udacity.

- tweet_json.txt
In order to generate the tweet_json.txt file, I proceeded to sign up for a Twitter Developers API. I followed the helpful instructions provided by Udacity. I then proceeded to create an application in the Twitter Developers API and create a Twitter API key, secret, and token for my app.

# Assessing
These datasets was assessed for the following quality and tidiness issue, 8 quality and 2 tidiness issues were gotten and were cleaned. It is necessary to clean our data for easy analysing and visualisation

# Quality Issues
## Twitter_archive
- Name column contains invalid values stored as None, the,and a etc.
- Null objects are represented as None in several columns
- Some of the tweet are not actual tweet but are reply or retweet
- Extract from "source" the medium/device in which the tweet were retweet from
- Extract "rating" from the "text" column
- Columns that are not needed such as "in_reply_to_status_id", "in_reply_to_user_id", "text", "retweeted_status_id", "retweeted_status_user_id", - "retweeted_status_timestamp", "expanded_urls", should be deleted
- Time stamp is object instead of date time
## image
Incomplete data set i.e 2075 available instead of 2356

# Tidiness Issues
## Image
- Dog stages are in multiple columns
- Combine the three data sets
# Cleaning Data
I completed all the cleaning steps by using the programmatic data cleaning process. With each step, I executed the code, verified and confirmed there weren't any errors. Once I had completed the cleaning and tideness of the archive dataframe I created a new dataframe called df_clean and save it into a new csv file. These are the different python built-in-functions and methods use for programmatic data cleaning process. i.e

.info() .tail() .head() .value_counts()

# Storing Data
After completing the cleaning process, I saved the final_data dataframe into a "twitter_archive_master.csv" file . I confirmed visually that the file was saved successfuly and also confirming programmatically by using the info() function.

# Visualising Data
After clearning the dataframe, the data was cleaned and I could generate graphs to visually present the data. I used various types of graphs and plots using multiple libraries such as matplotlib and seaborn.
