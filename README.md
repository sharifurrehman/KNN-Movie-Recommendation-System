# KNN-Based Movie Recommendation System

## Project Overview

The **KNN-Based Movie Recommendation System** is a machine learning project that recommends movies based on genre similarity. It uses the K-Nearest Neighbors (KNN) algorithm to identify movies with similar genre profiles and return relevant recommendations for a selected movie.

The project uses the MovieLens Latest Small dataset and demonstrates how feature engineering and nearest-neighbor search can be applied to a real-world recommendation task.

## Objectives

- Understand and implement the K-Nearest Neighbors algorithm.
- Explore and preprocess movie metadata.
- Convert movie genres into numerical features.
- Calculate movie similarity using cosine distance.
- Build a reusable movie recommendation function.
- Visualize genre distributions and validate the recommendation workflow.

## Dataset

**Source:** [MovieLens Latest Small Dataset](https://grouplens.org/datasets/movielens/)

The dataset includes movie metadata and user ratings.

This implementation uses `movies.csv`, which contains movie IDs, titles, and genre labels. The dataset contains approximately 9,742 movies and 19 genre categories, plus an entry for movies with no listed genres.

The notebook downloads and extracts the dataset automatically.

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- Google Colab
- Jupyter Notebook

## Machine Learning Approach

### 1. Data Loading and Preprocessing

The notebook downloads the dataset, loads movie metadata, checks missing values and duplicates, and separates genre labels.

### 2. Feature Engineering

Movie genres are transformed into binary feature vectors using `MultiLabelBinarizer`.

Each vector represents the genres associated with a movie.

### 3. KNN Model

The model uses Scikit-learn's `NearestNeighbors` with cosine distance to find movies whose genre vectors are closest to the selected movie.

### 4. Recommendations

The `recommend_movies()` function accepts a movie title and a requested number of recommendations. It returns similar movie titles, their genres, and a similarity percentage derived from cosine distance.

### 5. Visualization and Validation

The notebook visualizes the most common genres and performs basic checks on the feature matrix and recommendation function.

## How to Run

1. Open the notebook in Google Colab.
2. Run the notebook cells in order.
3. Allow the dataset to download automatically.
4. Train the KNN nearest-neighbor model.
5. Call the recommendation function with a movie title.

Example:

```python
recommend_movies("Toy Story (1995)", n_recommendations=10)
```

## Project Structure

```text
KNN-Movie-Recommendation-System/
├── KNN_Movie_Recommendation_System.ipynb
├── README.md
└── requirements.txt
```

## Limitations

- Recommendations are based on genre similarity, not individual user preferences.
- The current implementation does not use user ratings to personalize recommendations.
- Movies with identical or overlapping genres may receive high similarity scores even when their stories are different.
- Similarity percentages indicate feature similarity, not predicted user satisfaction.
- Recommendation quality has not been established through a formal offline evaluation.

## Future Improvements

- Incorporate movie tags, descriptions, and other metadata.
- Develop a collaborative filtering approach using user ratings.
- Compare different similarity metrics and recommendation strategies.
- Evaluate recommendation quality using suitable offline metrics.
- Build an interactive interface using Streamlit.

## Learning Outcomes

This project demonstrates practical experience with feature engineering, data preprocessing, the KNN algorithm, cosine distance, recommendation logic, data visualization, and basic software validation.

bution.
