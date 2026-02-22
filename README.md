# 🍎 Fruit Classification using Random Forest

## Overview
This project implements a **fruit classification system** using a **Random Forest classifier**.  
The main focus is on **exploratory data analysis (EDA)** and **handling missing values correctly** based on feature distributions, rather than blindly applying a single imputation strategy.

---

## Dataset Description
The dataset contains several features describing fruits, such as:

- `shape` – discrete numeric values representing fruit shape
- `taste` – categorical/ordinal values indicating taste characteristics
- `color` – ordinal numeric values representing color levels
- `fruit_name` – encoded fruit label (target variable)

Some features contain **missing (null) values**, which are handled during preprocessing.

---

## Exploratory Data Analysis (EDA)
Distribution plots (histograms with KDE) are used to understand the nature of each feature:

- **Shape & Taste**
  - Few distinct values
  - Strong spikes in the distribution
  - Treated as categorical-like features

- **Color**
  - Multiple ordered numeric levels
  - More spread-out distribution
  - Treated as an ordinal numeric feature

EDA guides the choice of imputation method.

---

## Missing Value Handling
Different imputation strategies are applied based on feature characteristics:

| Feature | Nature | Imputation Method |
|------|------|----------------|
| `shape` | Discrete / categorical-like | Mode |
| `taste` | Discrete / categorical-like | Mode |
| `color` | Ordered numeric | Median |

Additionally, **missing indicator columns** are added to preserve information about missingness when useful.

---

## Model
- **Algorithm:** Random Forest Classifier
- **Why Random Forest?**
  - Handles non-linear relationships
  - Robust to outliers
  - Works well with simple imputation methods
  - No feature scaling required

---

## Workflow
1. Load dataset
2. Perform EDA and visualize feature distributions
3. Handle missing values using appropriate strategies
4. Train Random Forest classifier
5. Evaluate model performance

---

## Technologies Used
- Python
- Jupyter Notebook
- Pandas
- NumPy
- Matplotlib / Seaborn
- Scikit-learn

---

## Key Takeaways
- Missing value imputation should be **data-driven**, not arbitrary
- Median is suitable for continuous or ordinal numeric features
- Mode is more appropriate for discrete or categorical-like features
- Random Forest models are robust but still benefit from thoughtful preprocessing

---

## Author
[Sangeetha james]


