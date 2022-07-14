# Item-based collaborative filtering

Item-to-item collaborative filtering matches each of the user’s purchased and rated items to similar items, then combines those similar items into a recommendation list. 

The item to item similarity matrix is much smaller than computing the user to user similarities. The data tends to be stationary in nature i.e does not change over time like how a users interests change.

eg:- A book will always remain a book, will have the inherent qualities of a book and will share almost similar properties with other books in the market.

We reciprocate the matrix used for User-based collaborative filtering for item-based. Now, we use the ratings that users have provided to the various movies to compute similarity scores between items.

It is important that we create the item similarity scores based on the common users who have seen both the items.

## [About the data](https://github.com/pxp210115/Data-Science-Portfolio/blob/rev_2/Content_based_filtering/README.MD):-

See data description in the link above.

## Algorithm used:-

We utilize the same algorithm that was utilized for User-based collaborative filtering i.e KNN approach. However in this case we shall change the simualtion options of the KNNBasic model from Surprise library.

![image](https://user-images.githubusercontent.com/100412162/179091196-deb35c65-d0d2-4bd4-b7c3-6ec3c5b16bad.png)

We utilize the compute_similarities() provided by "Surprise" package to create the item based similarity matrix.

Getting similar items to the stuff the test user liked ( weighted by rating).

![image](https://user-images.githubusercontent.com/100412162/179091511-3b69e6b5-618c-4b8d-8850-b4247d371faf.png)

We then use the below code to generate top 10 items from similar users.

![image](https://user-images.githubusercontent.com/100412162/179091680-f630af07-30b5-430f-bad3-e165cdde39fc.png)

Another use case can be getting item based recommendation which aggregate > 4.0 in ratings. We slightly modify the code by changing the heapq.nlargest to the below mentioned code:-

![image](https://user-images.githubusercontent.com/100412162/179096616-9418dadf-5b5e-4f2e-bee4-f15411989a20.png)

## Predictions:-

![image](https://user-images.githubusercontent.com/100412162/179091855-bbfdb78e-f67a-44aa-b052-f7e6811ac7e3.png)

We generate the list of items that are similar to the items the user has previously rated. These are ordered in their nature and look towards a greater number of clicks.

When we consider the alternate case of getting only items > 4.0 ratings.

![image](https://user-images.githubusercontent.com/100412162/179096788-0aeef437-8f8a-43b5-8323-788339f8e7a1.png)

We can see that there are some significant changes to the recommendations made. This can only be tested out by A/B Testing as to which model recommendations are better.

## Result:-

We achieve a model that is able to predict movies on the basis of similar users and their previously predicted data.


