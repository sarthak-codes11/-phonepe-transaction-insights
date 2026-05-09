## Approach

1. **Data Extraction** — Cloned PhonePe pulse repository and parsed nested JSON files into structured Pandas dataframes
2. **EDA** — 15 charts covering univariate, bivariate and multivariate analysis following the UBM rule
3. **Hypothesis Testing** — Pearson correlation, One-way ANOVA and Independent T-test
4. **Feature Engineering** — Label encoding, outlier capping, power transformation, standard scaling and new feature creation
5. **ML Models** — Regression models to predict transaction amounts with hyperparameter tuning

## Key Insights

- Merchant payments and peer to peer payments dominate transaction value on PhonePe
- Telangana, Maharashtra and Karnataka are the top states by transaction amount
- Registered users and transaction amounts have a Pearson correlation of 0.90 confirming user acquisition drives revenue
- Transaction amounts in 2023 are significantly higher than 2019 confirmed via T-test
- Q3 and Q4 show higher transaction volumes driven by festive season spending

## Tech Stack

- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn
- Scipy
- Jupyter Notebook

## How to Run

1. Clone this repository
2. Clone PhonePe pulse data into the same folder
```bash
git clone https://github.com/PhonePe/pulse.git
```
3. Open Jupyter Notebook
```bash
jupyter notebook
```
4. Run all cells top to bottom using Kernel → Restart & Run All

## Business Use Cases Addressed

- Customer segmentation by state and transaction type
- Geographical insights for targeted marketing
- Payment performance evaluation across categories
- User engagement trend analysis
- Trend analysis for demand forecasting

## Author
Sarthak Deore