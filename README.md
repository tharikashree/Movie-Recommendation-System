﻿# Movie-Recommendation-System

This project is a **Content-Based Filtering Movie Recommendation System** that suggests movies based on user preferences.

## Features
- **Content-Based Filtering**: Recommends movies based on similarity in content.
- **Interactive User Input**: Users can enter a movie title to get similar recommendations.
- **Lightweight & Fast**: Efficient recommendation system using a structured dataset.

## Dataset
The system utilizes `movies.csv`, which contains the following key attributes:
- `movieId`: Unique identifier for each movie
- `title`: Name of the movie
- `genres`: Genres associated with the movie

## Installation
### Prerequisites
Ensure you have **Python 3.x** installed along with the following dependencies:
```sh
pip install pandas
```

## Usage
1. **Prepare Dataset**: Place `movies.csv` in the `data` directory.
2. **Run the Script**:
   ```sh
   python main.py
   ```
3. **Enter a Movie Title**: The system will return a list of similar movies.

## Methodology
1. **Data Preprocessing**:
   - Handling missing values
   - Extracting the year from the movie title
   - Splitting genres into a list format
2. **Text Processing**:
   - Removing stop words
3. **Computing Similarity**:
   - A weighted genre-based recommendation is calculated as follows:
   
         recommendation_table_df = (movies_with_genres.dot(a_profile)) / a_profile.sum()
   This approach multiplies the genres by user preference weights and then computes the weighted average to rank movies.
4. **Recommendation Generation**:
   - Movies with the highest similarity scores are recommended.

## Example
```
Input: [
            {'title':'Predator', 'rating':4.9},
            {'title':'Final Destination', 'rating':4.9},
            {'title':'Mission Impossible', 'rating':4},
            {'title':"Beverly Hills Cop", 'rating':3},]
Output:
1                                      Rubber
2                                       Pulse
3                                   Cave, The
4                       Kaho Naa... Pyaar Hai
5                                 Future-Kill
6                                     Big Bad
7                                   Inception
```
## Future Improvements
- **Hybrid Recommendation**: Combining collaborative filtering.
- **Deep Learning Models**: Implementing neural networks for better recommendations.
- **Web Interface**: Deploying with a user-friendly UI.


