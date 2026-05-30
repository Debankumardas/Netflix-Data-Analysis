# 🎬 Netflix Movies Data Analysis

EDA on a Netflix movies dataset (9,800+ entries) exploring genre trends, popularity, and viewer ratings. Covers data cleaning, feature engineering, and visualizations using Python, Pandas, NumPy, Matplotlib, and Seaborn.

---

## 📌 Questions Explored

1. What is the most frequent genre of movies released on Netflix?
2. Which genre has the highest votes?
3. Which movie has the highest popularity? What is its genre?
4. Which movie has the lowest popularity? What is its genre?
5. Which year had the most movies filmed?

---

## 📂 Dataset

**File:** `mymoviesdb.csv`  
**Rows:** 9,826 movies  
**Columns:** `Release_Date`, `Title`, `Overview`, `Popularity`, `Vote_Count`, `Vote_Average`, `Original_Language`, `Genre`, `Poster_Url`

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| Python | Core language |
| Pandas | Data manipulation |
| NumPy | Numerical operations |
| Matplotlib | Plotting |
| Seaborn | Statistical visualizations |

---

## 🔍 Project Workflow

### 1. Data Exploration
- Loaded and inspected the dataset using `.head()`, `.info()`, `.describe()`
- Checked for duplicates and null values
- Identified non-numeric values in `Vote_Count` and `Vote_Average`

### 2. Data Cleaning
- Cast `Vote_Count` and `Vote_Average` to numeric types, coercing errors
- Dropped rows with missing values in key columns
- Converted `Release_Date` to datetime and extracted the year
- Dropped irrelevant columns: `Overview`, `Original_Language`, `Poster_Url`

### 3. Feature Engineering
- Categorized `Vote_Average` into 4 labels: `not_popular`, `below_avg`, `average`, `popular`
- Split multi-genre strings (comma-separated) and exploded the DataFrame for one genre per row
- Cast `Genre` column to category type

### 4. Data Visualization
- **Genre distribution** — horizontal bar chart showing the most frequent genres
- **Vote distribution** — count plot for vote categories across genres
- **Popularity extremes** — identified highest and lowest popularity movies
- **Release year trend** — histogram showing movie volume by year

---

## 📊 Key Findings

- **Most frequent genre:** Drama dominates Netflix's catalog
- **Highest popularity movie:** Identified with its genre using `.max()` filter
- **Most active release year:** Visible spike in recent years from the histogram
- **Vote distribution:** Majority of movies fall in the `average` and `below_avg` categories

---

## 📁 Project Structure

```
netflix-movies-analysis/
│
├── Movie_data_analysis.ipynb   # Main analysis notebook
├── mymoviesdb.csv              # Dataset
└── README.md                   # Project documentation
```

---

## 📃 License

This project is open source and available under the [MIT License](LICENSE).
