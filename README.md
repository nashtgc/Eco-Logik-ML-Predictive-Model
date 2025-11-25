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
By using the average and the median: Very imporatn to take out outlier  products with 0 sales throughout.

After getting the threshold, we restructure our problem statement:
1. Identify the factors to predict units sold for the products.
2. Identify which products will sell more than 1000 units.

Understanding the Dataset

<img width="370" height="447" alt="image" src="https://github.com/user-attachments/assets/0fc4d6ec-9f1b-4e88-b526-4d267ef28529" />

