# Runtime and Ratings: Are Longer Horror Movies Better (or Scarier)?

**Date:** 2024-10-15

## 📚 Project Purpose
Inspired by the Halloween season, this project investigates whether longer horror movies are rated better than shorter ones. As busy students with limited time, understanding if longer movies provide a better viewing experience can help in deciding whether to allocate extra time for them.

**Population:** All horror movies listed on IMDb.

**Sample:** 42,758 horror movies identified using IMDb’s advanced title search.

**Variable of Interest:** Average IMDb User Rating (1-10 scale).

**Factor:** Movie runtime.

**Parameter:** Testing if there is a significant difference in average IMDb ratings between long and short horror movies.

---

## 📊 Data Collection
- Initial search included Kaggle datasets and Canadian public polling data.
- Final dataset selected: **IMDb Horror: Chilling Movie Dataset** from Kaggle.
- Contains 837 horror movies with over 25,000 reviews each.
- Dataset has columns like runtime, rating, genre, gross profits, and release date.
- Minimal cleaning needed; licensed under CC0.

---

## 🔍 Statistical Analysis
### Libraries Used
- `mosaic`
- `ggplot2`

### Exploratory Data Analysis (EDA)
- Histograms and boxplots for `Rating` and `Runtime`
- Defined:
  - **Long movies**: Runtime ≥ Q3 (108 minutes)
  - **Short movies**: Runtime ≤ Q1 (91 minutes)
- Scatter plot indicated a slight positive correlation between runtime and ratings.

### Hypothesis Testing
- Null Hypothesis ($H_0$): Mean rating of long movies = Mean rating of short movies.
- Alternative Hypothesis ($H_A$): Mean rating of long movies ≠ Mean rating of short movies.
- Significance level ($\alpha$): 0.05
- Normality checked via QQ plots.
- Variances unequal → Used Welch’s t-test.

**Result:**
- p-value = 2.197e-11 < 0.05 → **Reject $H_0$**.
- Conclusion: Statistically significant difference between long and short movie ratings.

### Confidence Interval Testing (Bootstrap)
- Bootstrapped 2000 samples of mean differences.
- 95% Confidence Interval: (0.426, 0.777)
- 0 not captured → **Significant difference confirmed**.

---

## ✅ Conclusion
- Longer horror movies tend to have higher IMDb ratings than shorter horror movies.
- Horror fans are encouraged to invest time in longer movies for a better viewing experience.
- The project provided practical learning in hypothesis testing, confidence intervals, data sourcing, and real-world data handling.

---

## 📚 References
- Chen, G. (2024). University of Calgary Course Materials.
- IMDb. (n.d.). Advanced Search, Press Room, and IMDb Help pages.
- IMDb Horror: Chilling Movie Dataset (2023). Kaggle.
- R Core Team (2021). R: A language and environment for statistical computing.
- Wickham, H. (2016). *ggplot2: Elegant Graphics for Data Analysis*.
- Wickham, H. et al. (2019). *Welcome to the tidyverse*.

---

**Note:** All data analyses were performed using R and ggplot2 libraries.
