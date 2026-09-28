# Spotify Music Recommendation System & Exploratory Data Analysis

An end-to-end Machine Learning and Data Analytics project developed for the **Data Analytics course at Università della Svizzera italiana (USI)**.  
The project implements a hybrid content-based music recommendation engine leveraging Spotify’s granular audio features, unsupervised clustering (K-Means), and spatial proximity algorithms (KNN).

---

## 🎵 Project Overview

Streaming platforms rely heavily on understanding the intrinsic "musical DNA" of tracks rather than relying solely on surface-level metadata. This project explores over 170,000 individual tracks from a Spotify dataset to:
1. **Decode Musical Evolution:** Analyze how audio features (valence, energy, acousticness, danceability) and explicit content ratios have shifted over the last century using multi-granular datasets (tracks, artists, years, and genres).
2. **Perform Data Cleansing & Outlier Detection:** Remove non-musical artifacts (podcasts, white noise) and handle extreme technical anomalies via IQR and normalization.
3. **Build Recommendation Engines:** Implement and compare a **Hybrid K-Means + Cosine Similarity** model against a **K-Nearest Neighbors (KNN)** model using Euclidean distance.

---

## 🔍 Key Methodologies & Workflow

- **Exploratory Data Analysis (EDA):** Evaluated granularity differences across aggregated datasets (artist/year/genre averages vs. track-level variance) and mapped inter-feature correlations (e.g., strong positive ties between energy and loudness, and an inverse trend in acousticness over time).
- **Hybrid Content-Based Filtering:**
  - Categorized tracks into 15 distinct "musical families" using **K-Means clustering** over 10 core audio features (`acousticness`, `danceability`, `energy`, `instrumentalness`, `liveness`, `speechiness`, `tempo`, `popularity`, `loudness`, `valence`).
  - Applied **Cosine Similarity** within clusters to locate directionally aligned tracks while excluding songs from the same artist.
- **Global KNN Model:** Mapped tracks into a multidimensional vector space to measure absolute "physical proximity" via **Euclidean distance**, prioritizing technical precision and structural consistency.

---

## 📈 Key Insights & Results

- **Genre-Blind Serendipity:** The models demonstrate that mathematical similarity can bridge cultural genre gaps—recommending tracks with identical acoustic tempos or rhythmic energy profiles regardless of human-assigned genre labels.
- **Model Comparison:** While the hybrid K-Means model focuses on cluster-bound stylistic consistency, the global KNN model excels at strict mathematical proximity, serving as a powerful complementary tool for discovering unexpected musical affinities.

---

## 📂 Repository Structure

```text
├── music_recommendation.ipynb   # Full data pipeline, EDA, clustering, and models
├── Report.pdf                   # Formal project report (PDF format)
└── README.md
