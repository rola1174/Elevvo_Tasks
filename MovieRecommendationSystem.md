# MovieLens 100K Recommendation System

## Project Overview
This project implements a **Movie Recommendation System** using the **MovieLens 100K dataset**. 
The system provides personalized movie recommendations using collaborative filtering and matrix factorization methods.

### Main Goals
- Recommend movies based on **user similarity**.
- Implement **user-based** and **item-based collaborative filtering (CF)**.
- Apply **matrix factorization (SVD)** for recommendations.
- Evaluate performance using **Precision@10**.
- Visualize a **comparison of recommendation methods**.

---

## Dataset
**MovieLens 100K Dataset** from [Kaggle](https://www.kaggle.com/datasets/rajmehra03/movielens100k)

Files used:
- `u.data` – user-item ratings (user_id, item_id, rating, timestamp)
- `movies.csv` – movie IDs and titles

**Dataset stats**:
- 943 users
- 1,682 movies
- 100,000 ratings

---

## Tools & Libraries
- Python 3
- Pandas, Numpy
- Scikit-learn
- Matplotlib, Seaborn
- KaggleHub (for downloading dataset in Colab)

---

## Methods Implemented

### 1. User-Based Collaborative Filtering (User-CF)
- Computes **cosine similarity** between users.
- Recommends movies that similar users rated highly.
- Mean-centered ratings improve prediction accuracy.

### 2. Item-Based Collaborative Filtering (Item-CF)
- Computes **cosine similarity** between items.
- Recommends movies similar to the ones a user liked.

### 3. Matrix Factorization (SVD)
- Uses **Truncated SVD** to reduce the user-item matrix.
- Reconstructs predicted ratings for all users.
- Recommends unseen movies with highest predicted scores.

---

## Train/Test Split
- Each user's ratings are split into **train (80%)** and **test (20%)** sets.
- Test set ratings with `rating >= 4` are considered relevant for evaluation.

---

## Evaluation: Precision@10
- Precision@10 measures how many of the top-10 recommended movies were actually relevant.
- Formula:  
  \[
  \text{Precision@10} = \frac{\text{# of recommended movies in top 10 that are relevant}}{10}
  \]

**Results:**

| Method    | Precision@10 |
|-----------|--------------|
| User-CF   | 0.226        |
| Item-CF   | 0.223        |
| SVD       | 0.269        |

> 🎯 SVD achieved the best performance among the three methods.

---

## Visualization
A bar plot shows the **Precision@10 comparison**:

![Precision@10 Comparison](precision_plot.png)

---

## Example Recommendations
Top 10 **User-CF recommendations** for **User 1**:

| Title                                     | Score  |
|-------------------------------------------|--------|
| Far From Home: The Adventures of Yellow Dog (1995) | 11.14  |
| Superweib, Das (1996)                     | 10.60  |
| Billy Madison (1995)                       | 9.27   |
| Something to Talk About (1995)            | 8.94   |
| Mask, The (1994)                           | 8.31   |
| Four Weddings and a Funeral (1994)        | 7.90   |
| Dolores Claiborne (1995)                   | 7.69   |
| Assassins (1995)                           | 6.93   |
| …                                         | …      |

---

## How to Run
1. Clone the repository:
   ```bash
   git clone <repo-url>
