# Tap-Dom-ML-Predictive-Model
ML predictive model for Tap-Dom as a Business case study for ML Algorithms application. Nashiru Muniru (AI, Systems and Business Analyst) 

Business Challenge
Tap-Dom is a multinational events and fashion consumer goods e-commerce company that sells a wide range of events and fashion products. With a strong presence in the market, the company continually strives to enhance its market share, drive revenue growth, and strengthen its brand equity. The company's e-commerce portal was launched two years ago, and it has been successful in attracting customers from various parts of the world.
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


CREATING THE BENCHMARK MODEL
Example: Mean / Median-Based Models,  Rule-Based Models, etc.

EVALUATION OF THE MODEL 
How to evaluate the predictions?
<img width="1033" height="342" alt="image" src="https://github.com/user-attachments/assets/890dba4d-fc51-400d-969e-e35cf6142b20" />

A. CORRECTNESS: 
done using evaluation metrics ie.
<img width="1092" height="415" alt="image" src="https://github.com/user-attachments/assets/79d15e89-d279-4217-b5f1-9420bc1bc5af" />

i. Mean Absolute Error:
<img width="739" height="212" alt="image" src="https://github.com/user-attachments/assets/4647b7a9-7698-412a-ace9-9044fead2b26" />


B. RELIABILITY: (How reliable is the model on unseen data)
Ways d methods tochek the realibility of predictions
<img width="655" height="427" alt="image" src="https://github.com/user-attachments/assets/6800c57a-d0ea-49ea-afa4-1d6f4a4b6631" />

i. Data dvivition 
a. Train-Validate Split
<img width="445" height="328" alt="image" src="https://github.com/user-attachments/assets/d57ee7b9-a46f-4320-98a8-6fc601e93e7b" />

<img width="891" height="269" alt="image" src="https://github.com/user-attachments/assets/836640b1-f806-47a2-96aa-100b09623a06" />

<img width="1128" height="236" alt="image" src="https://github.com/user-attachments/assets/148224d6-b912-4ea2-bd2b-9123733ff90f" />
Division can be sequestial or randam depending on problem statement.


<img width="1115" height="253" alt="image" src="https://github.com/user-attachments/assets/68d02e47-3d39-4bfb-9c10-ca3edd4bf354" />

<img width="1193" height="551" alt="image" src="https://github.com/user-attachments/assets/be9a4831-4f6f-4e6a-9903-1541f106d966" />

Problem with the prediction 

Factors tha influence UNis Sold
<img width="1195" height="514" alt="image" src="https://github.com/user-attachments/assets/50f33289-44b6-4070-a556-a7bd864eca39" />

Rue Base Systems v/s ML 
<img width="939" height="422" alt="image" src="https://github.com/user-attachments/assets/de3a65c1-4d76-484c-995a-bda4d28051a8" />

To select the bet ML approach, Tap-Dom has has found tht its marketing strategies based on the existing segments are not effective. They want try out new-age bundle marketing strategies which would require the to group similar products together irrespective of te segment.
This clearly fits int an Unsupervised ML problem.
Problem statment added 
<img width="681" height="149" alt="image" src="https://github.com/user-attachments/assets/3bacfb61-8c41-4da2-bcde-6f98786bab61" />

The ML Workflow 
<img width="906" height="421" alt="image" src="https://github.com/user-attachments/assets/19064a73-8b21-4798-9953-1440580107af" />


