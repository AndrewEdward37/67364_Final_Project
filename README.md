# 67364_Final_Project: Analyzing trends in the US based on tweets during the COVID-19 Pandemic

## Introduction & Motivation

The SARS-CoV-2 has for the past year caused much difficulty and damage throughout the world. As of now, specifically in the United States - there have been over 13 million cases confirmed, with more than 150k new cases identified each day. Given the amount of glaring examples of people reacting in all sorts of ways to Covid-19, with protests against masks and outright declarations of it being a hoax, what really is the overall impression of people in the U.S. on the virus? Moreover, with the spread of "fake news" and the possibilities of such ideas floating about more rapidly with the lockdown and longer access to social media - has this had an effect peoples' perception in the United States? In other words, have peoples' opinions changed at all throughout the pandemic, and in what ways? These were the initial questions we asked ourselves while discussing the topic.

Our scope for the analysis broadened and we set on trying to understand and predict peoples' veiws on the virus depending on their social media interactions, specifically from their tweets. This was motivated further by two questions of "If there is a case of a significant amount of people not believing in the virus - is this more prominent in some places and why is that so?". To do so, we set out a series of goals in forms of analysis and modeling, building towards the sentiment analysis for predicted their opinions and opinion changes. Our goals were as follows:

- Analysis of the sentiment of tweets regarding the virus
- Understanding differences in word usage of "corona" and "Covid-19"
- A time series analysis on previous points, observing the changes over time
- Predicting which words could lead to a person having a specific sentiment (positive, negative)
- Preparing Word Clouds and Bigrams to show the interconnectedness of words within sentiments
- *Utilizing the previous points to build our own dictionaries for detecting more specific sentiment (believes, doesn't believe)
- *Predicting a persons' opinion towards the virus from their tweets

While we have managed to make good progress in the goals, we have set for ourselves, we did not reach the full extent of our motivated work. We hope to keep working on this project and cover the last two points (marked with *) to see our scope to fruition. Moreover, we further hope to gain access to more specific location of tweets to answer our further motivations of state-by-state analyses and the possibility of our model being used in national decision making.

## Data Collection
To collect tweets from older months, we could not use the Twitter API free version because it only acquires tweets in the past seven days.
And since Twitter launched V2 of its API this September and retired the old one, all libraries and work-arounds were no longer an option.
So to collect our data we used [snscrape](https://github.com/JustAnotherArchivist/snscrape).
A scraper for social networking services (SNS). With it, we scrapped Twitter's search page, which returns a lot of any time you choose but does not return everything.
This is a limitation for the paper but we just used this data to explore and showcase all sorts of analysis that we can do if we had access to the premium API.

We created a list of keywords, mostly focusing on `Covid-19` and `Corona` to retrieve all tweets using snscrape.
For every tweet, we collected the date, text and if the person who tweeted used COVID-19 or Corona when talking about the virus.
We were not able to add more search terms becasue there were some bugs with the scraper. It would return tweets outside of the range we wanted to examine.
If we had access to the premium API we would be able to use more keywords to search such as, `pandemic`, `virus`, `hoax`, `fake news`.

Moreover, all tweets retrieved are from the United States of America.

Tweets collected were around `25,000 tweets` from 1st of March 2020 to 30th of November 2020.
