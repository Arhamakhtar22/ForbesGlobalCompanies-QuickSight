# ForbesGlobalCompanies-QuickSight
This dashboard i created provides an interactive and insightful representation of top 2000 company performance across different industries. It uses a combination of KPIs, charts, and controls to visualize critical metrics like market value, sales, profit margin, and profitability ratios, offering a detailed breakdown and flexibility for exploration.  <br />
Dataset: https://www.kaggle.com/datasets/mohammadgharaei77/largest-2000-global-companies

<img width="826" alt="Screenshot 2024-12-07 at 7 52 10 PM" src="https://github.com/user-attachments/assets/1ce47576-0bd2-4cb1-8b1c-eaa4e75e63ef">

1) KPI Cards
<img width="945" alt="Screenshot 2024-12-07 at 7 52 39 PM" src="https://github.com/user-attachments/assets/b567b587-fb0c-4430-af1d-663a7c39d985">

Metrics: <br />
Market Value: Displays the total market value of companies within the selected industry. <br />
Total Sales: Shows the aggregated sales of companies within the selected industry. <br />
Profit Margin: Reflects the average profit margin across all companies in the selected industry. <br />

Industry Filter: A filter on the Industry field dynamically updates the KPI values when a user selects an industry. <br />
The Profit Margin KPI Card is used by making a calcualted field using Profit / Sales * 100

Why I Used It: <br />
The KPIs provide a summary of the financial health and performance of companies in the selected industry. <br />
Filtering by industry ensures that users can focus on specific segments <br />

2) Horizontal Stacked Bar Chart
<img width="1153" alt="Screenshot 2024-12-07 at 7 57 08 PM" src="https://github.com/user-attachments/assets/f7298d18-e8f1-4513-b31f-cc915e500946">

Metric: <br />

Market Value: Displays the market value for each company within the selected industry. <br />

The chart is controlled by the same Industry filter, ensuring that only companies from the selected industry are displayed. <br />

Minimum Profit Margin Control: Users can filter the bar chart results by setting a minimum profit margin threshold using the parameter MinProfitMargin. <br />

<img width="599" alt="Screenshot 2024-12-07 at 7 58 45 PM" src="https://github.com/user-attachments/assets/ebf6c487-7a36-48a2-8b7b-89e212b55948">

<img width="238" alt="Screenshot 2024-12-07 at 7 59 26 PM" src="https://github.com/user-attachments/assets/b57afab9-630b-45f4-97f7-fb26e9386d06">

Drill-Through to Table: <br />

The bar chart is connected to a detailed table through Actions. <br />
Clicking on a company in the bar chart reveals additional details in the table, including: <br />
Profit Margin <br />
ROA(Return on Assets): Profit / Assets * 100 <br />
Market Value <br />

Why I Used It?
The bar chart allows users to compare market values of companies in the selected industry visually. <br />
The drill-through table provides additional context, offering a deeper understanding of company-specific metrics. <br />

How to make it:


<img width="238" alt="Screenshot 2024-12-07 at 8 03 20 PM" src="https://github.com/user-attachments/assets/a64ed6e6-d0e8-46b4-a6db-c1e10d9ea784">

<img width="238" alt="Screenshot 2024-12-07 at 8 03 35 PM" src="https://github.com/user-attachments/assets/a4e527c7-b61e-40e0-a957-ad265ca30522">

3) Scatter Plot

<img width="578" alt="Screenshot 2024-12-07 at 8 05 09 PM" src="https://github.com/user-attachments/assets/02a373e0-dfc6-40d9-8bb2-de65d2b62f48">

Metrics:

<img width="241" alt="Screenshot 2024-12-07 at 8 09 12 PM" src="https://github.com/user-attachments/assets/aaaa097c-fcc4-409c-a8a2-bd2eff9a5890">

The DynamicBubbleSize is a calcualted field made using:

ifelse(
  ${BubbleSizeParam} = 'Market Value', {Market Value},
  {Profit Margin}
)


Bubble Size Control: <br />
Parameter: BubbleSizeParam <br />
Dropdown Control: Users can choose to size bubbles based on either Market Value or Profit Margin.


<img width="600" alt="Screenshot 2024-12-07 at 8 06 15 PM" src="https://github.com/user-attachments/assets/79f802b8-7d13-4288-bc9f-7516995a8302">


<img width="241" alt="Screenshot 2024-12-07 at 8 14 06 PM" src="https://github.com/user-attachments/assets/fe29d64e-5d65-40a1-9d7d-5385c3893c9e">

4) Pie Chart

<img width="604" alt="Screenshot 2024-12-07 at 8 16 37 PM" src="https://github.com/user-attachments/assets/c2286454-625f-4cfe-8889-4449c220a5b8">

Metric: <br />

Market Value Breakdown: Displays the market value contribution of each industry as a percentage of the total. <br />

Industry Selection: <br />
Controlled by the parameter IndustryParam. <br />
A dropdown allows users to filter the pie chart to display only data for the selected industry. <br />


<img width="604" alt="Screenshot 2024-12-07 at 8 17 45 PM" src="https://github.com/user-attachments/assets/869bd8f3-1b88-4de2-af86-e8905236d22c">

<img width="240" alt="Screenshot 2024-12-07 at 8 18 30 PM" src="https://github.com/user-attachments/assets/be82b1f1-4c82-42fd-9aaa-50b7607d5265">


5. Filters and Parameters <br />
   
Filters <br />
Industry Filter: <br />
Affects the KPI cards, bar chart, scatter plot, and pie chart. <br />
Enables users to focus on specific industries for a tailored view. <br />
Parameters <br />
MinProfitMargin: v

Purpose: Filters companies in the bar chart and table to show only those with a profit margin above the specified threshold. <br />
Control Type: Slider <br />
Default Value: 10% <br />

BubbleSizeParam: <br />

Purpose: Allows users to dynamically adjust the bubble size in the scatter plot based on: <br />
Market Value <br />
Profit Margin <br />
Control Type: Dropdown <br />
Default Value: Market Value <br />
Stakeholder Value: <br />
Adds flexibility and customization to the scatter plot, enabling stakeholders to explore different dimensions of performance. <br />

IndustryParam: <br />

Purpose: Filters the pie chart to display data for the selected industry. <br />
Control Type: Dropdown <br />
Default Value: None <br />
Stakeholder Value: <br />
Provides an industry-specific view of market value contribution, assisting in sector-level analysis. <br />


