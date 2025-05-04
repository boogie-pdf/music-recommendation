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
- spotipy, pandas, numpy, scikit-learn, matplotlib, kagglehub

How to run the code
STEP 1: Set Up Your Spotify API Credentials
  1. Go to https://developer.spotify.com/dashboard
  2. Create an app and get your: client_id , client_secret
<img width="1418" alt="image" src="https://github.com/user-attachments/assets/7d604c86-9ad2-4b62-b428-d542d6ccea6b" />
  3. Replace them in the notebook:
    sp_oauth = SpotifyOAuth(
        client_id='YOUR_CLIENT_ID',
        client_secret='YOUR_CLIENT_SECRET',
        redirect_uri='https://example.com/callback',
        scope='user-top-read playlist-modify-public'
    )
STEP 2: Run the Jupyter Notebook (music_recommendation.ipynb)
  Follow the steps inside the notebook:
     1. Authorize your Spotify account
       First, It will show the link in result. You have to click the link.
       <img width="1244" alt="image" src="https://github.com/user-attachments/assets/29b9dbc8-336e-418d-aeb0-e71b8cbcf168" />
       Then, It will pop up like this, click "authorize"
       <img width="1298" alt="image" src="https://github.com/user-attachments/assets/48678854-0954-4337-9158-f0e70b8a0a9d" />
       Copy link of response URL, thenk put it in the block and click enter.
       <img width="993" alt="image" src="https://github.com/user-attachments/assets/8037f87f-8cbd-4943-be61-6aa1169e0817" />
       <img width="993" alt="image" src="https://github.com/user-attachments/assets/d335b2c2-824a-486a-b8cc-d6853ca7e579" />
       <img width="1238" alt="image" src="https://github.com/user-attachments/assets/559d8a56-f077-483e-be79-f0061e3a892d" />
    2.  Load dataset from Kaggle (via kagglehub)
    3. Generate recommendations
    4. Export them as a new Spotify playlist
    5. Benchmark performance (CPU vs GPU)
  
