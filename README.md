# Customer Segmentation & Retention Analytics | Power BI

## Project Overview

An interactive Power BI project designed to analyze customer segments, historical spending, purchase behavior, and customer retention indicators. The dashboard helps stakeholders understand customer value, identify at-risk customers, and develop data-driven marketing and retention strategies.

## Objective

- Segment customers using Recency, Frequency, and Monetary (RFM) analysis.
- Monitor customer count, historical spend, repeat customer rate, and retention-status indicators.
- Compare customer segments by size and spending.
- Identify high-value and at-risk customer groups.
- Support targeted marketing, customer loyalty, and retention decisions.

## Tools Used

- **Power BI Desktop** — Dashboard development and data visualization
- **Power Query** — Data cleaning and transformation
- **DAX** — Measures, calculated columns, KPI calculations, and RFM scoring
- **Microsoft Excel / CSV** — Dataset storage and source data
- **GitHub** — Project versioning and portfolio publishing

## Dataset Description

The project uses a synthetic customer-level dataset containing 150 customer records.

The dataset includes customer identifiers, demographic information, location, join date, last purchase date, purchase frequency, total historical spend, loyalty tier, preferred product category, purchase channel, satisfaction score, and other customer attributes.

Each row represents one customer.

**Data limitation:** The dataset is a customer snapshot rather than transaction-level history. Historical spend represents recorded customer-level spend, not a monthly revenue series. Retention status is estimated from purchase recency and should be interpreted as a retention proxy.

## Power Query Steps

The data preparation process includes:

1. Imported the customer dataset into Power BI Desktop.
2. Reviewed column names and data types.
3. Converted join date and last purchase date fields to Date.
4. Checked customer identifiers and relevant numeric columns.
5. Reviewed missing or invalid values in important fields.
6. Renamed the customer table to `DimCustomer`.
7. Applied the transformations and loaded the cleaned data into the model.

## Data Modeling

- Created a `DimDate` table using DAX.
- Added year, month number, month name, year-month, and quarter attributes.
- Created a relationship between `DimDate[Date]` and `DimCustomer[Join Date]`.
- Used the date table to support customer join-date analysis.

## DAX Measures and Calculations

The project includes measures and calculated columns for:

- Total Customers
- Total Historical Spend
- Total Recorded Orders
- Repeat Customers
- Repeat Customer Rate %
- Retained Customers
- At-Risk Customers
- Churned Customers
- Retention Rate Proxy %
- Average Spend per Customer
- Average Order Value Measure
- Recency Days
- Recency Score
- Frequency Score
- Monetary Score
- RFM Total Score
- RFM Segment
- Calculated Retention Status
- Status Validation

RFM scores classify customers using recency, purchase frequency, and historical spend thresholds. Segments include Champions, Loyal Customers, Potential Loyalists, At Risk - High Value, Hibernating, and Needs Attention.

The retention classification uses the defined recency thresholds and is an analytical proxy, not a verified measure of contractual or cohort retention.

## Dashboard Features

### Page 1 — Customer Overview

- KPI cards for customer and spending indicators
- Customer count by RFM segment
- Historical spend by RFM segment
- Customer distribution by calculated retention status
- City/region slicer
- RFM segment slicer

### Page 2 — Customer Analysis

- Customer trend by join month
- Segment performance matrix
- Purchase channel slicer
- Loyalty tier slicer
- Gender slicer
- Date-range slicer
- Key business insights

### Interactive Analysis

Users can filter the report using the available slicers and date selection to explore customer groups and compare segment performance.

## Key Business Insights

Use the actual dashboard results to identify:

1. Which RFM segment has the largest customer count.
2. Which RFM segment contributes the highest historical spend.
3. How many customers are classified as retained, at risk, or churned.
4. Which customer segments show higher purchase frequency and spending.
5. Which high-value, at-risk customers may benefit from targeted retention campaigns.
6. How customer acquisition varies by join month.

### Business Recommendations

- Create targeted win-back campaigns for at-risk customers.
- Reward loyal and high-value customers through loyalty initiatives.
- Personalize marketing by customer segment and preferred product category.
- Monitor customer recency and purchase behavior to identify changes in engagement.

**Interpretation note:** The join-month trend represents customer acquisition timing, not monthly retention. True cohort retention requires transaction history or periodic customer snapshots.

## Screenshots

### Page 1 — Customer Overview

![Customer Overview Dashboard](screenshots/dashboard_page_1.png)

### Page 2 — Customer Analysis

![Customer Analysis Dashboard](screenshots/dashboard_page_2.png)

## Project Structure

```text
Customer-Segmentation-Retention-Analytics/
├── README.md
├── powerbi/
│   └── Customer_Segmentation_Retention_Analytics.pbix
├── data/
│   ├── Customer_Segmentation_Retention_Dataset.csv
│   └── Data_Dictionary.md
├── screenshots/
│   ├── dashboard_page_1.png
│   └── dashboard_page_2.png
├── documentation/
│   ├── Business_Insights.md
│   └── Methodology.md
└── presentation/
    └── Project_Summary.pdf
```

## How to Use

1. Download or clone this repository.
2. Open the `.pbix` file using Power BI Desktop.
3. If prompted, update the data source path to the downloaded dataset.
4. Refresh the data if required.
5. Explore the dashboard using the available slicers and visuals.

## Conclusion

This project demonstrates practical Power BI skills in data preparation, data modeling, DAX calculations, RFM-based customer segmentation, dashboard design, and business insight communication.

It provides a foundation for customer analytics and retention monitoring. Transaction-level data would be required to extend the project to true monthly revenue analysis and cohort-based retention measurement.

## Author

**K B SWETAA**

Power BI | Data Analytics | Business Intelligence

## Disclaimer

This project uses synthetic data for educational and portfolio demonstration purposes. Customer classifications and business recommendations are illustrative and should be validated before use in real business decisions.
