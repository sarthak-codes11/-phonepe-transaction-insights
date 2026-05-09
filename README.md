# PhonePe Transaction Insights

Analysis of PhonePe's publicly available pulse data to uncover transaction trends, user engagement patterns, and geographic insights across India.

## Project Type
Exploratory Data Analysis + Regression

## Domain
Finance / Digital Payments

---

## Problem Statement

With the increasing reliance on digital payment systems like PhonePe, understanding transaction dynamics, user engagement, and geographic distribution is critical for improving services and targeting users effectively. This project analyzes aggregated transaction and user data across all Indian states from 2018 to 2024.

---

## Dataset

Source: [PhonePe Pulse GitHub Repository](https://github.com/PhonePe/pulse)

Three main datasets were extracted from the JSON files:

| Dataset | Description | Shape |
|---|---|---|
| df_agg_trans | Aggregated transactions by state, year, quarter and payment type | (5034, 6) |
| df_agg_user | Registered users and app opens by state and year | (1008, 5) |
| df_map_trans | District level transaction counts and amounts | (20604, 6) |

---

## Tech Stack

- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn
- SciPy
- Jupyter Notebook

---

## Project Structure

```
phonepe/
├── pulse/                  # PhonePe raw JSON data (cloned from PhonePe/pulse)
├── Sample_ML_Submission_Template-2.ipynb   # Main analysis notebook
└── README.md
```

---

## Key Findings

- Merchant payments and peer to peer payments account for the majority of transaction value on PhonePe
- Telangana, Maharashtra and Karnataka are the top three states by transaction amount
- Registered users and transaction amounts have a Pearson correlation of 0.90 confirming user acquisition directly drives revenue
- Transaction amounts in 2023 are significantly higher than 2019 confirmed via independent T-test (p < 0.05)
- Q3 and Q4 see higher transaction volumes driven by festive season spending
- App opens are growing faster than registrations in recent years indicating improving user engagement

---

## Hypothesis Testing

| Hypothesis | Test Used | Result |
|---|---|---|
| Registered users correlate with transaction amount | Pearson Correlation | r = 0.90, p = 0.0000, Rejected H0 |
| Transaction amounts differ across payment types | One-way ANOVA | F = 206.37, p = 0.0000, Rejected H0 |
| Transaction amounts grew from 2019 to 2023 | Independent T-test | t = 8.77, p = 0.0000, Rejected H0 |

---

## ML Models Used

- Random Forest Regressor
- Linear Regression
- Gradient Boosting Regressor

---

## How to Run

1. Clone the PhonePe pulse data:
```bash
git clone https://github.com/PhonePe/pulse.git
```

2. Clone this repository:
```bash
git clone https://github.com/sarthak-codes11/-phonepe-transaction-insights.git
```

3. Place both folders in the same directory so the structure looks like:
```
phonepe/
├── pulse/
└── Sample_ML_Submission_Template-2.ipynb
```

4. Open Jupyter Notebook from that directory:
```bash
jupyter notebook
```

5. Run all cells top to bottom using Kernel → Restart & Run All

---

## Author

Sarthak
