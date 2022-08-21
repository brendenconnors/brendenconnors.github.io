---
title: Trump's Election Twitter Storm
layout: projects
---

Regardless your political leaning, Donald Trump's tweets during the 2020 election were hard to miss. Below, I investigated Trump's changing sentiment on Twitter prior to and during the 2020 presidential election.

## What is "Sentiment"?
Sentiment analysis allows us to score a statement on a scale from -1 to 1, where -1 represents a 
very negative statement, and 1 represents a very positive statement. So, "I love everything!" would be near 1, "I hate everything!" would be near -1, and "the turtle is green." would be near 0.

NLTK's Vader is used for sentiment analysis to preserve exclamations and capitalization, which is particularly important for Trump's tweets like "I WON THIS ELECTION, BY A LOT!""

## Methods
For each Trump tweet from November 1st through November 12th, a sentiment score is calculated. Sentiment analysis is rather noisy, so some form of aggregation is needed discover any sort of pattern. Here we calculate the average sentiment in disjoint 12 hour windows. This was done so each day has a point that represents his sentiment in the morning and night. Each of these points is plotted at the midpoint of their 12 hour window (6 a.m. and 6 p.m.). Note: Tweets that only contain media and retweets are removed.

**Notes:** All state race call times are from the Associated Press. Only updates in Electoral College votes are plotted after 1:00 a.m. on November 4th to avoid rapid jumps in the data.

{% include trump_sentiment.html %}
{% include trump_table.html %}

<br>
Data Sources: [@AP_politics](https://twitter.com/AP_Politics?ref_src=twsrc%5Egoogle%7Ctwcamp%5Eserp%7Ctwgr%5Eauthor),
[@realDonaldTrump](https://twitter.com/realDonaldTrump),
[Alex Gaynor & NYT](https://github.com/alex/nyt-2020-election-scraper)

Citations: <br>
Hutto, C.J. & Gilbert, E.E. (2014). VADER: A Parsimonious Rule-based Model for
Sentiment Analysis of Social Media Text. Eighth International Conference on
Weblogs and Social Media (ICWSM-14). Ann Arbor, MI, June 2014.