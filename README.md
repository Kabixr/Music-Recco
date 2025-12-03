# 🎧 Emotion-Aware Song Recommendation Engine  
*A hybrid NLP + Machine Learning system that transforms mood text into personalized music recommendations.*

---

## 📌 Overview  
This project builds an intelligent music recommendation engine that interprets a user's mood through natural-language input and predicts a matching audio profile.  
It combines **NLP, supervised regression, audio clustering, similarity search, and Spotify API integration** to generate playlists that align with emotional intent.

The entire workflow runs inside a **single Colab cell**, producing recommendations, visuals, and playlist exports automatically.

---

## 🚀 Key Features  

### 🧠 1. Emotion-to-Audio Feature Mapping (Supervised ML)  
- Converts user mood text → numeric audio features:  
  **danceability, energy, valence, tempo**  
- Powered by **TF-IDF + Ridge Regression** trained on curated mood–feature data.  
- Enhanced with **VADER sentiment** to improve valence prediction.

### 🎶 2. Audio Clustering (KMeans)  
- Groups thousands of songs by audio similarity.  
- Helps match moods to the right musical feel.

### 🔍 3. Recommendation Engine  
- Uses **NearestNeighbor similarity search** to find songs closest to the desired audio profile.  
- Outputs a ranked playlist with distance-based scoring.

### 🎧 4. Spotify Integration (Optional)  
- With a Spotify Client ID + Secret, it fetches **live Spotify URLs** for recommended tracks.  
- Runs normally without credentials (URLs simply omitted).

### 📊 5. Auto-Generated Visualizations  
Saved inside `emotion_music_plots/`:

- Audio Feature Correlation Heatmap  
- PCA Audio Cluster Projection  
- Radar Plot of Target Mood Profile  
- Top Recommendation Text Grid  

### 📄 6. Playlist Export  
- Saves the top recommendations as **emotion_playlist.csv**  
- Includes: title, artist, features, distance score, playable link (if enabled)

---

## 🛠️ Tech Stack  

| Component | Technologies |
|----------|--------------|
| NLP | TF-IDF, VADER Sentiment |
| ML | Ridge Regression, KMeans, NearestNeighbors |
| Data | Pandas, NumPy |
| Visualization | Matplotlib, Seaborn |
| API | Spotify Web API (Spotipy) |
| Runtime | Google Colab |

---

## 📂 Project Structure  
emotion_music_plots/
target_profile_radar.png
cluster_sample_pca.png
top_recommendations_visual.png
emotion_playlist.csv
emotion_recommender.ipynb (optional)
README.md

yaml
Copy code

---

## ▶️ How to Use  

### 1. Open the Colab Notebook  
Run the provided **one-cell script**.

### 2. (Optional) Enter Spotify API Credentials  
- Go to https://developer.spotify.com/dashboard  
- Create an app → copy Client ID + Secret  
- Paste when prompted

### 3. Enter Your Mood Text  
Examples:  
- “I want upbeat workout music”  
- “Feeling sad, need calming soft songs”  
- “Chill lo-fi beats for studying”  
- “Happy vibe romantic playlist”  

### 4. Get Your Playlist  
- Top 10 song recommendations  
- Playable Spotify links (if enabled)  
- Visualizations auto-download  
- CSV playlist generated

---

## 📈 Example Output

Predicted Target Profile:
danceability: 0.78
energy: 0.92
valence: 0.63
tempo: 138 BPM

Top Recommendations:

Blinding Lights — The Weeknd

Physical — Dua Lipa

Rain On Me — Lady Gaga
...

yaml
Copy code

---

## 🧪 Future Enhancements  
- Transformer-based mood mapping (OpenAI/LLMs)  
- Spotify OAuth (user-specific recommendations)  
- Genre-aware cluster modeling  
- Album artwork + audio previews  
- Streamlit / HuggingFace deployment  
- Reinforcement feedback tuning  

---

## ⭐ Project Description (Short Version — 30 Words)  
A hybrid NLP–ML system that interprets mood text, predicts audio features, clusters songs, and retrieves optimized recommendations. Includes supervised mood mapping, Spotify integration, similarity search, visual analytics, and playlist generation.

---

## 🙌 Credits  
- Spotify Audio Features Dataset  
- Scikit-Learn  
- Spotipy  
- NLTK VADER Sentiment  
- Google Colab Runtime

---

## ⭐ If You Like This Project  
Please consider **starring the repository** — it helps support and showcase the work!
