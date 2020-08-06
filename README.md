![new](https://user-images.githubusercontent.com/61956315/89567159-32f08300-d7ef-11ea-8689-e7ea54973ffe.png)

# Netflix-Recommender-System
## Introduction to the data set
The Netflix Movie Recommender System is based on the 'Netflix Prize data' project hosted by Netflix. It contains information on the movie ratings such as MovieID, CustomerID, Rating, Date, Name and YearOfRelease. 

## Objective

The goal of this project is to predict user ratings for films.

## Overview

User rating prediction has been done on a subset of the data for ease of computation. An exploratory data analysis was performed to understand the variable relationships and their distribution. A Collaborative Filtering recommender system was built to predict user ratings. This recommender system produces recommendations based on the knowledge of users’ attitude to items, that is it uses the ***"wisdom of the crowd"*** to recommend items. It can be divided in the following manner:

- **Memory-Based CF** - It utilizes the entire user-item database to generate predictions and can be further divided into two sections
    - **Item-Item CF** - “Users who liked this item also liked …”
    - **User-Item CF** - “Users who are similar to you also liked …”
    
- **Model-Based CF** - It provides item recommendation by first developing a model of user ratings.

Cosine Similarity is calculated using the pairwise distance function of sklearn for predicting similarity between users. The model is evaluated using the RMSE metric using mean_squared_error function from sklearn. 

The Model-Based CF is based ***Matrix Factorization (MF)*** that deals better with sparse matrices. It has the ability to learn from known user ratings to predict latent preferences of users with unknown ratings. ***Singular Value Decomposition***, also popularly known as **SVD**, was used as a Matrix Factorization method and can better address a cold-start problem than Memory-based recommenders. A cold-start problem is defined as a situation when a new user has little to no history of ratings or preferences.

## Dependencies

To use the Netflix Recommender System.ipynb, we need the following:

- Numpy
- Pandas
- Matplotlib
- Seaborn
- Scipy
