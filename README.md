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
├── Movie_Correlation.ipynb         # Main analysis notebook
└── README.md
```

## Workflow

1. **Data Cleaning** — handle missing values, convert dtypes (`budget`, `gross`, `votes` to int64), extract release year
2. **Exploratory Analysis** — scatter plots, regression plots to visualize budget vs gross relationship
3. **Correlation Analysis** — Pearson correlation matrix on numeric features, then on all features after encoding categoricals
4. **Visualization** — heatmaps, bar charts comparing gross and votes across companies and genres

## Key Findings

- **Votes and gross** have the strongest correlation (~0.63) among all feature pairs — blockbusters naturally attract more ratings
- **Budget and gross** are strongly correlated (~0.74) — higher investment tends to yield higher returns, though not guaranteed
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
git clone https://github.com/yourusername/Movie_Correlation.git
cd Movie_Correlation
pip install pandas numpy matplotlib seaborn
jupyter notebook Movie_Correlation.ipynb
```
