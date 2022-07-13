# User- Based Collaborative filtering:-

User-Based Collaborative Filtering is a technique used to predict the items that a user might like on the basis of ratings given to that item by the other users who have similar taste with that of the target user.

Similarity between two users can be calculated using this score:-

![image](https://user-images.githubusercontent.com/100412162/178848297-468a0e72-b18c-4186-a84c-b1b981461b0f.png)

## About the data:-

Can be seen in the link above.

## Algorithm used:-

KNNBasic is an algorithm that is directly derived from a basic nearest neighbors approach. This algotihm helps in understanding the set of users that are closest in n-dimensional space to the test_user for whom we need to predict the ratings.

We utilize the [surprise](https://surprise.readthedocs.io/en/stable/getting_started.html#basic-usage) package to get easy predictions, similary scores and simulation options.

![image](https://user-images.githubusercontent.com/100412162/178848896-423f76a6-c05d-423e-8193-cf19b3f94f9e.png)

Note 📝:- It is to be noted that we train the entire dataset as the end goal is not to make perfect predictions but to get a list of items that the user might next click/purchase.

The above picture shows the simulation options chosen were "cosine" similarity and "user_based". We then utilize the compute_similarities function to compute the similarity matrix.

The next step is to get the top-N similar users to our test subject.

![image](https://user-images.githubusercontent.com/100412162/178849295-656c9ee7-ab60-41da-9ce7-c26c5954299a.png)

The user-similarity matrix looks like the below:-

![image](https://user-images.githubusercontent.com/100412162/178849802-89ab7693-c949-4e4d-bd80-e383f50bfc63.png)

## Predictions:-

![image](https://user-images.githubusercontent.com/100412162/178849531-c6264e10-b31b-4fcb-9b6a-1183a0bed9fe.png)

We can see that the user has been recommended the above movies when he himself has rated movies like "The Heat", "The dead man walking" and "Things to do in Denver when you are dead".

## Result:-

We obtained a fast and good looking recommendation engine which proposes recommendations which are close to the genre of movies previously rated by similar users. However, actual testing of a recommendation system can be only done on customers by following A/B Testing procedures.
