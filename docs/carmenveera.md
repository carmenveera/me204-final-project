## Final project
# Do Popularity and Critical Acclaim Move Together Across Film Genres?

**Author:** carmenveera

Movies are often assumed to be popular *because* they're good — but is that really true? Using data from The Movie Database (TMDB), I looked at how genre, audience popularity, and critical rating relate to each other, and how genre trends have shifted over the decades.

## Finding 1: Sci-Fi and Adventure draw far more attention than Drama — despite being rarer

<iframe src="charts/finding1_average_popularity_by_genre.html" width="100%" height="450" style="border:none;"></iframe>

Science Fiction has the highest average popularity score (14.13), followed by Adventure (13.24) and Fantasy (12.32). Drama, despite being the most common genre in the dataset (3,041 movies), has one of the lowest average popularity scores (7.51). How often a genre appears has little to do with how much attention it draws.

## Finding 2: Popularity and critical rating don't move together

<iframe src="charts/finding2_popularityvsvote_by_decade.html" width="100%" height="450" style="border:none;"></iframe>

Animation has the highest average critical rating (7.14) despite only moderate popularity, while Science Fiction and Adventure — the two most popular genres — sit in the middle of the rating range (6.63 and 6.71). Horror stands out as the clearest mismatch: fairly popular (9.78) but the lowest-rated major genre (6.24).

## Finding 3: Action-oriented genres are steadily displacing Drama

<iframe src="charts/finding3_genre_share_by_decade.html" width="100%" height="450" style="border:none;"></iframe>

Drama's share of top films has fallen from 37.2% of top films in the 1970s to 24.9% in the 2020s. Action has more than doubled its share over the same period (9.7% → 18.5%), and Thriller shows a similar rise (12.5% → 18.6%). Comedy has also declined somewhat (23.6% → 18.1%), while Adventure and Romance stayed comparatively flat.

## Limitations

This analysis is exploratory, not causal — it describes patterns in the TMDB dataset rather than explaining *why* they occur. Popularity scores are a platform-specific metric and may not reflect real-world box office success or lasting cultural impact.

[See the full analysis in NB03 →](https://github.com/carmenveera/me204-final-project/blob/main/notebooks/NB03-Data-Analysis.ipynb)