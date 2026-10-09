# Movie Correlation Analysis

Exploratory data analysis on a dataset of 7,000+ movies scraped from IMDB, exploring what factors most influence a film's box office performance.

## Objectives

- Identify which numeric features (budget, votes, score, runtime) correlate most strongly with gross revenue
- Discover which production companies and genres generate the highest total gross
- Practice end-to-end EDA workflow: cleaning, transformation, visualization, and correlation analysis

## Dataset

- **Source:** [Movie Industry — Kaggle](https://www.kaggle.com/datasets/danielgrijalvas/movies/data) by Daniel Grijalvas
- **File:** `movies.csv`
- **Size:** 7,000+ movies scraped from IMDB
- **Features:** name, rating, genre, year, released, score, votes, director, writer, star, country, budget, gross, company, runtime

## Project Structure

```
Movie_Correlation/
├── movies.csv                      # Raw data downloaded from Kaggle 
├── Movie Correlation.ipynb         # Main analysis notebook
└── README.md
```

## Workflow

1. **Data Cleaning** — handle missing values, convert dtypes (`budget`, `gross`, `votes` to int64), extract release year
2. **Exploratory Analysis** — scatter plots, regression plots to visualize budget vs gross relationship
3. **Correlation Analysis** — Pearson correlation matrix on numeric features, then on all features after encoding categoricals
4. **Visualization** — heatmaps, bar charts comparing gross and votes across companies and genres

## Key Findings

- **Budget is the strongest driver of gross revenue** (r ≈ 0.74): higher investment tends to yield higher box office, although it is not guaranteed
- **Votes and gross** are also strongly correlated (r ≈ 0.61), because blockbusters naturally attract more audience engagement
- **Score (IMDb rating) barely relates to gross** (r ≈ 0.22): a well-rated film is not necessarily a commercial hit
- **Action** is the highest-grossing genre by a wide margin (~$238B total, ~2.7× Comedy)

## Business takeaway

For a studio or investor, budget and audience engagement (votes) track revenue far more closely than IMDb scores. Genre choice matters as well, because Action and Animation deliver the largest total returns.
- **Action** is the highest-grossing genre by a significant margin

## Tools & Libraries

| Library | Purpose |
|---|---|
| `pandas` | Data manipulation |
| `numpy` | Numerical operations |
| `matplotlib` | Base plotting |
| `seaborn` | Statistical visualization |

## How to Run

```bash
git clone https://github.com/mynguyen09062006-blip/Movie_Correlation.git
cd Movie_Correlation
pip install pandas numpy matplotlib seaborn
jupyter notebook "Movie Correlation.ipynb"
```
