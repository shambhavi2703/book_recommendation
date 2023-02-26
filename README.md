# book_recommendation
The book recommendation system is designed to suggest books to users based on their age, average rating of books, collaborative filtering, and nearest neighbor algorithms. The system uses the age and average rating of books to recommend books to users that fit their age group and preferred rating range.

## STEPS TO FOLOW TO MAKE YOUR OWN BOOK_RECOMENDATION SYSTEM PROJECT 

## STEP 1 DOWNLOAD THE DATASET 

To use the BX dataset for this project, follow these steps:

The dataset used in this project can be downloaded from [here](http://www2.informatik.uni-freiburg.de/~cziegler/BX/).


1. Click on each of the following links to download the dataset files:

BX-Books.csv
BX-Book-Ratings.csv
BX-Users.csv

2. Save the files in a folder on your local machine.

Note: These files are provided for research purposes only. Please refer to the website for any additional information or usage guidelines.


## Step 2: open a Python compliler
Create a new Python script in your preferred Python environment (e.g. Anaconda, Spyder, IDLE, Visual Studio Code).

## Step 3: Import necessary libraries
In order to run the code successfully, we need to import some necessary libraries. These libraries are:

1. NumPy: a library for the Python programming language, adding support for large, multi-dimensional arrays and matrices, along with a large collection of high-level 2. mathematical functions to operate on these arrays.
3. Pandas: a software library written for data manipulation and analysis. In particular, it offers data structures and operations for manipulating numerical tables and time series.
4. Seaborn: a Python data visualization library based on matplotlib. It provides a high-level interface for drawing attractive and informative statistical graphics.
6. Matplotlib: a comprehensive library for creating static, animated, and interactive visualizations in Python.
7. Warnings: a module that implements a simple filter to suppress specific warnings.


#### incase libarary not found
Note: If any of these libraries are not installed on your system, you can use pip to install them. For example, if you need to install seaborn, you can run pip install seaborn in your command prompt or terminal.

## Step 4: Load the data
Load the data from the dataset files (BX-Books.csv, BX-Book-Ratings.csv, BX-Users.csv) into the Jupyter Notebook using pandas.

## Step 5: Data preprocessing
Clean and preprocess the data to ensure that it is ready for analysis. This may involve removing missing values, handling categorical variables, and feature engineering.

## Step 6: Perform exploratory data analysis
Perform exploratory data analysis (EDA) to gain insight into the dataset, including identifying any missing or erroneous data, and visualizing the data.

## Step 7: Build the recommendation system
Build the recommendation system. This may involve collaborative filtering, content-based filtering, or a hybrid approach.


# MODELS USED
## Average Weighted Ratings
1. The average weighted method is a popular technique used in recommendation systems to suggest items to users based on their preferences and ratings.
2. It is a hybrid method that combines the average rating of an item with the total number of ratings it has received.
3. The goal is to provide more accurate recommendations by taking into account both the quality and popularity of an item.
4. To calculate the weighted average, the number of ratings for an item is multiplied by its average rating and divided by the total number of ratings across all      items.
5. The resulting score is used to rank the items and suggest the top choices to the user.
6.This method is particularly useful when dealing with large datasets where popular items may have many ratings and less popular items may have fewer ratings.


#### References:
Su, X., & Khoshgoftaar, T. M. (2009). A survey of collaborative filtering techniques. Advances in artificial intelligence, 2009, 1-19. https://doi.org/10.1155/2009/421425
Sarwar, B., Karypis, G., Konstan, J., & Riedl, J. (2001). Item-based collaborative filtering recommendation algorithms. In Proceedings of the 10th international conference on World Wide Web (pp. 285-295). https://doi.org/10.1145/371920.372071





## Collaborative Filtering 
It is a type of recommendation system that predicts a user's preferences by analyzing their past behaviors and the behavior of other users who have similar preferences.
The code provided in the question implements a Collaborative Filtering recommendation system using cosine similarity.


Here are the key points of the Collaborative Filtering code:
1. The dataset used is a book ratings dataset, which contains information about books, users, and ratings.
2.The first step is to set a popularity threshold to filter out books with very few ratings. In this code, the threshold is set to 50 ratings per book.
3.A new dataframe is created that contains only popular books and their ratings.
4.The book ratings are then transformed into a list of dictionaries, where each dictionary represents a book and its ratings given by different users.
5.The DictVectorizer class from scikit-learn is used to convert the list of dictionaries into a sparse matrix.
6.Cosine similarity is calculated between the books using the pairwise_similarity() function from scikit-learn's metrics module.
7.A function called getTopRecommendations() is defined to recommend books to the user based on the input book.
8.The function takes the book's ISBN as input and returns a list of recommended books.
9. The recommended books are determined by finding the books that are most similar to the input book, based on cosine similarity.

#### References:
"Collaborative Filtering" on Wikipedia: https://en.wikipedia.org/wiki/Collaborative_filtering
"scikit-learn DictVectorizer" documentation: https://scikit-learn.org/stable/modules/generated/sklearn.feature_extraction.DictVectorizer.html
"scikit-learn pairwise_similarity" documentation: https://scikit-learn.org/stable/modules/generated/sklearn.metrics.pairwise.cosine_similarity.html

## Nearest Neighbour Based

1. Nearest neighbor is a popular technique used in recommendation systems to identify similar items or users.
2. It uses the concept of distance (usually cosine similarity) to find the nearest neighbors.
3. Once the nearest neighbors are identified, the system can recommend items based on what similar users have liked or what similar items have been liked by the user.
4. Nearest neighbor algorithms can be implemented using different approaches, such as k-nearest neighbor, collaborative filtering, or content-based filtering.

#### References:

Al-Hasan, M., & Shamma, R. (2014). A survey of neighbor selection techniques in collaborative filtering systems. Knowledge-Based Systems, 69, 77-86. https://doi.org/10.1016/j.knosys.2014.06.015
Ekstrand, M. D., Riedl, J. T., & Konstan, J. A. (2011). Collaborative filtering recommender systems. Foundations and Trends® in Human-Computer Interaction, 4(2), 81-173. https://doi.org/10.1561/1100000009
