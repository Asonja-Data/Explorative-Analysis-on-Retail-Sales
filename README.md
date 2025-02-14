# Explorative-Analysis-on-Retail-Sales
## Project Overview
This project analyzes customer demographics, purchasing behavior, and sales trends using a retail sales dataset. Techniques employed include data exploration, time series analysis, customer and product analysis, and data visualization to derive actionable insights for business decision-making.
## Project Scope
This project aims to leverage retail sales data to drive business improvements through:
-	Comprehensive data cleaning and preprocessing.
-	In-depth exploratory data analysis.
-	Time series analysis to understand and forecast sales trends.
-	Product category analysis to optimize product offerings.
-	Visualizations to communicate key findings.
-	Development of actionable recommendations for marketing, sales, and product strategies.
## Dataset Source: 
- <a href=”https://github.com/Asonja-Data/Explorative-Analysis-on-Retail-Sales/blob/main/retail_sales_dataset.csv”/a>

## Dataset Description
-	File Name: Retail Sales Analysis.ipynb
-	Size: 1000 rows × 9 columns
-	Column Description:
  
| Column Name | Description |
|-------------|-------------|
| Transaction ID |	Unique identifier for each transaction |
| Date | Date of purchase |
| Customer ID |	Unique identifier for each customer |
| Gender | Gender of the customer |
| Age	| Age of the customer |
| Product Category |	Category of the purchased product |
| Quantity |	Number of units purchased |
| Price per Unit	| Price per unit of the product |
| Total Amount	| Total transaction value |

## Methodology
1. Data Loading:
Necessary libraries were imported, and the dataset was loaded using pandas.
Libraries Used:
  - pandas
  - seaborn
  - matplotlib.pyplot
  - statsmodels
The dataset was load into the notebook using pandas function. The first five rows were viewed to ensure the dataset is successfully loaded and ready for exploration.

2. Data Cleaning:
Identify columns with missing values, duplicates, as well as, find unique values in categorical columns

Result: 
No missing values or duplicates were found. The unique value counts provide insights into the data's characteristics.
-	Customer ID: 1000 unique values
-	Gender: 2 unique values
-	Product Category: 3 unique values
-	Transaction ID: 1000 unique values
-	Age: 47 unique values
-	Quantity: 4 unique values
-	Price per Unit: 5 unique values
-	Total Amount: 18 unique values

3. Descriptive Analysis
   
Descriptive statistics were generated using df.describe() to understand the distribution and central tendency of numerical variables.

4. Time Series Analysis
- Step 1: The date column was parsed to ensure that Pandas recognizes it as dates, as well as setting it as the index making time-based data selection and manipulation much more convenient.
- Step 2: Change the time granularity to monthly and weekly granularity

  Monthly Granularity
   -	Light Blue Line (Monthly Sales): Represents the actual quantity of sales for each month. Shows fluctuations indicating varying demand patterns.
   -	Green Line (3-Month Rolling Average): Represents the smoothed trend by averaging sales over a 3-month window. Smooths out fluctuations, revealing underlying trends.
   -	Observations: General upward trend in sales (Mar-Jun 2023), decline (Jul-Oct 2023), recovery (Nov-Dec), and sharp drop (Jan 2024), which could indicate seasonal 
      effects or a drop in demand after the holiday season.

  Weekly Granularity
   -	High Volatility in Weekly Sales: The light blue line indicates substantial week-to-week variability in sales. This is typical for many businesses and could be due to 
      factors like promotions, day-of-week effects, seasonality within the week, or random customer behavior.
   -	Smoothing Effect of Rolling Average: The orange line demonstrates how the 7-day rolling average smooths out the weekly fluctuations, revealing the overall trend.
   -	Trend Identification: The rolling average helps identify underlying trends. Upward trend (mid-2023), peak (late 2023), slight decline.

5. Customer and Product Analysis &Visualization

