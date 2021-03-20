# Product-Recommendations-for-Brazilian-E-commerce-Platform

## Background 
### Introduction of Olist
Olist is the largest department store in Brazilian marketplaces. It connects small businesses from all over Brazil to channels without hassle and with a single contract. Those merchants are able to sell their products through the Olist Store and ship them directly to the customers using Olist logistics partners. See more on olist's website: www.olist.com
#### Example of a product listing on a marketplace
![Capture](https://user-images.githubusercontent.com/76879882/111886246-b3d54700-899a-11eb-9644-0866e04044b0.JPG)

### Introduction of the dataset 
The dataset has information of 100k orders from 2016 to 2018 made at multiple marketplaces in Brazil. Its features allows viewing an order from multiple dimensions: from order status, price, payment and freight performance to customer location, product attributes and finally reviews written by customers. Below is the structure of this dataset
![Capture](https://user-images.githubusercontent.com/76879882/111886322-f72fb580-899a-11eb-8a37-182d4a203995.JPG)

## Problem Definititon 
A further investigations of the data shows that Olist is challenged with two problems. 
First, customers are not loyal. On average, customers shop for 1.034 times in this two-year time period, and less then 75% would acutally come back to make a second purchase. 
This is true even for states that have the greatest purchasing power, such as São Paulo, Rio de Janeiro and Minas Gerais. Hence, we believe Olist needs to figure out a way to encourage repeat purchases. 

Also, sales are declining in summer 2018. Over the past two years, sales were blooming in 2017 with some fluctuations, especially a downward sales trend was observed at the end of 2017. However, sales bounced back at the beginning of 2018 but then there's another decline that lasted the entire summer. Assume that this is not affected by seasonality since Olist is an E-commerce, if that downward sales trend presisted, it would affect Olists' performance. Hence, it is needed for Olist to figure out a way to increase sales. 

## Methodologies 
Since Olist needs to increase customer retention as well as generating more sales, and given that Olist is an E-commerce, these two goals can be achieved by deploying products recommendation system to increase user engagement. Amazon.com is the biggest E-commerce platform in America, hence it is a suitable comparable of Olist, the biggest department E-commmerce in Brazile. Studies from McKinsey & Company shows that, 35% of Amazon.com’s revenue is generated by its recommendation engine with its item-to-item collarborative filtering recommendations. (https://www.mckinsey.com/industries/retail/our-insights/how-retailers-can-keep-up-with-consumers#)
Hence, we recommend Olist to follow the same strategy as well. 
#### Demonstration of Amazon's recommendation system 
![Capture](https://user-images.githubusercontent.com/76879882/111887880-fe0ff580-89a5-11eb-8ea7-ac7796875076.JPG)

## Simplified Approaches using Association Rules
Olist can utilize its database and find out products that are co-purchased together. For example, if customers purchase product A also tend to purchase product B, then Olist can 
make product suggestion when customers browse on product A. In this example, I focus primarily on three states ( São Paulo, Rio de Janeiro and Minas Gerais) that contribute the most to Olist's total sales, and provide recommendations on products that are frequently purchased (more than 10 times). The reason is that I want to extract and study the mainstream purchasing patterns in states that have the greatest purchasing power, so that Olist can achieve higher efficiency with less effort. 

## Recommendations 
Using Association rule, I can obtain product bundles that are frequently purchased together.
#### Example of an useful rule
![image](https://user-images.githubusercontent.com/76879882/111888508-2c440400-89ab-11eb-9081-3c5aae97fa23.png)

Take this above rule as an example, product "6c3effec7c8ddba466d4f03f982c7aa3" and product "0aabfb375647d9738ad0f7b4ea3653b1" are frequently purchased together. (5 times out of 1000 transactions). Specifically, 83.3% of people that purchase product "5b8a5a9417210b1b84b67b9a7aefb935" also purchase "0aabfb375647d9738ad0f7b4ea3653b1". Hence, when customers browse on product "5b8a5a9417210b1b84b67b9a7aefb935", Olist can display products "0aabfb375647d9738ad0f7b4ea3653b1" as well. 







