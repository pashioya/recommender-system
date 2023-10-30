# Recommender System

A **Recommender System (RS)** is a system that recommends items to users based on their preferences. It is a type of information filtering system that seeks to predict the "rating" or "preference" that a user would give to an item. Recommender systems are utilized in a variety of areas including movies, music, news, books, research articles, search queries, social tags, and products in general. They are mostly known for their use in commercial applications, such as Amazon, Netflix, and YouTube.

There are two main types of recommender systems: **content-based** and **collaborative filtering**. More on this below.

## Assignment

You can decide either to implement a content-based or collaborative filtering recommender system. Please note that for a collaborative filtering recommender system, you will need to use a dataset that has user-item ratings. For a content-based recommender system, you will need to use a dataset that has item features.

## Dataset

You will need to pick a new dataset for this assignment. See the Datasets section for some suggestions, but first read on before choosing a dataset because there are some requirements that the dataset must meet depending on the type of recommender system you want to implement.

### Content-based RS

A content-based filtering algorithm is a type of recommender system that uses the description of the items and a profile of the user's interests to recommend items to the user. The algorithm is based on the assumption that if a user liked an item in the past, the user will like a similar item in the future.

The crux of the content-based filtering algorithm is the similarity function. The similarity function is used to measure the similarity between two items. The similarity function is used to find the items that are most similar to the items that the user has liked in the past. The items that are most similar to the items that the user has liked in the past are recommended to the user. The algorithm predicts that a user will like an item if the item is similar to items that the user liked in the past.

**Base your own solution on the notebook we provided in the course material and apply it to your dataset.**

### Collaborative Filtering RS

A collaborative filtering algorithm is a type of recommender system that uses the collective behavior of a group of users to recommend items to a new user. The algorithm is based on the assumption that users who agree in their evaluation of certain items in the past will agree again in the future.

The crux of the collaborative filtering algorithm is also a similarity function. The similarity function is used to measure the similarity between two users. The similarity function is used to find the users that are most similar to the user that is being recommended to. The users that are most similar to the user that is being recommended to are used to find the items that the user liked in the past. The items that the user liked in the past are recommended to the user. The algorithm predicts that a user will like an item if similar users liked the item.

**Base your own solution on the notebook we provided in the course material and apply it to your dataset.**

## Evaluation

During the exam period, you will be asked to present your recommender system to the teaching staff. You should be able to explain the algorithm you used, the dataset you used, and the results you obtained. You will also be asked to answer questions about your implementation.

## Submission

Create a `requirements.txt` file from your virtual environment and add the dependencies to it. Do this with `pip freeze > requirements.txt` in a terminal in PyCharm.

Create a zip file of your project and submit it to Canvas. Don't include the virtual environment in the zip file. The instructor will create a virtual environment and install the dependencies from your `requirements.txt` file using `pip install -r requirements.txt`.

## Datasets

When choosing a dataset, make sure it contains ratings. Look at the [MovieLens dataset](Links to an external site.) that we have used in the example notebooks. It consists of multiple files: a metadata file and a ratings file.

The metadata file contains the information about the items, and the ratings file contains the ratings of the items by the users. You can use the metadata file to create a content-based recommender system, and you can use the ratings file to create a collaborative filtering recommender system. So, depending on the type of recommender system you want to build, you should go for something similar to either the `movies_metadata.csv` or the `ratings_small.csv` file in terms of content.

Some datasets mentioned below are huge. When prototyping your models, it's best to use only a small subset of the data. You can use the `sample` method of a Pandas DataFrame to get a random sample of the data. Also, keep in mind that most datasets also require some data preprocessing.
