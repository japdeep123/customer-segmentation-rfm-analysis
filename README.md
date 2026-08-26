# Customer Segmentation + RFM Analysis

An Excel dashboard applying the RFM (Recency, Frequency, Monetary) framework to segment an e-commerce customer base into actionable groups, validate the Pareto principle, and prioritize retention spend where it protects the most revenue.

## 📌 Project Overview

Using 7,000 transactions from 500 customers (FY 2022–2023), this project scores every customer on Recency, Frequency, and Monetary value, classifies them into 9 industry-standard RFM segments, and builds a dashboard to answer the core question every retention strategy depends on: which customers matter most, and what should be done about each group.

## 🎯 Business Objective

- Segment the customer base into behaviorally distinct groups using the RFM model
- Test whether the Pareto principle (80/20 rule) holds for this business
- Identify which segments carry the highest immediate churn/revenue risk
- Determine which product categories and geographies deserve the most marketing investment
- Translate segment-level findings into specific retention actions per group

## 🛠️ Tools & Techniques

- **Microsoft Excel** — dashboard design and RFM scoring logic
- **Power Query** — data import, cleaning, and merging across Transactions, Customers, and Products tables
- **Power Pivot & DAX** — star schema data model and KPI measures (Total Revenue, Total Customers, Avg Order Value, Champions Revenue, At Risk Count)
- **Excel formulas** — IFS (RFM scoring & segmentation logic), MAXIFS, COUNTIF/SUMIF, AVERAGEIF, IFERROR, UNIQUE()
- **Pivot Tables & Pivot Charts** — 6 dashboard visualizations driven by dynamic slicers (AgeGroup, Country, Segment)

## 🧮 RFM Methodology

Each customer is scored 1–5 on three dimensions, using **Net Revenue (Revenue × (1 − Discount))** for Monetary value to reflect true realized value rather than gross billing:

| Metric | Definition | Business Meaning |
|---|---|---|
| **Recency (R)** | Days since last purchase | Recent buyers are more likely to buy again |
| **Frequency (F)** | Total orders placed | Frequent buyers show stronger engagement |
| **Monetary (M)** | Total net revenue generated | High spenders drive disproportionate revenue |

Combined scores map to 9 segments: **Champions, Loyal Customers, Potential Loyalists, New Customers, Promising, Need Attention, About to Sleep, At Risk, Lost.**

## 📊 Key Insights

| Metric | Value |
|---|---|
| Total Customers | 500 |
| Total Orders | 7,000 |
| Total Revenue | ₹7.59Cr (75.92M) |
| Avg Order Value | ₹10.85K |
| Champions Revenue | ₹3.76Cr (37.60M) |
| At Risk Count | 26 |

**Findings:**
- **Pareto principle confirmed** — Champions (40% of customers) drive 49.5% of revenue; Champions + Loyal Customers together account for 89.5% of revenue from 81.4% of customers.
- **Champions are the clear priority** — 200 customers, ₹3.76Cr in revenue, averaging just 17.6 days since last purchase and 17.3 orders. Recommended action: VIP loyalty program, early access, and referral incentives.
- **"About to Sleep" is the highest immediate risk** — 25 previously active customers (₹20.7L revenue) have gone quiet, averaging 55.8 days since last purchase. A 15% discount + FOMO win-back campaign within 30 days is recommended before they convert to "Lost."
- **Recency is the strongest churn signal** — Champions sit at 17.6 days since last purchase vs. 132.8 days for Need Attention and 127 days for At Risk, a 7–8x gap that outweighs frequency as a predictor of disengagement.
- **Electronics and Sports lead category revenue** — ₹1.75Cr and ₹1.70Cr respectively (45.5% combined), making them the primary offer focus for Champion/Loyal re-engagement campaigns.
- **Germany, India, and Canada drive over half of revenue** — 54.6% combined, informing a proposed regional marketing split (Germany 25%, India 20%, Canada 20%, UK 15%, USA 15%, France 5%).

## 👥 Segment Breakdown

| Segment | Customers | Revenue (₹) | Rev % | Avg Recency | Avg Frequency | Recommended Action |
|---|---|---|---|---|---|---|
| Champions | 200 | 3,75,97,812 | 49.5% | 17.6 days | 17.3 | Reward + advocacy program |
| Loyal Customers | 207 | 3,03,57,687 | 40.0% | 28.6 days | 12.7 | Upsell + cross-sell |
| Potential Loyalists | 40 | 33,91,594 | 4.5% | 22.7 days | 11.4 | Nurture to loyalty |
| About to Sleep | 25 | 20,70,409 | 2.7% | 55.8 days | 7.8 | 15% discount + FOMO campaign |
| New Customers | 19 | 15,98,359 | 2.1% | 13.7 days | 8.3 | Onboarding + 2nd purchase push |
| Need Attention | 4 | 4,95,924 | 0.7% | 132.8 days | 12.5 | Re-engage urgently |
| Promising | 3 | 2,37,749 | 0.3% | 94.7 days | 10.7 | Activation + education |
| At Risk | 1 | 1,25,867 | 0.2% | 127.0 days | 9.0 | Win-back email + survey |
| Lost | 1 | 46,354 | 0.1% | 5.0 days | 10.0 | Minimal investment |

## 💡 Strategic Recommendations

- **Protect ₹7.93Cr** in Champions + Loyal Customers revenue through a dedicated VIP retention program.
- **Recover ₹21.96L** in at-risk revenue via a time-boxed win-back campaign targeting "About to Sleep" and "At Risk" segments.
- **Convert Potential Loyalists to Loyal** — 40 customers represent a potential ₹3.4Cr uplift if nurtured effectively.
- **Concentrate 90% of retention marketing budget** on the top 3 segments by revenue contribution rather than spreading spend evenly across all 9.

## 🏗️ Data Model

Built as a star schema in Power Pivot with relationships:
`Transactions[CustomerID] → Customers[CustomerID]`
`Transactions[ProductID] → Products[ProductID]`
`Transactions[InvoiceDate] → Calendar[Date]`

## 📁 Repository Contents

- `Dashboard_RFM_Customer_Segmentation.xlsx` — Interactive Excel dashboard with RFM scoring, segmentation logic, and Power Pivot data model
- `Dashboard_Images_RFM_Analysis.pdf` — Dashboard visual reference
- `RFM_Project_Business_Guide.pdf` — Full methodology, segment definitions, and business Q&A documentation

## 🏷️ Project Type

Training Project — Big 4 consulting standard framework (RFM methodology used by McKinsey, BCG, Deloitte, PwC for customer strategy)

## 👤 Author

**Japdeep Singh**
Portfolio: [japdeep123.github.io/portfolio](https://japdeep123.github.io/portfolio/)
