# Spotify-Descriptive-Analytics-Report-

# 🎧 Audio Aura: Wrapped

**Decoding Listener Behaviour and Chart-Topping Trends**

A descriptive analytics study of what 80 Spotify tracks reveal about genre, mood, release trends and popularity. Built with Python, Pandas, Matplotlib and Seaborn.

---

## 📌 Overview

This project applies descriptive analytics to a real-world music dataset to understand how **genre, audio features, artist identity and release timing** relate to a track's popularity on Spotify. It ends with practical suggestions for playlist curators, artists and labels, and a roadmap towards predictive analysis.

| | |
|---|---|
| **Course** | BCA, Data Science & Artificial Intelligence (2nd Year), BCADS23 |
| **Subject** | Descriptive Analytics |
| **Faculty** | Ms Monika Rao |
| **University** | Babu Banarasi Das University |

---

## 📊 Dataset

- **Source:** [30,000 Spotify Songs (Kaggle)], it's reproducible).
- **Cleaning:** kept 12 relevant columns, converted duration from milliseconds to minutes, engineered `release_year`, and fixed 3 tracks whose release date was a bare year. No duplicates and very few missing values; one genuine loudness outlier (−36.5 dB) was kept.

---

## 🎯 Objectives

1. Which genres dominate the sample?
2. Which artists and tracks are most popular, and why?
3. How have duration and popularity changed across release years?
4. How do popularity and audio features (danceability, energy, valence, acousticness) relate?
5. What makes each genre musically distinct?
6. Which audio features move together?

---

## 🔍 Key Findings

- **Genre concentration:** rap (26%), pop (19%) and r&b (16%) make up 61% of the sample; rock is smallest at 10%.
- **Popularity is artist-driven:** Camila Cabello (87) and The Chainsmokers (85) lead; most others sit between 73 and 79.
- **Audio features barely predict popularity:** the strongest correlation with popularity is danceability at r = 0.15.
- **Genres have audio fingerprints:** EDM has the lowest acousticness (0.04) and highest energy (0.80); rap has the highest danceability (0.72).
- **Songs got shorter:** average duration fell from 6.3 min (1978) to a stable 3.3–5.1 min band from the 2000s onward.
- **Production features move together:** energy vs loudness is +0.60 and energy vs acousticness is −0.50.

---

## 📈 Visualisations

| # | Chart | Purpose |
|---|---|---|
| 1 | Top 8 artists (bar) | Average popularity by artist |
| 2 | Genre distribution (donut) | Share of each genre |
| 3 | Audio traits by genre (grouped bar) | What makes each genre unique |
| 4 | Lowest 10 tracks (line) | Do low-popularity tracks share audio traits? |
| 5 | Top artists by playtime (bar) | Total listening minutes per artist |
| 6 | Mood vs energy and tempo vs loudness (scatter) | Quadrant view of sound and production |
| 7 | Popularity and duration by year (dual line) | Trends over time |
| 8 | Correlation matrix (heatmap) | Relationships between features |

---

## 🧮 Statistical Methods

- **Aggregation:** genre totals and average popularity
- **Central tendency:** mean 44.1, median 48.0, mode 0 (7 tracks) for popularity
- **Spread:** range, standard deviation (popularity SD = 24.1)
- **Frequency distribution:** release-year decades (the 2010s account for 72.5% of the sample)

---

## ⚠️ Limitations

- Small sample (n = 80), so small genres like rock are "a snapshot of this sample", not the full picture.
- Year-level averages for 1991 and 2013 rest on a single track each; the dips to zero are sampling artefacts.
- The source playlists lean towards upbeat, radio-friendly music, which limits generalisation to all of Spotify.

---

## 🔮 Next Steps (Predictive)

Popularity prediction, genre auto-tagging, song-length forecasting and similarity-based recommendation engines.

---

## 📚 References

- Arvidsson, J. (2020). *30,000 Spotify songs* [Data set]. Kaggle.
- McKinney, W. (2010). Data structures for statistical computing in Python.
- Hunter, J. D. (2007). Matplotlib: A 2D graphics environment.
- Waskom, M. L. (2021). Seaborn: Statistical data visualization.

---

## 👩‍💻 Author

**Joanna**, BCA (Data Science & AI), Babu Banarasi Das University
