# Movie Recommendation System

![Python](https://img.shields.io/badge/Python-3.10-blueviolet)
![Framework](https://img.shields.io/badge/Streamlit-1.15.2-red)
![API](https://img.shields.io/badge/API-TMDB-fcba03)

A Content-based movie recommendation system that utilizes content similarity to suggest similar movies to users.

Check out the live demo: [Movie Recommendation System](https://chiebuka-movie-recommender.streamlit.app/)

## Overview
The system recommends movies based on its similarity with selected movie.
Relevant content features such as genre, keywords, cast, crew and storyline are used to identify and recommend similar movies.

## Workflow
1. The datasets are extracted from [TMBD 5000 movies data](https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata) and loaded into a pandas dataframe.
2. The relevant features are selected and extracted to form a movie description.
3. The extracted text features are then vectorized into numerical features using Countvectorizer.
4. The vectors are then passed to a K Nearest Neighbour model which uses Cosine Similarity measure to rank the movies based on similarity.
5. The trained model is then deployed as a [web app] [movie](https://chiebuka-movie-recommender.streamlit.app/) for movie recommendation using Streamlit.

## How to run the project?

1. Clone this repository to your local machine with the command : `git clone https://github.com/Chiebukar/movie_recommender_system.git`
2. Install the required libraries from the [requirements.txt](https://github.com/Chiebukar/movie_recommender_system/blob/master/requirements.txt) file with the command: `pip install -r requirements.txt`
3. Open your terminal/command prompt from your project directory and run the streamlit [app.py](https://github.com/Chiebukar/movie_recommender_system/blob/master/app.py) file by running the command: `streamlit run app.py`
5. You will be redirected to the app in the localhost of your browser with the address `http://127.0.0.1:5000/`.
