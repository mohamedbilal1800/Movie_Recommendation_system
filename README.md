# Movie Recommendation System

A content-based movie recommendation system that suggests movies based on user preferences, combining content and popularity-based filtering. This project uses various movie metadata features—such as genres, keywords, overview, tagline, cast, and director—to compute similarities and provide personalized recommendations.

## Features

- **Recommendation Methodology**: Combines content-based filtering with a popularity-based boost for more effective recommendations.
- **Similarity Metric**: Uses cosine similarity on TF-IDF vectors of selected features to assess movie similarity.
- **User Input Matching**: Allows for approximate matching of user input to movie titles, making it user-friendly.
- **Key Attributes**:
  - Genres
  - Keywords
  - Overview
  - Tagline
  - Cast
  - Director

## Dataset

The system operates on a dataset of movies, which includes the necessary attributes for recommendation. Ensure that the dataset is available in CSV format and includes columns for each of the following:
- **Genres**
- **Keywords**
- **Overview**
- **Tagline**
- **Cast**
- **Director**

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/username/movie-recommendation-system.git
   cd movie-recommendation-system
   ```

2. Install the required Python packages:
   ```bash
   pip install -r requirements.txt
   ```

3. Place the dataset file (e.g., `movies.csv`) in the project directory.

## Usage

Run the Jupyter notebook to interactively use the recommendation system or deploy it as a web app using Streamlit.

### Running the Notebook

1. Open Jupyter Notebook:
   ```bash
   jupyter notebook movie_recommendation_project.ipynb
   ```
2. Follow the instructions within the notebook to generate recommendations based on user input.

### Running as a Web App

You can also convert this system into a web application using Streamlit:
   ```bash
   streamlit run app.py
   ```

## Methodology

1. **Data Preprocessing**: Loads and preprocesses movie data by handling missing values, formatting text features, and merging metadata into a combined text field for similarity calculation.
2. **Feature Extraction**:
   - Uses TF-IDF vectorization on features like genres, keywords, and overview.
3. **Similarity Calculation**:
   - Computes cosine similarity between the TF-IDF vectors of the selected movie and all other movies in the dataset.
4. **Recommendation Generation**:
   - Sorts movies based on similarity scores and provides a list of the top N most similar movies.

## Example

If the user inputs `The Matrix` as a favorite movie, the system will output a list of similar movies based on both the content and popularity features selected.

## Libraries Used

- **Numpy**: For numerical operations.
- **Pandas**: For data manipulation.
- **Scikit-learn**: For TF-IDF vectorization and cosine similarity calculations.
- **Difflib**: For approximate movie title matching to enhance user experience.
