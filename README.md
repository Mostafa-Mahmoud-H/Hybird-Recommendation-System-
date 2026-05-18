# 🎬 Hybrid Movie Recommendation System

A movie recommendation system that combines **Content-Based Filtering** and **Collaborative Filtering** into a hybrid model, built with Python and deployed via Streamlit.

---

## 🚀 Live Demo

> Deploy on [Streamlit Cloud](https://streamlit.io/cloud) using the instructions below.

---

## 📌 How It Works

The system uses two techniques and merges them into a single score:

| Technique | Method | Weight |
|---|---|---|
| Content-Based Filtering | TF-IDF + Cosine Similarity on movie genres | 60% |
| Collaborative Filtering | SVD matrix factorization (Surprise library) | 40% |

**Final Score Formula:**
```
final_score = (0.6 × content_similarity) + (0.4 × predicted_rating / 5)
```

---

## 🗂️ Project Structure

```
movie_recommendation_project/
│
├── app.py                  # Streamlit app (main entry point)
│
├── src/
│   ├── data_processing.py  # Load and clean movies & ratings data
│   ├── content_based.py    # TF-IDF content-based engine
│   ├── collaborative.py    # SVD collaborative filtering model
│   ├── hybrid_model.py     # Combines both models
│   └── evaluation.py       # RMSE, MAE, Precision, Recall, F1 metrics
│
├── data/
│   └── raw/
│       ├── movies.csv      # MovieLens movies dataset
│       └── ratings.csv     # MovieLens ratings dataset
│
├── requirements.txt
└── README.md
```

---

## ⚙️ Installation & Run Locally

### 1. Clone the repository
```bash
git clone https://github.com/Omar7atem/Hybird-Movie-Recommendation-System.git
cd Hybird-Movie-Recommendation-System
```

### 2. Install dependencies
```bash
pip install -r requirements.txt
```

### 3. Run the app
```bash
streamlit run app.py
```

---

## ☁️ Deploy on Streamlit Cloud

1. Push your code to GitHub.
2. Go to [share.streamlit.io](https://share.streamlit.io) and connect your repo.
3. Set the **Main file path** to `app.py`.
4. Make sure `requirements.txt` is in the root of the repo.
5. Click **Deploy** — done!

---

## 📊 Dataset

This project uses the [MovieLens Small Dataset](https://grouplens.org/datasets/movielens/latest/):

- **movies.csv** — 9,742 movies with title and genres
- **ratings.csv** — 100,836 ratings from 610 users

---

## 📈 Evaluation Results (SVD Model)

| Metric | Value |
|---|---|
| RMSE | ~0.87 |
| MAE | ~0.67 |
| Precision@10 | ~0.78 |
| Recall@10 | ~0.62 |
| F1@10 | ~0.69 |

> Results may vary slightly due to random state in train/test split.

---

## 🛠️ Tech Stack

- **Python 3.10**
- **Streamlit** — Web UI
- **Pandas** — Data processing
- **Scikit-learn** — TF-IDF & Cosine Similarity
- **Scikit-Surprise** — SVD Collaborative Filtering

---

## 👤 Author

**Omar Hatem**  
GitHub: [@Omar7atem](https://github.com/Omar7atem)
