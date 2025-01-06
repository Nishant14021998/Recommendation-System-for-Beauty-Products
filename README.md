# Recommendation-System-for-Beauty-Products

## Project Overview
This project implements a Recommendation System for Amazon Beauty Products using collaborative filtering techniques. The system suggests products to users based on their historical reviews and ratings. It uses the **Surprise** library to build models like **SVD (Singular Value Decomposition)** and **SVD++** for predicting ratings and recommending products.

## Team Members
- **Nishant Pandey** (Team Leader)
- **Ayush Chakraborty**
- **Abhishek Sahoo**
- **Vikram Pathak**
- **Yash Joglekar**

## Objective
The objective of this project is to build a recommendation system that predicts user ratings for Amazon beauty products. The model is evaluated using **RMSE (Root Mean Squared Error)**, which measures the accuracy of the predicted ratings compared to the actual ratings given by users.

## Technologies Used
- Python 3.x
- Surprise library for collaborative filtering models
- pandas for data manipulation
- NumPy for numerical calculations
- matplotlib for visualizations

## Dataset
The dataset used is a subset of **Amazon Product Review Data**, specifically the "5-core" dataset for beauty products. The dataset consists of reviews, ratings, and metadata for Amazon beauty products.

### Key Attributes:
- **reviewerID**: A unique identifier for each user.
- **asin**: A unique identifier for each product.
- **overall**: The rating given by the reviewer (ranging from 1 to 5).
- **reviewText**: The content of the review (not used in this project).

Dataset Link: [Amazon Review Data](https://cseweb.ucsd.edu/~jmcauley/datasets.html#amazon_reviews)

## Methodology

### Collaborative Filtering
Collaborative filtering is used to predict the ratings for products that a user has not interacted with, based on the ratings of similar users. We implement two types of collaborative filtering:
- **User-based Collaborative Filtering**: Recommends products based on the preferences of similar users.
- **Item-based Collaborative Filtering**: Recommends products similar to those a user has rated highly.

### Matrix Factorization
Matrix factorization methods such as **SVD (Singular Value Decomposition)** and **SVD++** were used to predict user ratings for items. These methods break down the user-item interaction matrix into smaller matrices, which help uncover hidden patterns in user behavior.

## Model Performance
After training, the models were evaluated using **RMSE (Root Mean Squared Error)**. The models tested were:

- **SVD**: RMSE = 1.0820
- **SVD++**: RMSE = 1.0880
- **BaselineOnly**: RMSE = 1.0890
- **NormalPredictor**: RMSE = 1.4988

The **SVD** model performed the best, achieving the lowest RMSE.

## Conclusion
The project successfully developed a recommendation system using collaborative filtering techniques to recommend beauty products on Amazon. The **SVD** model performed the best with the lowest RMSE, indicating high accuracy.

### Future Work
Future work can focus on integrating:
- Content-based filtering
- Deep learning approaches to further improve recommendation quality.

## References
1. Surprise Library Documentation: [https://surprise.readthedocs.io/en/stable/](https://surprise.readthedocs.io/en/stable/)
2. Amazon Review Dataset: [https://cseweb.ucsd.edu/~jmcauley/datasets.html#amazon_reviews](https://cseweb.ucsd.edu/~jmcauley/datasets.html#amazon_reviews)
3. Collaborative Filtering: A Review and New Directions by Yehuda Koren, Robert Bell, Chris Volinsky, IEEE Computer Society.