Step 1: Customer Demographics Analysis
-	Customer Age Analysis
  ![image](https://github.com/user-attachments/assets/82d636bb-9406-4537-95aa-56702c2b459d)

 	Interpretation:
    1.	Age Range: Broad range, likely 15-20 to 65-70.
    2.	Frequency: Peak around age 40.
    3.	Shape: Uneven, multiple peaks, not a normal distribution.
    4.	KDE: Smoothed representation, highlights modes.


-	Customer Gender Distribution
 ![image](https://github.com/user-attachments/assets/9b001b1b-a19a-4910-880c-021011fd6afd)

 	   Interpretation: Near-equal split between female (51%) and male (49%) customers.

Step 2: Purchasing Behavior Analysis
 ![image](https://github.com/user-attachments/assets/73b20a76-f7f3-4ca6-bb7e-1e81dc4084f8)
   
     Interpretation: 
    -	High-Value Customers: The chart immediately highlights the top 10 customers who contribute the most to revenue. Identifying these customers is crucial for targeted 
      marketing and loyalty programs.
    -	Spending Concentration: The consistent height of the bars indicates that these top 10 customers spend roughly the same amount. There's not a significant drop-off in 
      spending from the "highest" to the "10th highest." This suggests a relatively homogeneous group in terms of high spending.
    -	Relative Contribution: While the chart shows the absolute spending of each customer, it's important to consider their spending relative to the overall customer base. 
      These 10 customers likely represent a significant portion of total revenue, highlighting the importance of retaining them.

Step 3: Product Sales Analysis
 ![image](https://github.com/user-attachments/assets/6013ab33-721a-45aa-af94-e975641e1641)
    
     Interpretation: Product sales analysis identifies Clothing as the leading category, followed by Electronics and Beauty. The strong performance of Clothing suggests 
     either high customer demand or effective marketing campaigns. While Electronics and Beauty also perform well, they represent potential growth areas. 
 
 ![image](https://github.com/user-attachments/assets/0708f0b5-60cd-46d4-88f3-a45bb30f9047)
    
    Interpretation: Analysis of revenue by price point identifies $500 and $300 as the leading revenue generators, significantly outpacing lower price points ($50, $30, 
    and $25). The substantial revenue contribution from higher-priced products suggests a focus on premium offerings or effective pricing strategies for high-value 
    customers. While lower-priced items contribute less to total revenue, there may be opportunities to increase profitability in these segments through pricing 
    adjustments, targeted promotions, or cost optimization.
 
 ![image](https://github.com/user-attachments/assets/da77830b-1985-443f-a189-9356728bdef1)
   
    Interpretation: An analysis of revenue by product category identifies Electronics and Clothing as the leading revenue generators, followed by Beauty. While a previous 
    analysis highlighted Clothing's dominance in unit sales, Electronics surpasses it in revenue, indicating a focus on higher price points or potentially higher profit 
    margins. Beauty also demonstrates strong revenue performance, despite selling fewer units compared to Clothing and Electronics. This suggests opportunities to 
    investigate pricing and promotional strategies to maximize revenue across all categories.
 
 ![image](https://github.com/user-attachments/assets/7e592768-cb13-4435-b157-6e2a1eeb8835)
  
   Interpretation: The scatter plot analysis of price per unit and quantity sold reveals a nuanced relationship, with no clear linear correlation. While some high-priced 
   products achieve high sales volumes, others perform poorly, indicating that price alone does not guarantee sales success. Similarly, lower-priced products exhibit a wide 
   range of sales performance. This suggests that factors beyond price, including product demand, brand equity, and marketing effectiveness, are critical drivers of sales. 



## Recommendations
-	Target high-spending customers: Develop a loyalty program or personalized marketing campaigns for the top 10% of spending customers (or however you define "high- 
  spending"). Offer exclusive discounts, early access to new products, or personalized recommendations. Measure success by an increase in repeat purchases and average order 
  value from this segment. 
-	Optimize pricing for lower-priced items: Conduct A/B testing on pricing for items below $100 (or whatever threshold you determine) to identify price points that maximize 
  revenue without significantly impacting volume. Measure success by an increase in overall revenue from these lower-priced items. 
-	Investigate the drivers of Clothing's success: Conduct customer surveys or focus groups to understand why Clothing is the top-selling category. Use these insights to 
  develop marketing strategies or product improvements for other categories. Measure success by an increase in sales conversion rates and customer satisfaction scores 
  related to the Clothing category. 
-	Explore growth potential in Beauty: Given its strong revenue despite lower unit sales, investigate opportunities to expand the Beauty category. This could include adding 
  new product lines, increasing marketing spend, or partnering with influencers. Measure success by an increase in market share and overall revenue from the Beauty category.
