# Do Popularity and Critical Acclaim Move Together Across Film Genres?

**Author:** Carmen Vera 

We tend to assume that popular movies are popular *because* they're good. Looking at genre-level data from The Movie Database (TMDB), this turns out to be only half true — and the full picture reveals something bigger about how film genres have evolved over the last five decades.

## It starts with an imbalance: some genres get far more attention than others

<iframe src="charts/finding1_average_popularity_by_genre.html" width="100%" height="450" style="border:none;"></iframe>

Science Fiction and Adventure top the popularity rankings by a wide margin, while Drama sits near the bottom despite being the single most common genre in the dataset. That's the first surprise: the genre made most often isn't the genre audiences pay the most attention to. This raises an obvious question — is that attention going to the *best* films, or just the most eye-catching ones?

## The answer: popularity and quality are largely separate conversations

<iframe src="charts/finding2_popularityvsvote_by_decade.html" width="100%" height="450" style="border:none;"></iframe>

They're not the same thing. Animation has the highest average critical rating of any genre, yet only moderate popularity. Science Fiction and Adventure, the two most *popular* genres, land in the middle of the pack when it comes to rating. The clearest mismatch is Horror: reasonably popular, but consistently the lowest-rated major genre in the dataset. If popularity tracked quality, these rankings would line up. They don't.

## And that gap helps explain a real shift happening across the industry

<iframe src="charts/finding3_genre_share_by_decade.html" width="100%" height="450" style="border:none;"></iframe>

Put the two patterns together and a five-decade trend comes into focus. Drama's share of top films has fallen from roughly 37% in the 1970s to around 25% today — a genre that rates well critically but draws comparatively little popularity. Meanwhile, Action and Thriller — genres that lean toward popularity over acclaim — have both roughly doubled their share of top films over the same period. Comedy has drifted down slightly too, while Adventure and Romance have stayed fairly flat.

## What this means

The genres gaining ground over the last 50 years aren't the ones that are rate highest — they're the ones that reliably generate popularity, whether or not that popularity comes with acclaim. Drama, the strongest critical performer, has lost the most ground; Action and Thriller, stronger on popularity than on rating, have gained the most. That's a meaningful pattern: it suggests the film industry's genre mix has shifted in response to what draws attention, not necessarily what's considered "good."

What the data can't tell us is *why* — whether this is driven by marketing spend, franchise strategy, streaming algorithms, or changing audience tastes. But the consistency of the shift across five decades, and its alignment with the popularity–rating gap, makes it a pattern worth taking seriously rather than dismissing as noise.

## Limitations

This analysis is exploratory: it documents a pattern in the TMDB dataset rather than testing why it happens. "Popularity" here is a platform-specific TMDB metric, not box office revenue or a measure of lasting cultural impact, so it may not generalise to other definitions of "success." The genre-share trend also aggregates all TMDB-listed films within each decade, which may not fully represent theatrical releases or box-office hits specifically.

[See the full analysis in NB03 →](https://github.com/carmenveera/me204-final-project/blob/main/notebooks/NB03-carmenveera-Data-Analysis.ipynb)