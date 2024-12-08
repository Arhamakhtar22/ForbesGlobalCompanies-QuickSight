# ForbesGlobalCompanies-QuickSight
This dashboard i created provides an interactive and insightful representation of top 2000 company performance across different industries. It uses a combination of KPIs, charts, and controls to visualize critical metrics like market value, sales, profit margin, and profitability ratios, offering a detailed breakdown and flexibility for exploration.
Dataset: https://www.kaggle.com/datasets/mohammadgharaei77/largest-2000-global-companies

<img width="826" alt="Screenshot 2024-12-07 at 7 52 10 PM" src="https://github.com/user-attachments/assets/1ce47576-0bd2-4cb1-8b1c-eaa4e75e63ef">

1) KPI Cards
<img width="945" alt="Screenshot 2024-12-07 at 7 52 39 PM" src="https://github.com/user-attachments/assets/b567b587-fb0c-4430-af1d-663a7c39d985">

Metrics:
Market Value: Displays the total market value of companies within the selected industry.
Total Sales: Shows the aggregated sales of companies within the selected industry.
Profit Margin: Reflects the average profit margin across all companies in the selected industry.

Industry Filter: A filter on the Industry field dynamically updates the KPI values when a user selects an industry.
The Profit Margin KPI Card is used by making a calcualted field using Profit / Sales * 100

Why I Used It:
The KPIs provide a summary of the financial health and performance of companies in the selected industry.
Filtering by industry ensures that users can focus on specific segments

2) Horizontal Stacked Bar Chart
<img width="1153" alt="Screenshot 2024-12-07 at 7 57 08 PM" src="https://github.com/user-attachments/assets/f7298d18-e8f1-4513-b31f-cc915e500946">

Metric:

Market Value: Displays the market value for each company within the selected industry.

The chart is controlled by the same Industry filter, ensuring that only companies from the selected industry are displayed.

Minimum Profit Margin Control: Users can filter the bar chart results by setting a minimum profit margin threshold using the parameter MinProfitMargin.

<img width="599" alt="Screenshot 2024-12-07 at 7 58 45 PM" src="https://github.com/user-attachments/assets/ebf6c487-7a36-48a2-8b7b-89e212b55948">

<img width="238" alt="Screenshot 2024-12-07 at 7 59 26 PM" src="https://github.com/user-attachments/assets/b57afab9-630b-45f4-97f7-fb26e9386d06">

Drill-Through to Table:

The bar chart is connected to a detailed table through Actions.
Clicking on a company in the bar chart reveals additional details in the table, including:
Profit Margin
ROA(Return on Assets): Profit / Assets * 100
Market Value

Why I Used It?
The bar chart allows users to compare market values of companies in the selected industry visually.
The drill-through table provides additional context, offering a deeper understanding of company-specific metrics.
