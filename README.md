#  Movie Recommendation System

A content-based movie recommendation system that suggests movies similar to a movie selected by the user. It analyzes movie overviews, genres, keywords, and cast information to identify similar movies.
# Live Link : https://movie-recommendation-jygm.onrender.com/

##  Features

- Recommends movies based on content similarity.
- Uses movie overviews, genres, keywords, and cast information.
- Processes movie metadata to create meaningful tags.
- Uses cosine similarity to find similar movies.
- Provides recommendations from a dataset of approximately 4,800 movies.

##  Tech Stack

- **Python** — Core programming language
- **Pandas** — Data processing and manipulation
- **NumPy** — Numerical operations
- **Scikit-learn** — Text vectorization and similarity calculation
- **Pickle** — Saving the processed movie data and similarity matrix

##  How It Works

1. **Data Collection:** Loads movie information from `movies.csv` and `credits.csv`.
2. **Data Preprocessing:** Extracts relevant information, including genres, keywords, cast, director, and movie overview.
3. **Feature Engineering:** Combines the selected movie attributes into a single text field called `tags`.
4. **Text Vectorization:** Uses `CountVectorizer` with a maximum of 5,000 features and English stop-word removal to convert text into numerical vectors.
5. **Similarity Calculation:** Calculates pairwise cosine similarity between movie vectors.
6. **Recommendation:** Finds the selected movie and returns the five most similar movies based on their similarity scores.

##  Project Files

- `movies.csv` — Movie metadata
- `credits.csv` — Movie cast and crew information
- `movies_list.pkl` — Serialized processed movie data
- `similarity.pkl` — Precomputed movie similarity matrix
- `app.py` — Application code, if included in the repository
- `requirements.txt` — Python dependencies, if included

##  Installation and Usage

### 1. Clone the repository

```bash
git clone https://github.com/gojoskuna/Movie-Recommendation.git
cd Movie-Recommendation
```

### 2. Create a virtual environment (optional)

```bash
python -m venv venv
```

Activate it on Windows:

```bash
venv\Scripts\activate
```

### 3. Install dependencies

```bash
pip install pandas numpy scikit-learn streamlit
```

### 4. Run the application

If the application interface is implemented in `app.py` using Streamlit, run:

```bash
streamlit run app.py
```

Make sure the required pickle files are available in the locations expected by the application.

##  Recommendation Approach

This project uses **content-based filtering** rather than collaborative filtering. Recommendations are based on similarities between movie features, not on user ratings or the behavior of other users.

The `CountVectorizer` transforms the combined text tags into numerical vectors, and cosine similarity measures how similar the movie vectors are.

##  Future Improvements

- Display movie posters and additional movie information.
- Improve text preprocessing and feature weighting.
- Add filtering by genre or release year.
- Deploy the application so users can access it online.

##  Author

Developed as a machine learning project to explore text preprocessing, feature extraction, and content-based recommendation systems.
