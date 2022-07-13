# Recommender Systems Notes:-



## Collaborative Filtering

It is the art of recommending things that other people/ items of similar interests/ neighbourhood. We generally use top-N system architectures to deal with the problem.

The architecture is as follows:-

![image](https://user-images.githubusercontent.com/100412162/178832695-f23ecbbf-7dfb-4fbd-967e-2120c6fa5760.png)

Steps in the architecture:-

1) Collect user data with explicit/implicit ratings.
2) We then generate candidates for recommendation by looking up items which the user liked.
3) Score and rank the candidates
4) Filter 
5) Produce the top-n recommendation list

The different ways to measure similarity between people/ things:-

1) Cosine similarity - 

2) Adjust Cosine:-

3) Pearson similarity



## a) User-based collaborative filtering:-

The steps in building a user-based collaborative filtering matrix are:-
1) user-> item rating matrix
2) user-> user similarity matrix
3) look up similar users
4) Candidate generation
5) Candidate scoring
6) Candidate Filtering

![image](https://user-images.githubusercontent.com/100412162/178842399-ea9c63a1-e5ab-4558-8d39-ed00b6a541c7.png)

In the above picture we have three users with 4 movies in the matrix. We can suggest that Bob and Ann both like the Star wars movie, hence one should recommend recommend the second part of the movie which Ann saw to Bob as well.

If we try to create clusters/neighbors who are similar to each other then, we end up creating a user similarity matrix like the one below:-

![image](https://user-images.githubusercontent.com/100412162/178842712-b15cfacd-4fa1-4bd4-a283-a3255367440d.png)

This suggests that if both Ann and Bob are similar their similarity scores are as above.

Note 📝:- Sometimes the data is extremely sparse, hence it can be a very tedious task. We then have to put a min threshold of ratings/person on whom the similarity metric is then computed.

After creating the top-n users who are similar to Bob, we then score then
