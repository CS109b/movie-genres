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

## Milestone 4
### Milestone_04_deep_network_final.ipynb


### Milestone_4_pre-trained_network.ipynb

This notebook contains a variation on the VGG16, a pre-trained covnet included in Keras. Weights were pre-trained on ImageNet, the input was specified to the same 300x185x3 size we used in our original model, and the same binary cross-entropy loss function is used to train and evaluate performance. Fully connected layers are added at the end to specify our 7 desired output labels.

## Milestone 5

This notebook is an extension of Milestones 3 & 4, adding topic modeling variables, improving the data processing pipeline, and extending the deep learning model.

Specifically, these issues were addressed:

1. The test set must be set aside to start with, so subsequently generated training sets don't dip into it   
            
2. Implement training by "maxi-batches": 
  - set aside test
  - load one big train batch (~5k)
  - do one epoch of training
    
3. Manual image pre-processing - use scipy to load images in with uniform shape and formatting (and downsample, if desired)
        
4. Use Precision and Recall custom fcns for metrics
    
5. Save Keras model and associated metadata automatically
    
6. Log results for TensorBoard viz
    
7. Functionalize calls for model building and fitting, so we can sweep configs
