# Eco-Logik-ML-Predictive-Model
ML predictive model for Eco-Logik as a Business case study for ML Algorithms application. Nashiru Muniru (AI, Systems and Business Analyst) 

Business Challenge
Eco-Logik Ventures is a multinational consumer goods e-commerce company that sells a wide range of consumer products. With a strong presence in the market, the company continually strives to enhance its market share, drive revenue growth, and strengthen its brand equity. The company's e-commerce portal was launched two years ago, and it has been successful in attracting customers from various parts of the world.
However, in the recent past, the sales have not been increasing as predicted, and the management is concerned about the future of the business. They have tried various strategies such as discounts, promotions, and ads, but these have not yielded the desired results. The management believes that there may be underlying issues that need to be addressed to improve sales performance. 

In this work, I explore different ways to improve the company's sales. 

Took a look at the chart for the  average unit price every month to verify the claim. And the hypothesis was confirmed to be correct.
For a business to increase prices to increase sales is not good in the long run.

In this case, I first analyse to understand the business problem statement to determine whether it's best solved by ML or there are other simpler ways to solve it without using ML.

1. I investigated sales reports and realised that revenue was increasing.
Since Sales = Price * Units Sold
I investigated each element: Price and Unit Sold
Looking at the Unit Sold chart, it was clear that Unit Sold did not contribute the increase in revenue.
Then it must be the price. (hypothesis)

Since the problem was the price, it confirms it's a data science problem. Therefore, 
the problem statement:
1. Identify the factors to predict units sold for the products.
2. Identify which products will cross a certain threshold in terms of units sold.

How to identify the right threshold?
By using the average and the median: Very important to take out outlier  products with 0 sales throughout.

After getting the threshold, we restructure our problem statement:
1. Identify the factors to predict units sold for the products.
2. Identify which products will sell more than 1000 units.

Understanding the Dataset

1. Eco-logik has collected data in 6 different tables.
Let’s take a look at what each of these tables contain. 
<img width="370" height="447" alt="image" src="https://github.com/user-attachments/assets/0fc4d6ec-9f1b-4e88-b526-4d267ef28529" />

2. Data Dictionary - POS_Data
This table contains the sales for each product aggregated on a weekly basis.
<img width="798" height="542" alt="image" src="https://github.com/user-attachments/assets/b2b28cb1-cd6e-4af5-b867-b53ca62e279c" />

3. Data Dictionary - Online_Data
This table includes the weekly campaign details for each product. The date is again the weekly date.
<img width="702" height="291" alt="image" src="https://github.com/user-attachments/assets/e879ce5c-4618-4979-a4c1-bc45e861b9c2" />

4. Data Dictionary - Offline_Data
This table includes the weekly offline campaign. The date is again the weekly date.
<img width="661" height="452" alt="image" src="https://github.com/user-attachments/assets/004b790d-e304-416c-be44-347eaa6992de" />

5. Data Dictionary - Product_Attribute_Data
This table contains the daily data for the ratings of each product, product description length, availability of the product, etc. This is the only
table with daily data.
<img width="823" height="553" alt="image" src="https://github.com/user-attachments/assets/b3f5d3ff-dd68-444b-96e5-6bb2d30d0fe2" />

6. Data Dictionary - VPC_Data
This table contains the number of promotions for each product, the total number of products sold through these promotions or coupons, and the amount spent on promotions, aggregated on a weekly level.
<img width="778" height="244" alt="image" src="https://github.com/user-attachments/assets/77e72a25-6b05-4f7b-ab00-1202319b8147" />

7. Data Dictionary - Search_Rank_Data
This table contains the search rank for the product in a week andthe  median organic search rank for that product. This
table is at a weekly level.
