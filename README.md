# Tweet Sentiment

# Problem Statement

The aim of this project is to build a NLP classification model that can accurately classify a users tweets as "Negative", "Positive" or "Neutral". Having an effective model is important since it will be tracking the textual behavior in real time to predict if the context of a tweet is positive or not. With the use of this predictive model, companies can be learn about newly deployed features reactions in order to determaine better business strategies.



### For this project I will be using the OSEMiN framework, wich stands for Obtain, Scrub, Explore, Model and Interpret. 

* Obtain: The dataset consists of 9,000 user tweets and was downloaded from the Data.world Datasets Library.

* Scrub: I will search for null values and outliers to replace them with more suitable values or delete them form the data set. I will also look at multicollinearity issues amongst the features and find creative ways to deal with them.

* Explore: Throughout the whole process, it is important to lookout for other important information that can be gathered from the data. I will carry out Exploratory Data Analysis and answer relevant questions about the current state of business.

* Model: I will use single and ensemble binary classification models. The aim of the project is to select the best performing model and fine-tune its hyperparameters to achieve correct identification of user sentiment.

* Interpret: Interpret the results of the models to make recommendations that generate value.



# Results

## Deep NLP

<img src='https://raw.githubusercontent.com/phillipojo24/Mod-4-project/master/Screen%20Shot%202021-02-01%20at%209.03.31%20PM.png'>

Our Initial Model has an accuracy of 64% however this is not a good criterion to judge whether the model is predicting correctly for our business case because the data set is imbalanced. Even thought we gave the Neural Network the option to weigh the minority classes higher than the majority, we still found the model to perform poorly.

## Vanilla Random Forest with Tfidf vectorizer

<img src='https://raw.githubusercontent.com/phillipojo24/Mod-4-project/master/Screen%20Shot%202021-02-01%20at%209.05.00%20PM.png'>

The dataset distribution is imbalanced. We must use some sort of "oversampling" tequnice to balance out the dataset. Theres a method called upsampling that is used around tweet sentiment analysis that consists of adding new tweets for the minority classes, positive and negative, to have them reach a number of tweets equal to the majority class, Neutral here. If we do not do this, the model will try and predict a Neutral label as it is 60% guaranteed due to the imbalance.

## Upsampling

This is a technique were we use a function that repeatedly takes samples, with replacement, from the minority class until the class is the same size as the majority.

## Random Forest with "upsampling" technique

<img src='https://raw.githubusercontent.com/phillipojo24/Mod-4-project/master/Screen%20Shot%202021-02-01%20at%209.05.16%20PM.png'>

# Conclusion / Recomendations

* Random Forest Classifier proved to be the best suitable model for this dataset.

* After using a "upsampling" technique, our model was able to predict Negative tweets by a user 93% of the time which is very impressive do to with the very initial imbalanced data set.

* Words like "ipad", "iphone", "apple" were important in helping the model predict the differnt classes. We will have to do future analysis to see which classes it specifically impacted in predicting.

# Future Work

   * Improve the model by removing words in very low or high frequency

   * Find better ways to clean the tweets for better pre processing. Alot of mispelled words and repeated letters.


```python

```
