# Movie Recommendation System using Machine Learning with Python


## Project Overview

This project builds a Movie Recommendation System using content-based filtering with Python and machine learning. The system recommends movies similar to the ones users like, using features such as genres, cast, crew, keywords, and descriptions.
---

## 📂 Dataset:

The dataset used is from TMDb (The Movie Database) and contains:

- movies.csv — movie metadata


## Key columns used:

- title
- overview
- genres
- cast
- crew
- keywords


---

## ML Concepts Implemented

- **Data Preprocessing**:
  
  - Merged movie and credits datasets
  - Extracted key fields (director, cast, genres, keywords)
  - Removed duplicates and missing values
  - Cleaned and tokenized text data

- **Feature Engineering**:
  
  - Combined relevant features into a single 'tags' column
  - Converted text into lowercase, removed spaces and punctuation
  - Used Stemming with NLTK's PorterStemmer

- **Vectorization**:

  - Applied TF-IDF Vectorizer to convert text into numerical format
  - Computed cosine similarity matrix for content comparison

- **Recommendation**:
 ```python 
def recommend(movie):
    movie_index = df[df['title'] == movie].index[0]
    distances = similarity[movie_index]
    movies_list = sorted(list(enumerate(distances)), reverse=True, key=lambda x:x[1])[1:6]
    return [df.iloc[i[0]].title for i in movies_list]
```
---

## Technologies Used

- Python
- Jupyter Notebook
- pandas
- numpy
- scikit-learn
- nltk
- ast
- pickle

---

## Conclusion

- This project demonstrates the end-to-end pipeline of building a content-based movie recommendation system using real-world data. It highlights skills in data preprocessing, NLP, feature extraction, machine learning, and similarity metrics. With future enhancements like collaborative filtering and deployment, this project can evolve into a full production-level system.

---

## Results

- The recommendation engine was able to suggest accurate and relevant movie titles based on user input, showcasing the power of content similarity using NLP and cosine distance. The model performs well with diverse genres and delivers useful suggestions in real-time.

  
---


## 📬 Contact

**Akash Kumar Rajak**  
📧 Email: [akashkumarrajak200@gmail.com](mailto:akashkumarrajak200@gmail.com)  
💼 GitHub: [AkashKumarRajak](https://github.com/AkashKumarRajak)<br>
🔗 LinkedIn: [AkashKumarRajak](https://www.linkedin.com/in/akash-kumar-rajak-22a98623b/)



