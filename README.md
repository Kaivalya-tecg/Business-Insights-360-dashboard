# Business Insights 360 Dashboard

### Dashboard Link : https://app.powerbi.com/view?r=eyJrIjoiZmQyYTJiNmMtNGUyNS00ODViLWJiNDMtMDExNzJiZjY1Zjk4IiwidCI6ImE4ZWVjMjgxLWFhYTMtNGRhZS1hYzliLTlhMzk4YjkyMTVlNyIsImMiOjN9&disablecdnExpiration=1717430801

## Problem Statement

AtliQ Hardware is a hardware company which sells hardware products to retail stores. Examples of retail stores are Croma (India), Best Buy (USA), etc. The company is in many countries in the world and these countries are known to be markets in this project. The markets come under 4 regions like APAC (Asia-Pacific), EU (Europe), LATAM (Latin America) and NA (North America). customers are the different stores to which AtliQ sells hardware products (example: Best Buy, Micro Center, Croma, etc). The company sells 6 segments of products namely, 1) Accessories 2) Desktop 3) Networking 4) Notebook 5) Peripherals and 6) Storage. These segments have various categories and various products come under these categories. Examples of categories are Laptops, Tablets, Mobile phones, etc.
The objective of this project is to give insights in the form of a comprehensive Power BI dashboard into the company's operations and identify any opportunities of growth and areas of improvement. This dashboard acts like a single platform where various departmental information of AtliQ is found to take strategic data-driven decisions. The departments that can be found on the dashboard are: 1) Finance 2) Sales 3) Marketing 4) Supply Chain. There also is an Executive dashboard, which acts like a single platform to show all the crucial metrics of the company to the C-suite, VPs and Directors of the company.
Any data analytics project are carried out in three steps: 1. Data Collection 2. Data Modelling 3. Data Visualization


### Steps followed 
A high-level overview of the steps in the project are:
- Data Loading : Load data into Power BI Desktop, dataset is a csv file. The data is present in the form of dimension and fact tables in multiple csv files. All these files have been loaded into Power BI
- Data Transformation : Open power query and make necessary transformations to the data, like handling duplicates, anomalies and any other minor changes. Combining few tables into a fact table has also been done in this step. After the transformation, closing and loading the data has been done.
- Data Modelling : Relationships between the dimension and fact tables have been established in order to make further analysis meaningful. Without proper data modelling, there is a high risk of incorrect analysis which leads to incorrect visualizations.
- Data Visualization : In this step, the data has been visualized which gives deep insights into the operations of the company. The overall dashboard tells a meaningful story about the business and drives the strategic decision-making of the executives.

To begin with, a Home page has been created with different views, which act as buttons to be redirected to that particular view. In order to achieve this, 'Action' button was set on the particular image and 'Page Navigation' was set to the respective department's view.
        
Snap of the Home page ,

![home page](https://github.com/Kaivalya-tecg/BI-360/assets/90671545/25ad90fb-8ead-4ac3-bab1-b827b65733ac)

Finance View:
- This view contains the dashboard which is meant for the finance department of AtliQ Hardware. The dashboard monitors crucial metrics like Net Sales, Gross Margin%, Net Profit% (which are in the form of scorecards on the dashboard).
- There is a 'Matrix' visualization which gives us information about all the financial metrics which determine how well the business is doing with respect to its revenue.
- These metrics have been created as measures and these measures have been created using DAX (Data Analysis Expressions).
- For example: The DAX formula used for calculating Gross Margin% is: Gross Margin%= [Gross Margin $]/ [Net Sales $]
Net Profit%= DIVIDE([Net Profit $],[Net Sales $],0)
- In the finance view, the filters that can be seen are region, market, customer, segment and category. This means that the information on the dashboard change according to the selected filter.
- We can also find 'Tile' filter, which has years (2018,2029,2020,2021,2022 est), quarters (Q1,Q2,Q3,Q4),ytd_ytg(Year-To-Date, Year-To-Go), and Benchmarks (vs Target, vs Last Year)
- The 'Area chart' shows us the Net sales performance over time. On the x-axis we have different months based on the year selected, and on the y-axis we have Net sales vs the benchmark.
- The rest of the 'Matrix' visuals show us i) the P & L values in different regions of the business. This can also be expanded to see how the P & L Values of different markets are. ii) the segment of products and their corresponding P & L Values. This can further be expanded to see the different categories of products and their P & L Values.

