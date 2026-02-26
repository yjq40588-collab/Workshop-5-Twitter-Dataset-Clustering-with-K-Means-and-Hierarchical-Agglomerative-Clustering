# Workshop 5: Twitter Dataset Clustering with K-Means and Hierarchical Agglomerative Clustering

> **Course**: NLP  
> **Student**:JIAQI YANG
> **Student ID**: [682131020]

---

## Project Overview
This repository contains the full implementation of **Workshop 5**, which focuses on clustering analysis of a historical Twitter dataset using two unsupervised learning algorithms: **K-Means** and **Hierarchical Agglomerative Clustering (HAC)**.

The goal is to:
- Convert text and time features into numerical representations.
- Identify distinct tweet behavior patterns (e.g., casual updates vs. interactive/promotional content).
- Compare the performance and interpretability of K-Means and HAC on large-scale data.

---

##  Dataset
- **File**: `workshop_km.csv`
- **Size**: 1,048,575 rows × 4 columns
- **Original columns**:
  - `timestamp`: Tweet posting time (PDT)
  - `fixed_col`: Constant value (`NO_QUERY`)
  - `username`: Twitter username
  - `tweet`: Tweet content

### Feature Engineering
For clustering, we extract 6 numerical features:
| Feature          | Description |
|------------------|-------------|
| `hour`           | Hour of day (0–23) from timestamp |
| `minute`         | Minute of hour (0–59) from timestamp |
| `tweet_length`   | Character count of the tweet |
| `word_count`     | Number of words in the tweet |
| `mention_count`  | Number of `@user` mentions |
| `url_count`      | Number of URLs in the tweet |

---

##  Dependencies
Install required libraries:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn scipy
