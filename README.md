# Music_Recomendation_System-Kmeans_Clustering

🎶 Music Recommendation System
This project implements a content-based music recommendation system using unsupervised machine learning (KMeans clustering) on audio features. The system groups songs with similar characteristics (danceability, energy, tempo, valence, etc.) and recommends tracks from the same cluster, enabling efficient music discovery.

📂 Dataset
File: final_music_dataset.csv
Rows: 600 songs
Features:
Metadata: track, artist, language
Audio Features: danceability, energy, valence, tempo, acousticness, instrumentalness, speechiness, liveness, duration_ms
Preprocessing: Standardized with StandardScaler to normalize feature ranges.

🛠️ Tech Stack
Programming Language: Python
Libraries Used:
pandas, numpy → Data manipulation
scikit-learn → Feature scaling, KMeans clustering
matplotlib, seaborn → Data visualization

📊 Workflow
Data Preprocessing
Removed non-numeric columns (track, artist, language)
Standardized numerical features using StandardScaler

Clustering (KMeans)
Applied Elbow Method to determine optimal number of clusters
Trained KMeans (k=4) to group songs into clusters

Visualization
Plotted Elbow Curve to justify cluster selection
Used Seaborn boxplots to analyze feature distribution across clusters

Recommendation Engine
Function recommend_similar_songs(song_name) finds the cluster of a given song
Returns 5 random recommendations from the same cluster (similar audio profile)

📈 Results
Songs are grouped into 4 distinct clusters based on mood, danceability, and energy.
Recommendations successfully suggest tracks with similar vibes.

🚀 Future Enhancements
Replace random sampling with Cosine Similarity for ranking-based recommendations
Integrate lyrics embeddings (NLP) and genre metadata
Add user profile learning for personalization
Connect with Spotify API for real-time data and streaming integration
