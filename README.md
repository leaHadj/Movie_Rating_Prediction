# IMDB Movie Rating Prediction

This project aims to predict IMDB movie ratings using a combination of textual and numerical features extracted from movie metadata.  
It was developed as a personal project to strengthen skills in **data preprocessing, feature engineering, and supervised machine learning**.

---

## Project Overview

The goal of this project is to automatically estimate the **IMDB score** of a movie based on information such as its title, genre, description, duration, budget, and popularity.  

The project follows a complete **data science pipeline**:
- Data loading and cleaning  
- Exploratory Data Analysis (EDA)  
- Feature engineering (encoding, normalization, text vectorization)  
- Model training (Regression models)  
- Evaluation and interpretation of results  

---

## Dataset

The dataset comes from IMDB and includes various metadata such as:
- Movie titles and overviews  
- Genres  
- Release dates  
- Budgets and revenues  
- Popularity and vote counts  
- IMDB average rating (target variable)

---

## Machine Learning Approach

| Step | Description |
|------|--------------|
| **Preprocessing** | Handling missing data, encoding categorical features, text cleaning |
| **Feature Engineering** | Combining numerical and textual data (TF-IDF, one-hot encoding) |
| **Modeling** | Linear Regression, Random Forest, Gradient Boosting |
| **Evaluation** | RMSE, MAE, R² metrics used to assess performance |

The best results were obtained using a **Gradient Boosting Regressor**, which provided a good balance between bias and variance.

---

## Technologies Used

| Purpose | Library |
|----------|----------|
| Data Manipulation | Pandas, NumPy |
| Visualization | Matplotlib, Seaborn |
| Machine Learning | Scikit-learn |
| Text Processing | TfidfVectorizer |
| Python Version | 3.11 |

---

## Results

- Best model: **Gradient Boosting Regressor**  
- RMSE: around **0.45** on the test set  
- The model correctly captures the relationship between popularity, vote count, and IMDB score.

Example insight:
> Movies with high budgets and many votes tend to have more stable ratings, while lesser-known independent films show more variability.

---

## Installation and Execution

```bash
git clone https://github.com/leaHadj/IMDB-Rating-Prediction.git
cd IMDB-Rating-Prediction

python -m venv venv
venv\Scripts\activate    # On Windows
# or
source venv/bin/activate # On Mac/Linux

pip install -r requirements.txt
jupyter notebook
