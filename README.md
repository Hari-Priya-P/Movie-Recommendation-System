# Movie-Recommendation-System

Used the 'MovieLens' dataset to build movie recommendation system. Integrated the dataset with IMDB and TMDB data set publically available and Split the dataset into 80% training and 20% testing based on the User ID. Building the model included steps like data preprocessing, prediction of user ratings for movies, recommendation of movies based on the predicted ratings and evaluation of the recommendations to understand the accuracy of the system. Built the following models.
- Popularity based model
- Content based model 
- Collaborative Filtering
- Matrix Factorization method
- Combined model ( SVD + CF)
- Hybrid model

#### 1. Popularity based model
- Genre wise popular movies
- Computed on Popularity metric from TMDB data and Weighted Rating from IMDB 

#### 2. Content based model
- User profile based on item profiles : Genre and Year of release of movie
- Movie - Movie similarity

#### 3. Collaborative Filtering
Used KNN (k- nearest neighbors) algorithm with Surprise library
Variations of KNN based approaches:
- KNNBasic
- KNNwithMeans
- KNNWithZScore
- KNNBaseline : integrates the baseline average ratings

#### 4. Matrix Factorization
Matrix Factorisation algorithms using Surprise library.
- SVD : baseline estimates + latent factor predictions
- SVDpp : SVD + considers implicit ratings

#### 5. Combined Model
- Matrix Factorization + CF 
- Weighted linear combination of prediction ratings
- Combined : KNNBaseline (with pearson baseline similarity), SVDpp, SVD, BaselineOnly

#### 6. Hybrid Model
Combination of recommendations using:
- Combined model ( SVD + CF)
- Content Based Movie-Movie Similarity
- Popularity model + User Profile (Genre Based)
