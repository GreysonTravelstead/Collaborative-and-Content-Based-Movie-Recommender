# Collaborative-and-Content-Based-Movie-Recommender
Movie Recommender Using Collaborative and Content based filtering methods.


Dataset: https://ai.stanford.edu/~amaas/data/sentiment/


Introduction:

A dataset of over 40,000 movie titles was used to create a python movie recommendation tool
using both collaborative and content based filtering methods. The data contained other attributes
such as description, cast, genres, budgets, release dates, and over 100,000 ratings for the movies.
The importance of recommender systems has been growing exponentially over the years; as big
corporations such as Amazon and Netflix use these systems to recommend movies or products
based on information from every user. One of the main goals in these systems is to reduce
root-mean-square error (RMSE), which basically expresses the difference between what users
actually do and what the system predicts.

Methods:

Content Based
Import the MovieLens dataset into jupyter notebook. After importing the dataset, it is important
to pre-process the data before any models are applied. Remove stop words that would ultimately
lower the performance of the model. Next, the movie overview is the basis of the model. Using
the movie overview, a TF-IDF matrix will be created using all 40,000 movies. After creating the
matrix, using the cosine similarity is used to generate a numeric quantity that represents the
similarity between two movies. Define a recommender function that will return a list of movies
based on the similarity scores that were previously assigned. To do this: a reverse map that
matches movie titles with their indices will be needed. The list of cosine similarity scores for the
user imputed movie will be constructed within the function. Sorting of those movies will be done
in order to return the top 10 and the list will be returned.

Collaborative Based
Collaborative based filtering will be used to return a list of movies based off the predicted rating
a user would give that movie. Surprise, a python scikit, will be used for this method. Using the
dataset of ratings, cross validation will divide the rating data into five folds. The training of this
model is done on all folds except one. The final score of the model will be the average of those
five folds. Once this is done, SVD will be applied to factorize the matrix into a singular matrix
and values. RMSE and MAE measurements are used to analyze the performance of the
algorithm. Create a function that will map the predictions for each user and generate a list of
movies based on that user's top ten predicted ratings.

Future Considerations:

The content based filtering systems could be improved. Although the results of the algorithm
returned a decent list of recommended movies, there were instances that the predictions were
weak. This could be improved by factoring in other attributes such as genre, director, cast, etc.
I believe that this would improve the accuracy of the predictions by quite a lot.

In regard to the collaborative based filtering method, we are limited to predicting movies that the
user has watched or rated already. The algorithm could be improved to serve this feature. We
believe that the real solution would be to show users recommended movies that they have not
seen based on the way they rated other movies. This would be a more practical and real world
application of the model.

