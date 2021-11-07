# Content-Based-Movie-Recommender-System-with-sentiment-analysis

Content-based methods are based on the similarity of movie attributes. Using this type of recommender system, if a user watches one movie, similar movies are recommended. For example, if a user watches a comedy movie starring Adam Sandler, the system will recommend them movies in the same genre or starring the same actor, or both. With this in mind, the input for building a content-based recommender system is movie attributes.

The details of the movies(title, genre, cast,crew, rating, etc) are fetched using Dataset of TMDB on Kaggle, 
https://www.kaggle.com/tmdb/tmdb-movie-metadata is the link where I downloaded my dataset and  performed sentiment analysis on those reviews.

# Business Problem:
Predict genres based on overview of movie and other features.

# Requirement Gatherings:

Have two csv files:
In Movies.csv has 20 fields namely: 
- budget
- homepage
- genres
- Id
- Keywords
- original_langugae
- orignal_title
- overview
- poplarity
- production_companies
- production_countries
- release date
- revenue
- runtime
- spoken_languages
- status
- tagline
- title
- vote_avergae
- vote_count

In Credits.csv, we have 4 columns:
- movie_id
- title
- cast
- crew

# Designing our Movie Recommendation System

Since out of 24 columns, we require movie_id, title, cast, crew, genres, keywords and  overview columns to build our model. Based on these details I hvae created a new dataset with only 3 columns that is: MOvie_Id, title and tags. In tags columns we will extract all the important details ( cast, crew, genres, keywords and  overview)that is require for our model.

To obtain recommendations for our users, we will predict their tags for movies they haven’t watched yet. Movies are then indexed and suggested to users based on these predicted tags. To do this, we will use past records of movies and tags to predict their future ratings

# Implementations:
For our recommender system, we'll use content-based filtering. To find the similarity between movies for our content based method, we’ll use a cosine similarity function. 

### Similarity Score :

How does it decide which item is most similar to the item user likes? Here we use the similarity scores.

It is a numerical value ranges between zero to one which helps to determine how much two items are similar to each other on a scale of zero to one. This similarity score is obtained measuring the similarity between the text details of both of the items. So, similarity score is the measure of similarity between given text details of two items. This can be done by cosine-similarity.

# How Cosine Similarity works?

Cosine similarity is a metric used to measure how similar the documents are irrespective of their size. Mathematically, it measures the cosine of the angle between two vectors projected in a multi-dimensional space. The cosine similarity is advantageous because even if the two similar documents are far apart by the Euclidean distance (due to the size of the document), chances are they may still be oriented closer together. The smaller the angle, higher the cosine similarity.

![image](https://user-images.githubusercontent.com/79011767/140651396-80524b79-4fae-4dc7-b43a-afcf768ae6e6.png)



# Tools and Libraries used
- Pytg

