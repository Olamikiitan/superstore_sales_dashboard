Superstore Executive Sales Dashboard

A Power BI dashboard that helps management monitor sales performance, profitability, customer behaviour and regional performance for a national retail company.

Built for the AnalystLab Africa Data Analytics Internship, Week 2: Business Analytics Case Study.

## The business problem

Senior management needs one interactive view of how the business is doing. In this project I took the role of a Junior Business Intelligence Analyst. My job was to prepare the raw sales data, build a dashboard in Power BI, and recommend actions based on what the data showed.

 Dataset
I used the Superstore Sales Dataset ([Kaggle](https://www.kaggle.com/datasets/vivek468/superstore-dataset-final)).

- Period: 2014 to 2017
- Size after cleaning: 9,993 order lines, covering 5,009 orders
- Regions: Central, East, South, West
- Customer segments: Consumer, Corporate, Home Office
- Product categories: Furniture, Office Supplies, Technology

 Tools Used

- Microsoft Power BI Desktop
- Power Query (data cleaning and transformation)
- DAX (measures and calculated columns)

How I prepared the data

1. Imported the CSV and reviewed its structure, using Power Query's column quality and profile views on the whole dataset.
2. Checked for missing values and found none.
3. Found and removed 1 duplicate record. Two rows for order US-2014-150119 were identical in every column except `Row ID`, so I left `Row ID` out of the duplicate check. The row count went from 9,994 to 9,993.
4. Converted `Order Date` and `Ship Date` from text to dates, using the US date format, and changed `Postal Code` to text.
5. Created two helper columns, `Order Year` and `Month Year`, for the slicers and the trend chart.

KPIs and measures

| KPI | How I calculated it |
|---|---|
| Total Sales | Sum of `Sales` |
| Total Profit | Sum of `Profit` |
| Total Orders | Distinct count of `Order ID` (one order can have several rows) |
| Average Sales | Total Sales divided by Total Orders, so it is the average per order |
| Profit Margin | Total Profit divided by Total Sales |

Headline results: $2.30M in sales, $286.4K in profit, 5,009 orders, $458.56 average sales per order, and a 12.5% profit margin.

 The dashboard

The dashboard has three pages, with a consistent dark theme and five dropdown slicers (Region, Order Year, Order Id, Segment and Category) that filter the pages.

1. Overview:KPI cards, a sales and profit trend by month, sales by category, sales by customer segment, and a map of sales by state.
2. Sales and Profits:profit by sub-category, top products by profit, sales and profit by region, and a category matrix with profit margin. Loss-making items are shown in red.
3. Insights and Recommendations: the key findings, risks, opportunities and actions.

![Overview page](screenshots/overview.png)
![Sales and Profits page](screenshots/sales-and-profits.png)

Key insights

1. Sales are growing, but margin is not keeping pace. Sales rose from $484K in 2014 to $733K in 2017. Profit margin peaked at 13.4% in 2016 and slipped to 12.7% in 2017.
2. The West and East regions lead. West earns the most ($725K sales, $108.4K profit). Central has a much weaker margin (7.9%) than the others.
3. Technology and Office Supplies carry the profit. Furniture sells $742K but earns only $18.5K in profit, a 2.5% margin.
4. Sales are seasonal. September to December brings in about 52% of annual sales, and January and February are the weakest months.
5. Home Office is the smallest segment but the most profitable per dollar, with a 14.0% margin. Consumer is the largest segment at 50.6% of sales.

Risks

- Heavy discounts are linked to losses. Order lines discounted by more than 20% lose money overall, while undiscounted lines earn a margin of about 30%. This shows a relationship, not proof that discounts alone cause the losses.
- Tables and Bookcases lose money, and so do several states, including Texas, Ohio, Pennsylvania and Illinois.
- About one in five order lines is unprofitable.

Opportunities

- High-margin products such as Copiers, Paper, Labels and Envelopes.
- High-margin states such as New York, Washington and Michigan.
- Growing the Home Office segment and lifting sales in the quieter months.

 Recommendations

1. Cap discounts at about 20% and require approval above that.
2. Review pricing and supplier costs for Tables and Bookcases.
3. Investigate the Central region and the loss-making states.
4. Reprice or drop products that consistently lose money.
5. Plan stock and marketing around the September to December peak, and run promotions in January and February.
6. Push high-margin Technology and supply products.
7. Grow in the West, New York and Washington, and market to Home Office customers.

 Repository contents

| File | Description |
|---|---|
| `WEEK_2_ANALYSTLAB.pbix` | The Power BI dashboard |
| `Business Intelligence Overview Report` | What BI is, why dashboards matter, and the objective of this dataset |
![Overview page](PAGE%201.png)
![Sales and Profits page](PAGE%202.png)
![Insights page](PAGE%203.png)| Summary of insights, risks, opportunities and recommendations |

## How to open the dashboard

Download the `.pbix` file and open it in Power BI Desktop (free for Windows). Use the slicers to filter by region, year, segment and category, and use the page buttons at the top to move between pages.
 Author

Mariam Olaitan Azeez, Data Analytics Intern at AnalystLab Africa

AnalystLabAfrica
