# RS-MovieLens
MovieLens Recommender: A Comparative Study of Recommendation Algorithms
Access the full project report here (Full_Report.pdf)

## Abstract

This project compares various recommender system models on the MovieLens 1M dataset. Models include Content-Based, Collaborative Filtering, Singular Value Decomposition (SVD), and Deep Learning. The Softmax Deep Neural Network performed best with the lowest Mean Square Error (MSE) on the test set.

## Table of Contents

1. [Introduction](#introduction)
2. [Dataset](#dataset)
3. [Data Visualization](#data-visualization)
4. [Recommender System Models](#recommender-system-models)
   - [Content-Based](#content-based)
   - [Collaborative Filtering](#collaborative-filtering)
   - [SVD Model](#svd-model)
   - [Deep Learning Model](#deep-learning-model)
5. [Conclusion](#conclusion)

## Introduction

This project explores various recommender system algorithms using the MovieLens 1M dataset. The goal is to compare different approaches and identify the most effective model for movie recommendations.

## Dataset

The MovieLens 1M dataset contains:
- 1,000,209 anonymous ratings (1-5) from 6,040 users on 3,900 movies
- Basic movie information (title, genre)
- Simple demographic information for users (age, gender, occupation, zip)

## Data Visualization

Key insights from data visualization:
- Most users gave 4-star ratings, followed by 3 and 5 stars
- Drama is the most common genre, followed by Comedy and Action

## Recommender System Models

### Content-Based

- Uses TF-IDF features for movie genres and titles
- Calculates cosine similarity between movies
- RMSE: 1.1277, MSE: 1.2717

### Collaborative Filtering

Four variations implemented:
1. User-Based with Cosine Similarity
2. User-Based with Pearson Similarity
3. Item-Based with Cosine Similarity
4. Item-Based with Pearson Similarity

Performance was mediocre due to data sparsity issues.

### SVD Model

- Addresses the long-tail problem
- Hyperparameters: n_factors=40, n_epochs=40, lr=0.005, reg=0.05
- RMSE: 1.3213, MSE: 1.7459

### Deep Learning Model

- Uses embedding layers for users and movies
- Two dense layers with ReLU activation
- Softmax output layer
- RMSE: 1.0151, MSE: 1.0305

## Conclusion

The Deep Neural Network model outperformed all other models, achieving the lowest MSE on the test set. This project demonstrates the importance of experimenting with various models to find the most suitable solution for specific recommendation tasks.

| Model | RMSE | MSE |
|-------|------|-----|
| Content-Based | 1.12768 | 1.27165 |
| User-Based (Cosine) | 3.49445 | 12.21119 |
| User-Based (Pearson) | 3.54791 | 12.58767 |
| Item-Based (Cosine) | 3.46470 | 12.00414 |
| Item-Based (Pearson) | 3.52966 | 12.45852 |
| SVD | 1.32133 | 1.74591 |
| DNN | 1.01514 | 1.03052 |
