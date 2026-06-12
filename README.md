# 🎬 Netflix Titles — Exploratory Data Analysis

A data analysis project that explores the Netflix titles dataset to uncover trends, patterns, and insights about the platform's content library.


## 📁 Dataset

- **File:** `netflix_titles.csv`
- **Records:** 8,807 rows × 12 columns
- **Columns:** `show_id`, `type`, `title`, `director`, `cast`, `country`, `date_added`, `release_year`, `rating`, `duration`, `listed_in`, `description`

## 🛠️ Tech Stack

| Library | Purpose |
|---|---|
| `pandas` | Data loading, cleaning, and analysis |
| `matplotlib` | Core plotting |
| `seaborn` | Statistical visualizations |


## 📋 Project Structure

## 🔍 Steps Covered

### Step 1 — Load & Inspect
- Loaded the dataset and examined shape, data types, null values, and duplicates.
- Found no duplicate records; identified missing values primarily in `director`, `cast`, `country`, `rating`, `duration`, and `date_added`.

### Step 2 — Data Cleaning
| Column | Missing Values | Action Taken |
|---|---|---|
| `director` | ~30% (2,634) | Dropped — too many nulls, text data unsuitable for imputation |
| `cast` | ~9.4% (825) | Filled with `"Unknown"` |
| `country` | ~9.4% (831) | Filled with `"Unknown"` |
| `rating` | 4 | Filled with mode |
| `duration` | 3 | Filled with `"Unknown"` |
| `date_added` | 10 | Filled with `"Unknown"` |

### Step 3 — Exploratory Data Analysis (EDA)

Key questions answered:

- **Which countries have the most Netflix titles?**
  → USA (2,818), India (972), UK (419)

- **What is the most common content rating?**
  → TV-MA with 3,212 titles (mature audiences)

- **Movies vs TV Shows?**
  → 6,131 Movies vs 2,666 TV Shows

- **Which year had the most releases?**
  → 2018 with 1,146 titles

- **Content split by percentage?**
  → 69.69% Movies, 30.31% TV Shows

### Step 4 — Visualizations

8 charts were created to support the analysis:

1. **Bar Chart** — Top 10 release years by number of titles
2. **Bar Chart (Seaborn)** — Top 10 most frequent individual actors
3. **Histogram** — Movies vs TV Shows distribution
4. **Pie Chart** — Content released before vs after 2000
5. **KDE + Histogram** — Distribution of release years (movies only)
6. **Box Plot** — Spread of numeric variables
7. **Heatmap** — Correlation between release year and movie duration
8. **Bubble Plot** — Release year vs duration for movies

### Step 5 — Insights Report

- Movies make up ~70% of Netflix's catalog, significantly outnumbering TV Shows.
- The United States dominates content production by a wide margin.
- Content output surged sharply after 2010, reflecting Netflix's aggressive expansion.
- Most titles fall in the 2013–2019 range; older content appears as outliers.
- 592 titles were added after 2020, showing Netflix's commitment to fresh content.


## 💡 Key Findings

> The most unexpected finding was how heavily Netflix skews toward Movies (nearly 70%) and how dominant US-produced content is across the platform. The sharp content growth post-2010 also stands out as a defining trend.

---

## 🚀 How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/netflix-eda.git
   cd netflix-eda
   ```

2. Install dependencies:
   ```bash
   pip install pandas matplotlib seaborn
   ```

3. Download the dataset from [Kaggle — Netflix Movies and TV Shows](https://www.kaggle.com/datasets/shivamb/netflix-shows) and place `netflix_titles.csv` in the project root.

4. Open and run the notebook:
   ```bash
   jupyter notebook project_1_.ipynb
   ```

---

## 📊 Dataset Source

[Netflix Movies and TV Shows — Kaggle](https://www.kaggle.com/datasets/shivamb/netflix-shows)

---

## 📄 License

This project is for educational purposes only.