Snap of the Finance dashboard is as follows:
![finance](https://github.com/Kaivalya-tecg/BI-360/assets/90671545/7d8c7b1a-a738-47e5-aec0-5b24e2f0f6dc)


Sales View:
- This view contains the dashboard which is meant for the sales department of AtliQ Hardware. The dashboard monitors crucial metrics like customer performance and products performance (which are in the form of matrix visuals on the dashboard).
- In the sales view, the filters that can be seen are region, market, customer, segment and category. This means that the information on the dashboard change according to the selected filter.
- We can also find 'Tile' filter, which has years (2018,2029,2020,2021,2022 est), quarters (Q1,Q2,Q3,Q4),and ytd_ytg(Year-To-Date, Year-To-Go).
- The 'scatterplot' on the dashboard indicates the Net sales and Gross margin of different markets. More the net sales, larger is the bubble on the scatterplot. Clearly, India has the highest sales compared to all the other markets.
- There are two 'donut charts' one of which shows the proportion of Net sales, Pre-invoice deductions and Post-invoice deductions for the selected year. The other donut chart shows the proportion of Total COGS(Cost of goods sold) and the gross margin.

Snap of the Sales dashboard is as follows:
![sales](https://github.com/Kaivalya-tecg/BI-360/assets/90671545/53df7673-9936-4256-82ae-2cabea9df8e4)


Marketing View:
- This view contains the dashboard which is meant for the marketing department of AtliQ Hardware. The dashboard monitors crucial metrics like products performance and region/market performance (which are in the form of matrix visuals on the dashboard).
- In the marketing view, the filters that can be seen are region, market, customer, segment and category. This means that the information on the dashboard change according to the selected filter.
- We can also find 'Tile' filter, which has years (2018,2029,2020,2021,2022 est), quarters (Q1,Q2,Q3,Q4), and ytd_ytg(Year-To-Date, Year-To-Go).
-We can find a 'scatterplot' which shows the net sales and gross margin generated by different products across various regions.
- There is a 'donut chart' which shows the proportion of Tota COGS and Gross Margin.
- Beside that we can find a 'waterfall chart' which shows the increase/decrease of net profit, operational expense and gross margin.

Snap of the Marketing dashboard is as follows:
![marketing](https://github.com/Kaivalya-tecg/BI-360/assets/90671545/2a68fdba-2079-482c-ae17-dd362e316e66)

Supply Chain View:
- This view contains the dashboard which is meant for the supply chain department of AtliQ Hardware. The dashboard monitors crucial metrics like forecast accuracy, net error and absolute error(which are in the form of scorecards on the dashboard).
- In the supply chain view, the filters that can be seen are region, market, customer, segment and category. This means that the information on the dashboard change according to the selected filter.
- We can also find 'Tile' filter, which has years (2018,2029,2020,2021,2022 est), quarters (Q1,Q2,Q3,Q4), and ytd_ytg(Year-To-Date, Year-To-Go).
- The 'matrix' visual contains various customers and their corresponding forecast accuracy, last year's forecast accuracy, net error, net error%  and risk.
- There is a 'line and column clustered chart' which shows net error, forecast accuracy% and last year's forecast accuracy% over a time period.
- In another 'matrix' visual, these metrics are monitored for various products.

Snap of the Supply chain dashboard is as follows:
![supply chain](https://github.com/Kaivalya-tecg/BI-360/assets/90671545/3ce1a5ed-ec61-423a-b8a4-e9afa344a5e6)


Executive View:
- This view contains the dashboard which is meant for the executives (C-Suite, VPs  and directors) of AtliQ Hardware. The dashboard monitors crucial metrics like net sales, gross margin%, net profit% and forecast accuracy(which are in the form of scorecards on the dashboard).
- This view acts like a consolidated platform which contains crucial KPIs from all the departments of AtliQ Hardware.
- In the executive view, the filters that can be seen are region, market, customer, segment and category. This means that the information on the dashboard change according to the selected filter.
- We can also find 'Tile' filter, which has years (2018,2029,2020,2021,2022 est), quarters (Q1,Q2,Q3,Q4),ytd_ytg(Year-To-Date, Year-To-Go), and Benchmarks (vs Target, vs Last Year).
-One of visuals is a 'matrix' which shows crucial metrics the different subzones of AtliQ. These metrics include net sales, gross margin%, market share%, net profit%, net error% and risk.
- The 'ribbon chart' on the dashboard shows the market share of AtliQ Hardware compared to its competitors over different years. It is clear that the market share of AtliQ has increased over the years with 5.9% in 2022.
-There are two 'donut charts' which shows revenue i) by division ii) by channel
- There is a 'line chart' which shows the yearly trend of KPIs like revenue, gross margin%, net profit% and market share%.
-There are two tables which show top 5 customer and top 5 products by revenue.

Snap of the Executive view is as follows:
![executive](https://github.com/Kaivalya-tecg/BI-360/assets/90671545/be555fdc-1431-4835-ac61-797c89531031)

