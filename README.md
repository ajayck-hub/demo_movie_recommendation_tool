# Demo Movie Recommendation Tool

This is a demonstration of a Content-Based Movie Recommendation System built with Python, Pandas, and Scikit-Learn. The system suggests movies by analyzing the similarity between their genres.

## Features

- **TF-IDF Vectorization**: Transforms textual movie genres into a quantitative TF-IDF feature matrix.
- **Cosine Similarity**: Calculates pairwise similarity scores to match movies that share identical or related genres.
- **Dynamic Recommendations**: Provides a flexible function that accepts a movie title and outputs the top N most similar movies from the dataset.

## How It Works

1. A dataset containing movie titles and their corresponding genres is read into a Pandas DataFrame.
2. The genres are converted into vectors using a Term Frequency-Inverse Document Frequency (TF-IDF) feature extractor (ignoring basic stop words in English).
3. We compute a matrix of Cosine Similarities between all resulting vector pairs.
4. When prompted with a known movie title, the tool returns a list of other titles prioritized by their similarity score against the target movie.

## Setup

Make sure you have a Python environment, then install the provided dependencies:

```bash
pip install -r requirements.txt
```

## Running the Application

Just execute the basic script directly:

```bash
python movie_recommendation.py
```

### Example Usage

If you search for recommendations similar to `'The Matrix'`, the script evaluates its similarity to other movies based on their genres and returns the best matches (e.g. `'The Dark Knight'` and `'John Wick'`).
