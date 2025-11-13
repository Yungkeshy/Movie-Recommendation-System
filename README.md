# Movie Recommendation System

![Python](https://img.shields.io/badge/Python-3.9%2B-blue.svg)
![Streamlit](https://img.shields.io/badge/Streamlit-1.25%2B-red.svg)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-1.3%2B-orange.svg)

This project is a hybrid movie recommendation system built with Python, Scikit-learn, and Streamlit. It explores two common recommendation strategies: **Content-Based Filtering** and **Collaborative Filtering**.

The final web application uses the content-based model to provide real-time movie suggestions.

---

## 📸 App Screenshot

(I highly recommend taking a screenshot of your Streamlit app running and placing it here. This is more professional than the wallpaper link. First, push the screenshot file, e.g., `app_screenshot.png`, to your repo, then change the line below.)

![Screenshot of the Streamlit App](app_screenshot.png)

---

## ⚙️ Methodology

The repository explores two different machine learning approaches for recommendations.

### 1. Content-Based Filtering (Used in Streamlit App)
This model recommends movies by finding items with similar attributes (like genres, keywords, and overview).
* **Vectorization:** Movie attributes (genres, overview, keywords, etc.) are combined into a single "tags" string.
* **NLP Model:** A **TF-IDF Vectorizer** is used to convert these tags into a high-dimensional vector space.
* **Similarity:** **Cosine Similarity** is calculated between all movie vectors to find the most similar items.
* **Result:** The Streamlit app (`app.py`) uses a pickled version of this similarity matrix (`similarity.pkl`) to find the top 5 most similar movies to a user's selection.

### 2. Collaborative Filtering (Explored in Notebook)
This model recommends movies based on the behavior of similar users.
* **Model:** A **K-Nearest Neighbors (KNN)** algorithm is used.
* **Matrix:** The model is trained on a sparse user-item matrix of movie ratings.
* **Similarity:** It finds users with similar rating patterns to suggest movies they liked.

---

## 🛠️ Tech Stack
* **Data Analysis:** Pandas, NumPy
* **Machine Learning:** Scikit-learn (TF-IDF, Cosine Similarity, KNN)
* **Web App:** Streamlit
* **Data Serialization:** Pickle

---

## 🚀 How to Run the App

This repository includes a pre-built Streamlit app that uses saved models.

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/Yungkeshy/Movie-Recommendation-System.git](https://github.com/Yungkeshy/Movie-Recommendation-System.git)
    cd Movie-Recommendation-System
    ```

2.  **Install dependencies:**
    It's recommended to use a virtual environment.
    ```bash
    pip install -r requirements.txt
    ```

3.  **Run the Streamlit app:**
    This command will start a local web server and open the app in your browser.
    ```bash
    streamlit run app.py
    ```

---


## 📊 Dataset

The project uses the "Movies and Ratings for Recommendation System" dataset from Kaggle.
* **Source:** [Kaggle Dataset Link](https://www.kaggle.com/datasets/nicoletacilibiu/movies-and-ratings-for-recommendation-system/data)
