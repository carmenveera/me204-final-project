# ME204 Final Project: Do Popularity and Audience Ratings Move Together Across Film Genres?

| GitHub username | LSE ID     |
| ---------------- | ---------- |
| `carmenveera`     | `250093502 ` |

## Overview

Popular films are not always the ones audiences rate best. This project asks
whether a genre's popularity and its average audience rating move together on
TMDB (The Movie Database), and whether the balance between the two has shifted
across the last five decades — using genre-level data from roughly 10,000
popular films.

## Data sources

[The Movie Database (TMDB)](https://www.themoviedb.org/documentation/api), a
public film database with a free API. Two endpoints are used:

- `/movie/popular` — the main data source, paginated (500 pages, the API's own
  limit, 20 films per page) to collect roughly 10,000 popular films with their
  popularity score, audience rating, vote count, release date, and genre ids.
- `/genre/movie/list` — a lookup table translating TMDB's numeric genre ids
  (e.g. `28`) into genre names (e.g. `"Action"`).

No supplementary static datasets are used; every row in the processed tables
traces back to one of these two API calls.

## How to reproduce

**Python packages:** `pandas`, `plotly`, `requests`, `python-dotenv`, `kaleido`.
Install with:
```bash
pip install pandas plotly requests python-dotenv kaleido==0.2.1
```

**Credentials.** You need a free TMDB API key:
1. Create an account at [themoviedb.org](https://www.themoviedb.org/) and
   request an API key under Settings → API.
2. Copy `.env.example` to `.env` and paste your key: API_KEY=
   `.env` is git-ignored — never commit your real key.

**Run order.** Run the three notebooks in order; each depends on the output of
the one before.

| # | Notebook | Reads | Does | Writes |
|---|---|---|---|---|
| 1 | `NB01-Data-Collection.ipynb` | TMDB API (`/movie/popular`, `/genre/movie/list`) | Paginates through 500 pages of popular films (10,000 films) and downloads the genre lookup table; checks the collection for duplicates and record count | `data/raw/movies.json`, `data/raw/genres.json` |
| 2 | `NB02-Data-Transformation.ipynb` | `data/raw/movies.json`, `data/raw/genres.json` | Flattens the raw JSON into one row per film; drops duplicate film ids, films with no usable release date, and films below the 25th percentile of `vote_count` (removes low-vote films whose average rating is statistically unstable); extracts `release_year` and `decade`; explodes and merges genre ids into genre names | `data/processed/movies.csv`, `data/processed/genres.csv`, `data/processed/movies_with_genres.csv` |
| 3 | `NB03-Data-Analysis.ipynb` | `data/processed/*.csv` | Groups by genre and by genre-decade to compute average popularity, average audience rating, and genre share over time; produces three charts | `docs/charts/finding1_average_popularity_by_genre.html`, `docs/charts/finding2_popularityvsvote_by_decade.html`, `docs/charts/finding3_genre_share_by_decade.html` |

