# Movie Correlation Analysis

## What this project does

This project uses a dataset of 7,000+ movies scraped from IMDb to find which factors are most related to a film's box office revenue (gross). It is an end-to-end EDA in Python: cleaning, visualisation and correlation analysis.

## Why it is useful

For a studio or investor, it is helpful to know which factors actually move with revenue before deciding where to spend. Main findings:

- **Budget** has the strongest relationship with gross revenue (r ≈ 0.74).
- **Votes** (audience engagement) is also strongly related (r ≈ 0.61).
- **IMDb score** is only weakly related to gross (r ≈ 0.22), so a well-rated film is not necessarily a commercial hit.
- **Action** is the highest-grossing genre by a wide margin, followed by Comedy and Animation.

## How I processed the data

**1. Loading and checking**
- Loaded `movies.csv` with pandas and checked the percentage of missing values in each column. Most missing values were in `budget` (~28%) and `gross`.

**2. Cleaning**
- Dropped rows with missing values so that every movie has a budget and a gross.
- Converted `budget`, `gross` and `votes` from float to int64.
- The `year` column did not always match the actual release date, so I extracted the year from the `released` column with a regex (`correctyear`).
- Sorted the data by `gross` to see the top-earning films.

**3. Exploratory analysis**
- Scatter plot and regression plot of budget vs gross.
- Bar charts of the top 7 companies and top 7 genres by total gross, and a comparison of gross and votes by genre.

**4. Correlation analysis**
- Pearson correlation matrix of the numeric columns, shown as a heatmap.
- Converted text columns (genre, company, director, etc.) to category codes so they could be included in the correlation matrix.
- Unstacked the matrix into feature pairs, sorted them, and filtered pairs with correlation above 0.5.

## Getting started

1. Clone the repository:
   ```bash
   git clone https://github.com/mynguyen09062006-blip/Movie_Correlation.git
   cd Movie_Correlation
   ```
2. Install the libraries:
   ```bash
   pip install pandas numpy matplotlib seaborn jupyter
   ```
3. Open `Movie Correlation.ipynb` and choose **Run All**. The data file `movies.csv` is already included ([source: Kaggle](https://www.kaggle.com/datasets/danielgrijalvas/movies/data)).

## Getting help

If you have a question or find a problem, please open an issue in this repository or contact me on [LinkedIn](https://www.linkedin.com/in/my-nguyen-anh/) or at mynguyen09062006@gmail.com.
