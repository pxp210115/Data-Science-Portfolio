# Item-based collaborative filtering

item-to-item collaborative filtering matches each of the user’s purchased and rated items to similar items, then combines those similar items into a recommendation list. 

The item to item similarity matrix is much smaller than computing the user to user similarities. The data tends to be stationary in nature i.e does not change over time like how a users interests change.

eg:- A book will always remain a book, will have the inherent qualities of a book and will share almost similar properties with other books in the market.

![image](https://user-images.githubusercontent.com/100412162/178854282-391268a8-a678-4701-aad6-c26d83d7215c.png)

The above image shows that we reciprocate the matrix used for User-based collaborative filtering. Now, we use the ratings that users have provided to the various movies to compute similarity scores between items.

It is important that we create the item similarity scores based on the common users who have seen both the items.

![image](https://user-images.githubusercontent.com/100412162/178855966-4b86a37f-7ed9-4e27-807c-62a5aeeda24f.png)

## About the data:-

See the link for data description.

## Algorithm used:-

We utilize the same algorithm that was utilized for User-based collaborative filtering i.e KNN approach. However in this case we shall change the simualtion options of the KNNBasic model from Surprise library.

