---
title: Hip Hop Recommendation
layout: projects
classes: wide
---

## Introduction

This was a project that I worked on in a text mining course at the University of Montana. Initially, the goal was to automate some sort of web scraper, and build a clean dataset for some sort of textual analysis. I chose to create a dataset of song lyrics, as they are pretty easily found online, and fun to work with. After creation of my dataset, I was inspired to go a bit further than to just do a routine analysis of key words, sentiment, etc. So, I decided to create a recommendation engine that is based entirely off of song lyrics. 

## Data
The dataset that I built contains over 100K different hip-hop songs from over a thousand artists (before cleaning and removal of some songs/artists). Creating and cleaning this dataset was the most time consuming part of this project, as it typically is for any data science project. Special care was taken in the cleaning process to remove 'non-songs' (parody, poem, live versions, etc.) as well as preserve specific elements of the text used for feature engineering. 

## Word/Document Embeddings
An important aspect of many recommendation engines is the ability to compute some sort of similarity measure. This gets especially difficult with text. To do this, we make use of sentence/document embedding models. If you are not familiar with sentence/document embeddings I would encourage you to [read](https://livebook.manning.com/book/deep-learning-for-search/chapter-6/3a) a bit on what they are/how they work.

When I first began this project I trained my own Doc2Vec model which worked well. Since then I have transitioned to using pre-trained [sentence transformers](https://www.sbert.net/).

## App
Enjoy the app below and let me know how good/bad your recommendations are!
 Hosted on Hugging Face Spaces. There are some plotting issues with embedded hugging face spaces, for a better view check out [here](https://huggingface.co/spaces/brendenc/Hip-Hop-gRadio)

<html>
<head>
<script type="module" src="https://gradio.s3-us-west-2.amazonaws.com/3.0.20/gradio.js"></script>
</head>
</html>

<gradio-app space="brendenc/Hip-Hop-gRadio"> </gradio-app>
