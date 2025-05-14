# TMDB Movie Insights 

This project analyzes trends in movie popularity, revenue, and genre performance using the TMDB 5000 Movie Dataset. Using Python-based data analysis tools, we explore key factors that contribute to a movie's success including genre, budget, and audience ratings.

## Dataset

- **Source:** [Kaggle - TMDB 5000 Movie Dataset](https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata)
- `tmdb_5000_movies.csv`: Metadata for 5000 movies (genre, budget, revenue, popularity, etc.)
- `tmdb_5000_credits.csv`: Information on cast and crew

## Research Questions

1. Which movie genres are most successful in terms of popularity and revenue?
2. How do movie budgets correlate with financial performance (revenue)?
3. What trends exist in movie ratings over time?

## Technologies Used

- **Python 3**
- **Pandas** – for data cleaning and manipulation
- **Matplotlib & Seaborn** – for visualization
- **Jupyter Notebook** – for EDA and reporting

## Data Preprocessing

- Merged datasets on `id` and `movie_id`
- Converted stringified JSON columns (e.g., genres) to dictionaries
- Removed movies with zero or missing budget/revenue
- Extracted the primary genre
- Converted `release_date` to datetime and extracted year

## Key Findings

| Hypothesis | Statement | Outcome | Justification |
|-----------|-----------|---------|----------------|
| H1 | Action and Adventure genres generate the most revenue | ✅ Supported | These genres dominate in total revenue |
| H2 | Higher budgets lead to higher revenue | ✅ Supported | Pearson correlation r ≈ 0.73 |
| H3 | Movie ratings have improved over time | ❌ Not Supported | Slight decline observed since 2000s |

### Genre Analysis
- **Drama** and **Comedy** are the most frequently produced.
- **Action** and **Adventure** generate the highest revenue despite being produced less often.

### Budget vs Revenue
- Strong positive correlation (r ≈ 0.73).
- Outliers exist (e.g., low-budget hits or high-budget flops).

### Ratings Over Time
- Slight downward trend in average movie ratings over time (slope ≈ -0.013).


## Future Work

- Analyze the impact of **star power** (top actors/directors)
- Include **marketing budgets** if data available
- Compare **streaming vs theatrical** success
- Evaluate **multi-genre effects**
- Build **predictive models** for box office performance


## Acknowledgements

- [Kaggle TMDB Dataset](https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata)
- [Pandas Documentation](https://pandas.pydata.org/docs/)
- [Seaborn Documentation](https://seaborn.pydata.org/)
- [The Movie Database (TMDB)](https://www.themoviedb.org/)
