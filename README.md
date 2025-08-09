# 🎬 Movie Recommendation System – Collaborative Filtering (User-Based)

## 1. Problem Statement and Goal of Project

The goal of this project is to implement a **user-based collaborative filtering** recommendation system for movies.
Given a target user's rated movies, the system finds similar users, aggregates their preferences, and recommends new movies that the target user is likely to enjoy.

---

## 2. Solution Approach

The solution is based on **memory-based collaborative filtering** using **Pearson correlation** to measure similarity between users:

1. **Data Cleaning & Preparation**

   * Extract movie release years from titles.
   * Clean movie titles by removing year annotations.
   * Merge movie metadata with user ratings.

2. **Target User Selection**

   * Define a set of movies and ratings for a specific target user.

3. **Find Similar Users**

   * Identify users who rated at least one of the same movies.
   * Compute **Pearson correlation** between the target user and each similar user.

4. **Weighted Recommendations**

   * Weight other users’ ratings by their similarity scores.
   * Aggregate weighted ratings per movie to generate a ranked list of recommendations.

---

## 3. Technologies & Libraries

* **Python**
* **pandas** – Data manipulation and merging datasets
* **NumPy** – Numerical operations
* **Matplotlib** – Visualization of intermediate results (inline in Jupyter)
* **math.sqrt** – Pearson correlation calculation

---

## 4. Description about Dataset

* **movies.csv** – Contains `movieId`, `title`, and `genres` for each movie.
* **ratings\_sample.csv** – Contains `userId`, `movieId`, `rating`, and `timestamp`.
* Genres were dropped for this analysis; only movie title and year were retained for recommendations.

---

## 5. Installation & Execution Guide

1. **Clone the repository** and navigate to the project folder:

   ```bash
   git clone <repo-url>
   cd <repo-folder>
   ```
2. **Install dependencies**:

   ```bash
   pip install pandas numpy matplotlib
   ```
3. **Run the notebook** in Jupyter:

   ```bash
   jupyter notebook RecSys-Collaborative-Filtering-movies.ipynb
   ```

---

## 6. Key Results / Performance

* Successfully identifies the top movies recommended for the target user based on ratings from similar users.
* Pearson correlation ensures recommendations are weighted toward users with stronger similarity scores.

---

## 7. Screenshots / Sample Outputs

Sample recommendation flow in the notebook:

* Cleaned movie titles with extracted years
* Target user’s rated movies
* Top similar users (Pearson correlation scores)
* Final list of recommended movies ranked by weighted similarity

---

## 8. Additional Learnings / Reflections

* This project demonstrates **understanding of collaborative filtering from scratch** without relying on pre-built recommendation libraries.
* Shows the step-by-step transformation from raw CSV data to final recommendations.
* Implementation decisions, such as dropping genres and focusing on year/title cleaning, simplified the similarity calculation process.

---

## 👤 Author

**Mehran Asgari**
📧 [imehranasgari@gmail.com](mailto:imehranasgari@gmail.com)
🌐 [https://github.com/imehranasgari](https://github.com/imehranasgari)

---

## 📄 License

This project is licensed under the MIT License – see the `LICENSE` file for details.

---

> 💡 *Some interactive outputs (e.g., plots, widgets) may not display correctly on GitHub. If so, please view this notebook via [nbviewer.org](https://nbviewer.org) for full rendering.*

---