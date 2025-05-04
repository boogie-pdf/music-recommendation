# Music Recommendation System
Music Recommendation System By No veggie group

Features 
1. Spotify OAuth Authentication
2. Fetch User's Top Tracks from Spotify
3. Load Audio Feature Dataset from Kaggle
4. Build User Profile from Listening History
5. Recommend Songs Using K-Nearest Neighbors
6. Export Recommendations & Add to Spotify Playlist
7. Benchmark Execution Time on CPU vs GPU
8. Visualize Performance Comparison

Requirements Library
1. spotipy – Spotify Web API client
2. pandas, numpy – Data analysis and numerical computing
3. scikit-learn – Machine learning (KNN)
4. matplotlib – Visualization
5. kagglehub - Load datasets from Kaggle

---

## How to run the code

### STEP 1: Set Up Your Spotify API Credentials
  1. Go to https://developer.spotify.com/dashboard
  2. Create an app and get your: client_id , client_secret

<img width="1418" alt="image" src="https://github.com/user-attachments/assets/7d604c86-9ad2-4b62-b428-d542d6ccea6b" />

  3. Replace them in the notebook:
      ```python
          sp_oauth = SpotifyOAuth(
          client_id='YOUR_CLIENT_ID',
          client_secret='YOUR_CLIENT_SECRET',
          redirect_uri='https://example.com/callback',
          scope='user-top-read playlist-modify-public'
      )

### STEP 2: Run the Jupyter Notebook (`music_recommendation.ipynb`)

Follow the steps inside the notebook to complete the recommendation pipeline:

---
  
#### **1. Authorize your Spotify account**

  **1.1** The notebook will display a URL. Click it.  
<img width="600" src="https://github.com/user-attachments/assets/29b9dbc8-336e-418d-aeb0-e71b8cbcf168" />

  **1.2** Authorize the app in the browser.  
<img width="600" src="https://github.com/user-attachments/assets/48678854-0954-4337-9158-f0e70b8a0a9d" />

  **1.3** After authorizing, copy the **redirected URL** and paste it back into the notebook input.  
<img width="600" src="https://github.com/user-attachments/assets/8037f87f-8cbd-4943-be61-6aa1169e0817" />  

<img width="600" src="https://github.com/user-attachments/assets/d335b2c2-824a-486a-b8cc-d6853ca7e579" /> 

<img width="600" src="https://github.com/user-attachments/assets/559d8a56-f077-483e-be79-f0061e3a892d" />

---

#### **2. Load Dataset from Kaggle (via `kagglehub`)**

The notebook uses `kagglehub` to download the dataset:  
[maharshipandya/-spotify-tracks-dataset](https://www.kaggle.com/datasets/maharshipandya/-spotify-tracks-dataset)

---
    
#### **3. Generate Recommendations**

Averages your top Spotify tracks on selected audio features:  
`valence`, `energy`, `danceability`, `tempo`, etc.

---

#### **4. Export Recommendations to Spotify Playlist**

Uses `scikit-learn`'s **K-Nearest Neighbors** to find similar songs.  
Recommended tracks are automatically added to your Spotify account under the playlist:  
> 🎵 **No Veggie Recs**

---

#### **5. Benchmark Performance (CPU vs GPU)**

If you run the notebook on multiple hardware types (CPU, GPU, TPU), the system will generate:

- `benchmark_cpu.json`  
- `benchmark_gpu.json`

---

#### **6. Benchmark Performance (CPU vs GPU)**

If you run the notebook on multiple devices (CPU, GPU, TPU), your benchmark results will be saved as:

- `benchmark_cpu.json`
- `benchmark_gpu.json`

The results are visualized using `matplotlib` in a **log-scaled bar chart** for clear comparison.

---

# Important Note:
__Please avoid running STEP 11 in the notebook while running other steps at the same time. Run it only after all processing is complete.__
