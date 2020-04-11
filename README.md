# Sentiment Analysis on COVID-19 Related News + SHAP Explanation

In this project I used SHAP (SHapley Additive exPlanations), a popular importance weighting method, to explain a machine learning model that classifies the sentiment of a certain piece of information.

## Watch it live!

This Jupyter Notebook contains Javascript plots. 
To view a fully interactive version, please access through [this nbviewer page](https://nbviewer.jupyter.org/github/JessieJessJe/COVIDsentiment/blob/master/SentimentAnalysis_SHAP.ipynb).

## The database

COVID-19 related news from 2020-03-16 to 2020-03-25,
retrieved from [News.API](https://newsapi.org/).

## The procedures

1) Using VADER to label the sentiment of each piece of news data: 1 - positive; 0 - negative
2) Establishing a news sentiment classifier using logistic regression
3) Applying SHAP LinearExplainer to explain the sentiment classifier
4) Verifying using feature weights of logistic regression

## Results

Summarize the effect of all the features:
![SHAP Global Explanation](https://freight.cargo.site/t/original/i/657a903a499948bbe32a3a42fb6ac48442324548b3565f4ebfe84aefb92dc637/Screen-Shot-2020-04-10-at-3.45.42-PM.png)

Explain each news sentiment prediction:

First example:
![SHAP Local Explanation](https://freight.cargo.site/t/original/i/a7319b53ab2dcc2bbee16a41074c2fbbb4feba8d69f1eb25ca586893a000ad9c/Screen-Shot-2020-04-10-at-3.58.51-PM.png)

Second example:
![SHAP Local Explanation](https://freight.cargo.site/t/original/i/8c6ff6c2b1e6b313a5048337cf8e699394555700ba89ffd53dd8534ca5cf4cac/Screen-Shot-2020-04-10-at-3.59.12-PM.png)

## Insights

There are certain words like “love” and “hate” we use everyday to represent a positive or negative feeling.

However, in the event of COVID-19, the model shows that some neutral words also have a strong association with feelings. For example, “Tuesday” indicates positive in the model.  

One possible reason is that the subjects behind these words are portrayed by the media with certain attitude.

This project provides a potential point of view to examine how we are perceiving the pandamic through the lens of media and how our feelings are changing as time goes by.

## Reference

A Unified Approach to Interpreting Model Predictions -- [see the NeurIPS paper](http://papers.nips.cc/paper/7062-a-unified-approach-to-interpreting-model-predictions.pdf)

Sentiment Analysis with Logistic Regression -- [see the Notebook](https://slundberg.github.io/shap/notebooks/linear_explainer/Sentiment%20Analysis%20with%20Logistic%20Regression.html)

VADER Sentiment Analysis -- [view on GitHub](https://github.com/cjhutto/vaderSentiment)
