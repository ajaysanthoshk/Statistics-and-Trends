# Apple Quality Analysis: Exploratory Data Analysis (EDA)

## 🍎 Project Overview
This project performs an **Exploratory Data Analysis (EDA)** on the **Apple Quality Dataset** from Kaggle. The goal is to uncover patterns and relationships between apple attributes—such as size, weight, acidity, sweetness, crunchiness, juiciness, and ripeness—and how they influence overall apple quality.

---

## 📊 Dataset Information
**Source:** [Kaggle - Apple Quality Dataset](https://www.kaggle.com/datasets/nelgiriyewithana/apple-quality)  
**Rows:** 4,000 observations  
**Columns:** 8 numerical features + target variable (quality)

| Column | Description |
|--------|-------------|
| A_id | Apple identifier |
| Size | Apple size (in cm) |
| Weight | Apple weight (in grams) |
| Sweetness | Sweetness level |
| Crunchiness | Crunchiness measure |
| Juiciness | Juiciness level |
| Ripeness | Ripeness level |
| Acidity | Acidity level |
| Quality | Target variable (good/bad) |

### Descriptive Statistics
| Metric | Size | Weight | Acidity |
|--------|------|--------|---------|
| Mean | ~1.5 cm | 0.07 | 2.11 |
| Std Dev | 1.92 cm | 2.11 | - |
| Range | -2 to +6 cm | 0–500 g | Varies |
| Observations | 4000 | 4000 | 4000 |

---

## 📈 Visualizations & Analysis

### 1. **Histogram: Size vs. Weight Distribution**
- **Bins:** 20
- **Observation:** Weight ranges from 0–500g, showing broad market variation.
- **Shape:** Slightly skewed toward the center, indicating most apples fall in the mid-range of size and weight.

### 2. **Scatter Plot: Juiciness vs. Ripeness**
- **Axes:** Log-scale for ripeness (y) vs. juiciness (x)
- **Correlation:** Slightly negative (-6 to 8 range)
- **Insight:** Apple quality is closely tied to juiciness and ripeness. Optimal values cluster near 0.

### 3. **Correlation Heatmap**
Key correlations observed:
- **Weight & Size** → Positive (0.6–0.8) with sweetness → Medium-sized apples tend to be sweeter.
- **Acidity & Ripeness** → Strong negative (-0.3) → Overripe apples have higher acidity.
- **Crunchiness & Juiciness** → Positive (0.4) → Juicier apples are crunchier.

| Feature | Size | Weight | Sweetness | Crunchiness | Juiciness | Ripeness | Acidity |
|---------|------|--------|-----------|-------------|-----------|----------|---------|
| Size | 1.00 | 0.17 | 0.32 | 0.17 | 0.02 | 0.12 | 0.20 |
| Weight | 0.17 | 1.00 | 0.19 | 0.09 | 0.03 | 0.24 | 0.016 |
| Sweetness | 0.32 | 0.19 | 1.00 | 0.08 | 0.06 | 0.27 | 0.086 |
| Crunchiness | 0.17 | 0.09 | 0.08 | 1.00 | 0.26 | 0.20 | 0.07 |
| Juiciness | 0.02 | 0.03 | 0.06 | 0.26 | 1.00 | 0.097 | 0.23 |
| Ripeness | 0.12 | 0.24 | 0.27 | 0.20 | 0.097 | 1.00 | 0.20 |
| Acidity | 0.20 | 0.016 | 0.086 | 0.07 | 0.23 | 0.20 | 1.00 |

---

## 🔍 Key Insights

1. **Size & Weight** are positively correlated with sweetness, suggesting that medium-sized apples are often sweeter.
2. **Acidity** increases with overripeness (negative correlation with ripeness).
3. **Crunchiness and juiciness** are positively related—juicier apples tend to be crunchier.
4. **Quality distribution** is centered, indicating most apples fall within a standard range of attributes.
5. **Juiciness and ripeness** show a log-scale relationship, with optimal quality near balanced values.

---

## 🛠 Tools & Techniques

### Libraries Used:
- Python (Pandas, NumPy, Matplotlib, Seaborn)
- Jupyter Notebook for interactive analysis

### Methods:
- Descriptive statistics (mean, std, range)
- Histogram and scatter plot visualization
- Correlation matrix and heatmap
- Log-scale transformation for skewed data

---

## 📌 Conclusions
- Apple quality is influenced by multiple interacting factors.
- Optimal apples balance juiciness, ripeness, and acidity.
- Size and weight are reliable indicators of sweetness.
- Overripeness leads to increased acidity, which may reduce quality.

---

## 🚀 Future Work
- Build a classification model to predict apple quality.
- Perform feature engineering to highlight key attributes.
- Explore clustering to group apples by quality profiles.
- Conduct sensitivity analysis on ripeness and acidity thresholds.

---

## 👨‍💻 Author

**Ajay Santhosh Kavitha Veeramani**  


---

*This project was completed as part of the Applied Data Science course at the University of Hertfordshire.*
