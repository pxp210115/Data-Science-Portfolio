# Content Based Filtering:-

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54) ![scikit-learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white)

Content-based filtering uses item features to recommend other items similar to what the user likes, based on their previous actions or explicit feedback.

![image](https://user-images.githubusercontent.com/100412162/178734430-431306ff-4bb5-454b-9e42-c7d31d01e4a7.png)

## About the Data:-

### Ratings Data File Structure (ratings.csv)

All ratings are contained in the file `ratings.csv`. Each line of this file after the header row represents one rating of one movie by one user, and has the following format:

    userId,movieId,rating,timestamp

### Tags Data File Structure (tags.csv)

All tags are contained in the file `tags.csv`. Each line of this file after the header row represents one tag applied to one movie by one user, and has the following format:

    userId,movieId,tag,timestamp
    
### Movies Data File Structure (movies.csv)

Movie information is contained in the file `movies.csv`. Each line of this file after the header row represents one movie, and has the following format:

    movieId,title,genres

## Algorithm for Content-Filtering:-

### K-means clustering:-

![image](https://user-images.githubusercontent.com/100412162/178737094-6d02d994-fd9d-4b66-bd1b-db0882cecacf.png)

We utilize k-means clustering to find movies that are very close to each other in the 18 dimensional (genre) space. On the basis of the (k=40 chosen) clusters we are able to make predicitons of user rating on movies the user has never seen.

### Metrics:-

![image](https://user-images.githubusercontent.com/100412162/178735554-4ab83b78-829e-4f71-9e32-bf52738f646d.png)

We utilize metrics such as genre_similarity by using cosine_similiarity between genres. This includes finding the angle between movies in each genre space (18 genres) and then computing the cosine of the angle.

The mathematical equation can be expressed as:-

![image](https://user-images.githubusercontent.com/100412162/178736283-9aeee71f-255f-4088-8e82-a661e53c49a1.png)

Another metric presented above is the fact that people might like movies released in the same year as well ( Feature extracted from movie_title). This is also taken into consideration when providing recommendations as the final similarity metric is a product of the year_similarity and the genre_similarity.

### Evaluation:-

![image](https://user-images.githubusercontent.com/100412162/178828440-6ab1734a-6ad7-4a48-9e4a-960ea66b2e17.png)

We achieve the above performance metrics on content based filtering. These values have to be as close to 0 as possible. 

### Predictions:-

![image](https://user-images.githubusercontent.com/100412162/178828701-e7c74802-7d2e-4dcf-a964-e65b732a8963.png)

For a random user we make predictions on the movies the user has never seen and provide ratings to each of those. In the case of recommender systems the accuracy of the model is not important, but the relevance of the top-k recommendation is. We shall be focusing on better models which have proven to be extremely useful over time such as Collaborative Filtering on the same dataset to compare performance.












