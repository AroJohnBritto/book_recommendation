# Book Recommendation System

This project implements a **content-based book recommender** using a K-Nearest Neighbors model on book metadata (title, author, publisher). The goal is to recommend similar books based on user input using simple, interpretable features.

---

##  Project Features

* Uses a cleaned book dataset (`books.csv`)
* One-hot encoding for categorical metadata
* K-Nearest Neighbors (`ball_tree`) algorithm for efficient similarity search
* Custom recommendation function with case-insensitive matching
* Optional PCA-based 2D visualization of neighbors

---

##  Technologies Used

* Python 3.x
* pandas
* scikit-learn
* matplotlib
* Jupyter Notebook (for development)

---

##  Project Structure

```
├── books.csv                # Book metadata
├── recommender.ipynb        # Main notebook with code and visualization
├── README.md                # Project documentation (this file)
```

---

##  How It Works

1. Loads and cleans the book dataset
2. Encodes categorical columns into numeric features using `pd.get_dummies()`
3. Fits a `NearestNeighbors` model to the features
4. Accepts a user-provided book title (case-insensitive)
5. Returns 5 similar book titles using nearest neighbor indices

---

##  Visualization

Uses PCA to reduce feature space to 2D and plots the target book and its top neighbors for visual inspection.

---

##  Usage Example

```python
BookRecommender('Poor People')
```

Returns:

```
['Poor People', 'Title 2', 'Title 3', 'Title 4', 'Title 5', 'Title 6']
```

