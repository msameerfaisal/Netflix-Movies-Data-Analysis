# Netflix Movies and TV Shows — Data Analysis

A beginner-friendly exploratory data analysis (EDA) of Netflix's content catalog. This is my first end-to-end data analysis project using pandas and matplotlib, completed as part of my data science learning journey in summer 2026.

## About the Dataset

The dataset is the popular [Netflix Movies and TV Shows dataset from Kaggle](https://www.kaggle.com/datasets/shivamb/netflix-shows). It contains around 8,800 titles available on Netflix, with columns for:

- `show_id`, `type` (Movie or TV Show), `title`
- `director`, `cast`, `country`
- `date_added` (when the title was added to Netflix), `release_year`
- `rating`, `duration`
- `listed_in` (genres), `description`

## Questions Explored

I focused on three questions:

1. **How has the number of titles added to Netflix changed over the years?**
2. **Which countries produce the most content, and how does it split between Movies and TV Shows?**
3. **What are the top 10 genres on Netflix, separated by Movies and TV Shows?**

## Key Findings

### 1. Netflix's library grew explosively between 2015 and 2019

Title additions were near zero from 2008 to 2014, then grew rapidly, peaking at roughly 2,000 titles added in 2019. The number declined in 2020 and 2021, which could reflect either the end of the dataset, the impact of COVID-19 on production, or a strategic shift toward fewer but bigger original productions.

### 2. US dominates, but the global picture differs by content type

The United States is the top content producer in both Movies and TV Shows. However, the second tier looks very different between the two:

- **Movies:** India is a clear second (largely Bollywood), followed by the UK, Canada, and France.
- **TV Shows:** Asian markets dominate the next tier — UK, Japan, South Korea, India, and Taiwan are all major contributors, reflecting the global rise of anime and K-drama.

*Note: Co-productions are attributed to all participating countries (using pandas `explode`). For example, a title listed as "United States, India" is counted once for each country.*

### 3. Netflix is fundamentally an international platform

"International Movies" and "International TV Shows" are the #1 genre in their respective categories. This confirms what the country analysis showed: Netflix's catalog is globally sourced, not US-centric. The Movies side leans toward classic genres (Dramas, Comedies, Documentaries, Action), while the TV Shows side reflects the global trend — Anime Series and British TV Shows appear as distinct genre categories.

## Tools Used

- Python 3
- pandas (data cleaning, grouping, exploring)
- matplotlib (visualization)
- Jupyter Notebook

## How to Reproduce

1. Clone this repository:
```bash
   git clone https://github.com/msameerfaisal/Netflix-Movies-Data-Analysis.git
```
2. Install the required packages:
```bash
   pip install pandas matplotlib jupyter
```
3. Open `Netflix Movies Data Analysis.ipynb` in Jupyter Notebook and run the cells top to bottom.

The dataset (`Netflix.csv`) is included in the repository.

## What I Learned

This project taught me several real-world data analysis skills:

- **Question-driven cleaning** rather than upfront blanket cleaning of every column
- **Handling comma-separated values** in single cells using `str.split()` and `explode()`
- **The importance of `str.strip()`** to handle leading/trailing whitespace after splitting
- **Choosing the right matplotlib interface** (object-oriented with `fig, ax = plt.subplots()`) for multi-subplot charts
- **Writing analysis findings honestly** — offering multiple possible explanations for trends rather than overclaiming

## About Me

I'm a 17-year-old student from Karachi, Pakistan, learning data science as part of my preparation for university applications. This project is part of an ongoing summer 2026 learning roadmap. You can see my other projects on [my GitHub profile](https://github.com/msameerfaisal).

---

*If you have suggestions or spot something I could do better, I'd genuinely appreciate the feedback.*