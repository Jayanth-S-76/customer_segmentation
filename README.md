# Customer Segmentation Analysis
> Data-driven customer grouping and targeted marketing strategy for the U.S. retail market.

## Project Overview

This project analyzes shopping behavior of **3,900 U.S. customers** to uncover patterns in purchasing habits, payment preferences, and seasonal trends. The goal is to segment customers into distinct groups and derive actionable marketing strategies for each segment.

The analysis addresses four key business questions:
- Which product categories should receive discounts — and why?
- How does card spending vary across age groups?
- When and where do customers spend the most (seasonal & regional trends)?
- How can customers be clustered into targetable groups?

---

## Tech Stack

| Tool | Purpose |
|------|---------|
| Python | Core analysis and scripting |
| Pandas | Data manipulation and aggregation |
| Scikit-learn | K-Means clustering |
| Excel / Pivot Tables | Exploratory summaries (discount, age, location) |
| Matplotlib / Seaborn | Data visualization |
| PowerPoint (python-pptx) | Presentation generation |

---

## Dataset

**File:** `project_shopping_trends.xlsx`  
**Records:** 3,900 customers · 18 attributes

| Attribute | Description |
|-----------|-------------|
| Age | Customer age |
| Gender | Male / Female |
| Category | Clothing, Footwear, Accessories, Outerwear |
| Purchase Amount (USD) | Transaction value |
| Location | U.S. state |
| Season | Fall / Spring / Summer / Winter |
| Review Rating | 1–5 star rating |
| Discount Applied | Whether a discount was used (Yes/No) |
| Promo Code Used | Whether a promo code was used (Yes/No) |
| Previous Purchases | Count of past transactions |
| Payment Method | Credit Card, Debit Card, PayPal, Venmo, Cash, Bank Transfer |
| Frequency of Purchases | Weekly / Fortnightly / Monthly / Quarterly / Annually |

---

## Analysis Methodology

### 1. Discount Strategy
Calculated per category: total revenue, average purchase value, discount usage rate, and average review rating. Categories were mapped on a **Revenue × Discount Dependency** matrix to determine whether discounts are necessary or wasteful for each.

### 2. Card Spending by Age
Customers were grouped into three age bands (18–30, 31–50, 51+). Average card usage rate and average purchase amount were computed per group to identify payment preferences and spending behavior by age.

### 3. Seasonal & Location Analysis
A pivot table summed purchase amounts by U.S. state and season. Top-spending states per season were identified to guide regional campaign scheduling.

### 4. Customer Clustering (K-Means)
Numerical features (Age, Purchase Amount, Review Rating, Previous Purchases) were used as input to a **K-Means clustering algorithm** with K=3. Three was chosen to keep clusters actionable for marketing teams. Cluster profiles were derived by analyzing the mean values and behavioral patterns within each group.

---

## Results & Insights

### Discount Strategy

| Category | Total Revenue | Avg Purchase | Discount Rate | Avg Rating | Recommendation |
|----------|--------------|--------------|---------------|------------|----------------|
| Clothing | $104,264 | $60.03 | 42.1% | 3.72 | Core line — light promos only |
| Accessories | $74,200 | $59.84 | 43.8% | 3.77 | Bundle deals & BOGO offers |
| Footwear | $36,093 | $60.26 | 43.2% | 3.79 ⭐ | Market as premium — use reviews as ads |
| Outerwear | $18,524 | $57.17 | 44.4% | 3.75 | Heavy promos / clearance needed |

### Card Spending by Age

| Age Group | Card Usage | Avg Purchase |
|-----------|-----------|--------------|
| Younger (18–30) | 33.72% | $60.36 |
| Middle-aged (31–50) | 35.12% | $59.20 |
| Older (51+) | 33.27% | $59.95 |

> Spending amounts are nearly identical across age groups. The key differentiator is **payment preference**, not spending power. Middle-aged customers are the most card-reliant; older customers prefer cash and bank transfers.

### Seasonal Highlights

| Season | Top States |
|--------|-----------|
| Fall | Texas, California, Idaho, Illinois |
| Summer | Pennsylvania, Montana, North Dakota |
| Spring | Nevada, Alaska, Illinois, North Carolina |
| Winter | Vermont, Virginia, Montana, Rhode Island |

### Customer Clusters

| Cluster | Label | Size | Avg Age | Avg Spend | Past Orders | Strategy |
|---------|-------|------|---------|-----------|-------------|---------|
| 0 | Loyal High-Spenders | 1,168 | 46 | $76.63 | 38 | Loyalty rewards, exclusive offers |
| 1 | Budget Frequent Shoppers | 1,533 | 46 | $35.83 | 26 | Flash sales, promo codes, BOGO |
| 2 | High-Spend New Explorers | 1,199 | 40 | $73.94 | 12 | Onboarding campaigns, first-purchase incentives |

---

## Key Takeaways

1. **Outerwear** is the only category that is both low-revenue and heavily discount-dependent — it needs repositioning or clearance pricing.
2. **Footwear** has the highest review ratings and should be marketed on quality, not price.
3. **Regional campaigns** outperform national ones — summer spending peaks in rural western states, not just major cities.
4. **Cluster 2** (younger, high-spend, low history) represents the biggest growth opportunity — converting them to loyal customers has the highest ROI.

---

## Project Structure

```
├── project_shopping_trends.xlsx   # Raw dataset + pivot analyses
├── customer_clusters.xlsx         # Dataset with cluster labels assigned
├── analysis/
│   └── segmentation.py            # Clustering and analysis script
├── CustomerSegmentation.pptx      # Final presentation
└── README.md
```

---

## Author

Internship Project — Data Analyst Role  
Dataset: U.S. Customer Shopping Trends (3,900 records)
