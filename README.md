# RECOMMENDATION-SYSTEM
# Movie Recommendation System using KNN

## Project Overview
This project is a movie recommendation system built using the k-Nearest Neighbors (KNN) algorithm and a user-item interaction matrix created with the CSR (Compressed Sparse Row) matrix format from the `scipy` library. It suggests similar movies based on user ratings.

## Dataset
The project utilizes two datasets:
1. **Ratings Dataset:** Contains user ratings for movies (userId, movieId, rating, timestamp).
2. **Movies Dataset:** Contains movie information (movieId, title, genres).

## Key Libraries Used
- pandas
- numpy
- scikit-learn
- scipy
- matplotlib
- seaborn

## Project Steps

### 1. Data Loading
- Import the ratings and movies datasets using pandas.

### 2. Data Exploration
- Display the first few rows of each dataset.
- Analyze user frequency and movie rating statistics.

### 3. Movie Statistics
- Identify the highest and lowest-rated movies.
- Use Bayesian average to handle movies with fewer ratings.

### 4. User-Item Matrix
- Create a sparse matrix (CSR matrix) representing users and their ratings for movies.

### 5. k-Nearest Neighbors (KNN) Model
- Implement the KNN algorithm using `NearestNeighbors` from scikit-learn.
- Find similar movies based on user ratings.

### 6. Recommendation
- Given a movie, recommend similar movies based on user rating patterns.

## Sample Output
For a given movie (e.g., movieId = 5), the system outputs:
```
Since you watched <Movie Title>
Recommended Movie 1 (ID: <movieId>)
Recommended Movie 2 (ID: <movieId>)
...
```

## How It Works
- User-item ratings are represented as a sparse matrix.
- KNN identifies movies with similar rating patterns.
- Recommendations are made based on the similarity of movie rating vectors.

## Key Functions
### create_matrix(df)
- Converts ratings dataframe into a sparse matrix.
- Maps userId and movieId to matrix indices.

### find_similar_movies(movie_id, X, k)
- Finds k similar movies using KNN.
- Returns a list of similar movie IDs.

## Requirements
Install the required libraries using:
```
!pip install numpy pandas scikit-learn matplotlib seaborn
```

## Usage
- Run the provided script.
- Change `movie_id` to any movie ID for personalized recommendations.

## Future Improvements
- Implement FAISS for faster similarity search.
- Incorporate movie genres and other metadata.
- Use deep learning-based embeddings for better recommendations.

## Conclusion
This project demonstrates a basic movie recommendation system using KNN and a CSR matrix. It is a simple yet effective approach to collaborative filtering-based recommendations.

