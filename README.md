# Hybrid Movie Recommender System  

## Overview  
This project implements a **Hybrid Movie Recommender System** that combines:  
- **Content-Based Filtering** → Uses TF-IDF on movie metadata (title, overview, genres) to recommend movies similar to a given title.  
- **Collaborative Filtering (Simplified)** → Leverages user rating patterns to enhance recommendations.  
- **Hybrid Fusion** → Merges both signals into a single ranking score for improved recommendation quality.  

Additionally, an **interactive CLI interface** with **fuzzy string matching** allows users to search for movies even with spelling variations (e.g., *Dark Nite → The Dark Knight*).  

---

## Tech Stack  
- **Python** (core language)  
- **Pandas / NumPy** (data processing)  
- **Scikit-learn** (TF-IDF, cosine similarity)  
- **FuzzyWuzzy / RapidFuzz** (fuzzy string matching for search)  

---

## Dataset and Sources
- **MovieLens Dataset**: Provides user–movie ratings, enabling collaborative filtering.  
- **TMDb API**: Supplies additional movie metadata (title, genres, overview, release year), which powers the content-based filtering component.  

By merging these two sources, the recommender system can use both **user behavior (ratings)** and **movie features (metadata)** to deliver better recommendations. 

---

## Key Features
- **Content-based filtering** using TF-IDF on movie overviews, genres, and metadata.  
- **Collaborative filtering** using cosine similarity on rating vectors.  
- **Hybrid recommender** that combines both approaches to handle sparsity and cold-start issues.  
- **Fuzzy matching** for improved user input handling when searching for movie titles.  
- **Interactive recommender interface** to let users pick their intended movie and get recommendations (`Enter a movie title → Get recommendations`)  

---

## Example Run  

```bash
Enter a movie title (or 'quit' to stop): Oppenheimer  

Did you mean:
1. Oppenheimer (2023) [Score: 96]
2. The Oppenheim Project (2010) [Score: 78]

Enter the number of the correct movie: 1  

Showing recommendations for: Oppenheimer  

1. Schindler's List (1993) | Genres: Drama, History, War | Hybrid Score: 0.2687  
2. The Imitation Game (2014) | Genres: History, Drama, Thriller, War | Hybrid Score: 0.2567  
3. Apocalypto (2006) | Genres: Action, Drama, History | Hybrid Score: 0.2440  
