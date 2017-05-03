# Predicting Movie Genres

Kyle Honegger, Mark Hill, Joseph Reilly <br>
CS109b final project, Spring 2017

## Milestone 1
### Milestone_1_Kyle_Joe_Mark_v2.ipynb

This notebook contains our preliminary trials of working with the movie databases, as well as some EDA where we investigate the frequency of the most common movie pairs, text data from reviews and similar movies, and average profit by genre.

## Milestone 2
### Milestone2.ipynb & csv_processing.ipynb

Milestone2.ipynb contains the code used to download all of the data we used for training our models as well as formatting it into a csv file. csv_processing.ipynb contains code used to clean and preprocess the data, address any noticed idosyncracies, create the dummy variables for the categorical features, collapse the genres, and split the features from the genres.

## Milestone 3
### Milestone_3_v4.ipynb

This notebook contains the traditional machine learning methods we tested on this data. We split the data into train and test sets, one set drops missing values, one imputes missing values, and the others add subsequently more features to the data so we can see how performance changes as more and more features are added. We test a Naive Bayes classifier, Logistic regression, and a random forest classifier on the original data and data reduced via PCA to see if reducing the dimensions improves or worsens performance.


