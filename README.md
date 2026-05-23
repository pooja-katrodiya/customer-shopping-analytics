# Customer Revenue & Shopping Behavior Analytics

## Project Overview
End-to-end data analytics pipeline analyzing **3,900 customer transaction records** to uncover revenue patterns, discount effectiveness, seasonal trends, and customer segment behavior.

**Tools:** Python · PostgreSQL · Pandas · Matplotlib · Seaborn  
**Skills:** ETL, Data Cleaning, EDA, SQL Analytics, Data Visualization, Business Insights

---

## Business Questions Answered
- Which product categories and customer segments drive the most revenue?
- Do discounts actually increase spending — or just attract low-value transactions?
- Which season has the highest customer spending?
- How do subscribers differ from non-subscribers in spending behavior?
- Which customers spend the most, and what do they buy?

---

## Project Structure
```
customer-shopping-analytics/
│
├── customer_shopping_behavior.csv   # Raw dataset (3,900 records)
├── customer_analysis.ipynb          # Main EDA + SQL analysis notebook
├── charts/                          # Generated visualizations
│   ├── revenue_by_category.png
│   ├── revenue_by_gender.png
│   ├── seasonal_revenue.png
│   ├── discount_impact.png
│   ├── revenue_by_age_group.png
│   └── purchase_frequency.png
└── README.md
```

---

## Key Findings

| Finding | Detail |
|---------|--------|
| 🏆 **Clothing dominates revenue** | $104,264 — 44.7% of total revenue |
| 📅 **Fall is peak season** | Highest avg purchase at $61.56 vs $58.41 in Summer |
| 🏷️ **Discounts don't lift basket size** | Discounted avg purchase ($59.28) is lower than non-discounted ($60.13) |
| 👩 **Female customers spend more per transaction** | $60.25 vs $59.54 — opportunity to grow female segment |
| 🔁 **Subscribers are underrepresented** | Only 27% of customers — strong retention opportunity |

---

## Pipeline Summary

```
Raw CSV → Data Cleaning → Feature Engineering → EDA → SQL Analytics → Insights
```

1. **Data Cleaning** — Imputed 37 missing Review Ratings using category-level median; dropped duplicate column (`promo_code_used == discount_applied`)
2. **Feature Engineering** — Created `age_group` using quartile-based binning (`pd.qcut`)
3. **ETL to PostgreSQL** — Loaded cleaned data into PostgreSQL via SQLAlchemy
4. **EDA** — 5 visualizations covering revenue by category, gender, season, discount impact, and age group
5. **SQL Analytics** — 5 business queries including subquery for above-average discount spenders and cross-tab revenue pivot

---

## How to Run

```bash
# Install dependencies
pip install pandas matplotlib seaborn sqlalchemy psycopg2-binary

# Run the notebook
jupyter notebook customer_analysis.ipynb
```

> **Note:** To use the PostgreSQL connection, set your database password as an environment variable:
> ```bash
> export DB_PASSWORD=your_password_here
> ```

---

*Pooja Katrodiya | [LinkedIn](https://www.linkedin.com/in/poojakatrodiya/) | [Portfolio](https://pooja-katrodiya.github.io/github-portfolio)*
