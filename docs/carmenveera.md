

# Do Popularity and Audience Ratings Move Together Across Film Genres?

**Author:** Carmen Vera

We tend to assume that popular movies are popular *because* audiences love them most. Looking at genre-level data from The Movie Database (TMDB), this turns out to be only half true — and the full picture reveals something bigger about how film genres have evolved over the last five decades.

## It starts with an imbalance: some genres get far more attention than others

<iframe src="charts/finding1_average_popularity_by_genre.html" width="100%" height="450" style="border:none;"></iframe>

Science Fiction (16.78) and Adventure (15.29) top the popularity rankings by a wide margin, followed by Fantasy (13.07). Drama sits near the bottom at 7.93, despite being the single most common genre in the dataset (2,427 films). Only Documentary ranks lower, at 5.31. That's the first surprise: the genre made most often isn't the genre audiences pay the most attention to. This raises an obvious question — is that attention going to the genres audiences rate *best*, or just the ones that catch their eye?

## The answer: popularity and audience rating are largely separate conversations

<iframe src="charts/finding2_popularityvsvote_by_decade.html" width="100%" height="450" style="border:none;"></iframe>

They're not the same thing. Music has the highest average audience rating of any genre (7.36), despite low popularity. Science Fiction (6.64) and Adventure (6.65) — the two most *popular* genres — sit in the middle of the rating range. The clearest mismatch is Horror: fairly popular (10.52), but the lowest-rated major genre in the dataset (6.25). Drama, the most frequent genre, rates only averagely (7.96) too. If popularity tracked how audiences rate films, these rankings would line up. They don't.

## And that gap helps explain a real shift happening across the industry

<iframe src="charts/finding3_genre_share_by_decade.html" width="100%" height="450" style="border:none;"></iframe>

Put the two patterns together and a five-decade trend comes into focus. Drama's share of top films has fallen from 39.1% in the 1970s to 26.7% today — a genre that draws comparatively little popularity. Meanwhile, Action (9.5% → 17.8%) and Thriller (11.2% → 18.2%) — genres that lean toward popularity over rating — have both roughly doubled their share of top films over the same period. Comedy has drifted down too (22.7% → 17.4%), while Adventure and Romance have stayed fairly flat.

## What this means

The genres gaining ground over the last 50 years aren't the ones audiences rate highest — they're the ones that reliably generate popularity, whether or not that popularity comes with a strong rating. Drama, once the dominant genre by share, has lost the most ground; Action and Thriller, stronger on popularity than on rating, have gained the most. That's a meaningful pattern: it suggests the film industry's genre mix has shifted in response to what draws attention, not necessarily what audiences rate as "good."

What the data can't tell us is *why* — whether this is driven by marketing spend, franchise strategy, streaming algorithms, or changing audience tastes. But the consistency of the shift across five decades, and its alignment with the popularity–rating gap, makes it a pattern worth taking seriously rather than dismissing as noise.

## Limitations

This analysis is exploratory: it documents a pattern in the TMDB dataset rather than testing why it happens.

**"Popularity" here is a TMDB platform metric** — based on page views, votes, and watchlist activity — not box office revenue or a measure of lasting cultural impact, so it may not generalise to other definitions of "success."

**"Rating" here means audience rating, not critical acclaim.** TMDB's `vote_average` is the average score left by TMDB's own registered users, not a professional critics' score from an outlet like Metacritic or Rotten Tomatoes. This analysis says nothing about how professional critics received these genres.

**The dataset itself is popularity-pre-filtered.** It comes from TMDB's `/movie/popular` endpoint, so every film here already cleared TMDB's bar for "popular" before this analysis began. That makes it well-suited to comparing popularity and rating *within* the pool of films that already draw some attention, but it cannot say anything about genre patterns among obscure or low-visibility films.

**The genre-share trend aggregates all TMDB-listed popular films within each decade**, which may not fully represent theatrical releases or box-office hits specifically, and more recent decades likely have denser, more complete TMDB coverage than older ones.

[See the full analysis in NB03 →](https://github.com/carmenveera/me204-final-project/blob/main/notebooks/NB03-carmenveera-Data-Analysis.ipynb)