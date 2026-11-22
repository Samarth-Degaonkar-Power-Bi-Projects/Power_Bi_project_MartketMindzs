# MarketMindz: Marketing Campaign and Customer Purchase Analysis | Power BI

An interactive Power BI report that analyzes **2,240 customers** of a food and beverage retailer to answer three questions: which marketing campaigns work, who the buyers are, and what drives purchases. The report is built to help marketing teams target the right customers with the right campaigns and products.

## Dashboard Preview

**1. Campaign Performance**
![Campaign Performance](images/campaign_performance.png)

**2. Buyers Composition**
![Buyers Composition](images/buyers_composition.png)

**3. Purchase Drivers**
![Purchase Drivers](images/purchase_drivers.png)

## Business Questions

- Which campaign generated the most sales?
- Which campaign resulted in the most purchases?
- Which product did buyers purchase in each campaign?
- Which platform is preferred for each campaign?
- What education level do most of our customers have?
- What is the marital status of most of our customers?
- What is the average income by campaign?
- Which product is preferred by each age category?

## Dataset

| File | Description |
|---|---|
| `marketmindz_research_data.csv` | Customer-level data: 2,240 customers, 28 columns, enrolled between July 2012 and June 2014, across 8 countries |
| `marketmindz_research_data_dictionary.csv` | Description of every column |

Main field groups:

| Group | Columns |
|---|---|
| Customer profile | ID, Year_Birth, Education, Marital_Status, Income, Kidhome, Teenhome, Dt_Customer, Country |
| Product spend (last 2 years) | MntWines, MntFruits, MntMeatProducts, MntFishProducts, MntSweetProducts, MntBakedProds |
| Purchase channel | NumWebPurchases, NumCatalogPurchases, NumStorePurchases, NumDealsPurchases, NumWebVisitsMonth, Recency |
| Campaign response | AcceptedCmp1 to AcceptedCmp5, Response (last campaign), Complain |

## Report Pages

### 1. Campaign Performance
Campaign acceptance, sales by campaign, product mix per campaign, platform mix per campaign, and sales by product.

### 2. Buyers Composition
Customer profile by education, marital status, kids at home, and teens at home, plus income and product sales by age group.

### 3. Purchase Drivers
Two **Key Influencers** visuals that show which customer factors (income, age, web visits, country, education) most influence campaign acceptance and total sales, with a product slicer.

## Key Findings

These numbers come from the full dataset (spend is the amount spent over the last 2 years, in the currency of the source data):

- **Campaign 6 generated the most sales:** customers who accepted Campaign 6 (the last campaign) spent about 330K in total, the highest of any campaign. Campaign 5 came second at about 263K.
- **Campaign 6 resulted in the most purchases:** 334 customers accepted its offer, while Campaign 2 came last with only 30.
- **Wine sold the most in every campaign, and fruits sold the least:** wine made up 51% to 69% of spend among customers who accepted each campaign, while fruits was the lowest-selling product overall at about 4% of total spend.
- **Stores are the preferred platform in every campaign:** customers who accepted each campaign made more purchases in stores than on the web. Overall, stores account for 39% of all purchases versus 28% on the web.
- **Income is a strong signal:** the top income quarter spent about 1,358 on average versus 82 for the lowest, and accepted the last campaign at 26.9% versus 10% to 12.5% in the other groups.
- **Most customers hold a Graduation degree, followed by PhD:** among customers who accepted at least one campaign, 298 have a Graduation degree and 158 have a PhD. The same order holds across all 2,240 customers (1,127 Graduation and 486 PhD).
- **Education and response:** customers with a PhD responded the most (20.8%), and those with basic education the least (3.7%).
- **Most customers are married:** 864 customers (38.6%) are married, followed by 580 who are living together.
- **Campaign 5 attracted the highest-income customers:** across the six campaigns, the average income of customers who accepted was about 68.66K, and Campaign 5 had the highest at 82.35K.
- **Wine preference grows with age while meat declines:** wine rises from about 42% of spend among customers aged 25 to 35 to about 54% in the 75 to 85 group, while meat's share gradually falls from about 35% to about 25% to 27% over the same range.

## Data Quality Notes

- 24 customers (about 1%) have a missing Income value.
- The Income column header contains extra spaces in the source file.
- Marital_Status has a few unclear values (Alone, YOLO, Absurd).
- Dt_Customer is stored as text and must be converted to a date.
- Mexico has only 3 customers, so its percentages should not be compared with other countries.

## Tools Used

- Power BI Desktop (data modeling, visuals, Key Influencers)
- CSV data and data dictionary

## Repository Structure

```
.
├── MarketMindz_Marketing_Analysis.pbix        # Power BI report
├── marketmindz_research_data.csv              # Customer dataset
├── marketmindz_research_data_dictionary.csv   # Column descriptions
├── images/
│   ├── campaign_performance.png
│   ├── buyers_composition.png
│   └── purchase_drivers.png
└── README.md
```

## How to Use

1. Download or clone this repository.
2. Open the `.pbix` file in Power BI Desktop.
3. Move through the three pages and use the product slicer on the Purchase Drivers page.
4. If Power BI asks for the data source, point it to `marketmindz_research_data.csv`.

## Possible Next Steps

- Add slicers for country, education, and age group on every page
- Add headline KPI cards (total sales, acceptance rate, top product)
- Add named DAX measures instead of default aggregations
- Segment customers (for example high income, no kids) and compare campaign response

## Author

**Samarth Degaonkar**
Power BI Data Analyst | SQL | Python
[LinkedIn](https://linkedin.com/in/samarth-degaonkar-a76471168) | degaonkar.sam98@gmail.com
