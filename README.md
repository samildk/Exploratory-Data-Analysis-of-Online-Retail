# Exploratory-Data-Analysis-of-Online-Retail
This repository is a personal project on an Online Retail dataset containing Time-Series Analysis and Customer which help us to reach to Insights and Recommendations for customers
- Removing Null values from dataframe
- Removing Duplicated values from dataframe
- Removing negative values for “Quantity” column.

Afterwards, our dataset reduced from 541909 rows to 392731 rows, and the data description seems reasonable. 

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/8fb19179-e93f-4874-b2ea-2bc035f651df/1cc86e06-5de3-4f17-8b1e-4bd676b4ba38/Untitled.png)

# Descriptive Analysis

The descriptive analysis provides an overview of the key variables in the dataset and helps identify any potential issues or patterns. 

## Numeric Variables

### Price

The initial histogram didn't provide much useful information, so I adjusted the bin size and range to better visualize the distribution of prices.

The refined histogram shows that the majority of the prices are within the range of 0 to 60, with a few outliers at higher prices.

> 💡 **Insights and Recommendation:**  Analyze the higher-priced products to understand if they are niche or premium offerings that can be better promoted to target customers who are willing to pay more. Additionally, review the lower-priced products to ensure they are still profitable and aligned with the overall pricing strategy.
> 

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/8fb19179-e93f-4874-b2ea-2bc035f651df/25c93885-3c28-4c60-9dc0-b430af3684bf/Untitled.png)

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/8fb19179-e93f-4874-b2ea-2bc035f651df/77e131c2-dd9b-4c63-aca5-bb4c301a7d19/Untitled.png)

### Quantity

Similar to the price analysis, the initial histogram didn't reveal much, so I adjusted the bin size and range to better showcase the distribution of the number of products in each basket.

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/8fb19179-e93f-4874-b2ea-2bc035f651df/20a9a6ec-b95b-481a-82e3-d4fd1659c842/Untitled.png)

The updated histogram shows a long-tailed distribution, with the majority of the baskets containing fewer than 200 products.

> 💡 **Insights and Recommendation: we can analyse the products with most number of purchases and recommend it to similar customers (based on following customer segmentation) or use the product neighboring in big baskets.**
> 

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/8fb19179-e93f-4874-b2ea-2bc035f651df/f380206a-34b7-4504-98a7-8893569a8e09/Untitled.png)

## Categorical Variables

### Country

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/8fb19179-e93f-4874-b2ea-2bc035f651df/8e167149-122c-4c02-8504-77c94cf40c01/Untitled.png)

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/8fb19179-e93f-4874-b2ea-2bc035f651df/71cd9ca1-75ed-4e56-b08e-c77fc73dd5ff/Untitled.png)

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/8fb19179-e93f-4874-b2ea-2bc035f651df/da7b1bb3-c4f0-45fe-997f-fd02916c90f5/Untitled.png)

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/8fb19179-e93f-4874-b2ea-2bc035f651df/9dd3c417-bf98-4ae4-9baf-ad758ac5bd9d/Untitled.png)

> 💡 **Insights and Recommendation:** The United Kingdom dominates the transaction volume, but there are opportunities to expand into other countries with significant, yet untapped, market potential. By analysing patterns in countries with large transaction volume and recommend the same pattern for products to smaller transaction volume countries. Also we can develop targeted marketing and expansion strategies to capitalize on these opportunities and diversify the customer base.
> 

### Date and Time Analysis

**Hour:** 

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/8fb19179-e93f-4874-b2ea-2bc035f651df/0545a065-3787-49cf-8164-66375631476e/Untitled.png)

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/8fb19179-e93f-4874-b2ea-2bc035f651df/c68f46ab-8b27-45b1-b4e5-8c14683292b8/Untitled.png)

**Day of week:**

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/8fb19179-e93f-4874-b2ea-2bc035f651df/477f5bdf-03fb-4995-adcb-883d22548061/Untitled.png)

 **Day of month:**

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/8fb19179-e93f-4874-b2ea-2bc035f651df/cfd77187-b7a6-4bc0-8599-21ac6f49e8da/Untitled.png)

> 💡 **Insights and Recommendation:** Analysing the time with most purchases we can send the recommendations for customers via Email or SMS (recommendations we wanted to send in other parts of our analysis) at this certain time interval. In this Analysis we should send the recommendations at the beginning of the month, at Thursdays (or wednesdays) between 10-15.
> 

# Time Series Analysis

## Daily Time Series:

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/8fb19179-e93f-4874-b2ea-2bc035f651df/47ee924f-2423-46b8-9347-cea4f9f8a8e7/Untitled.png)

## Weekly Time Series:

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/8fb19179-e93f-4874-b2ea-2bc035f651df/ad83b1df-2b20-4f31-b2a1-c905c2cabca8/Untitled.png)

## **Monthly Time Series:**

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/8fb19179-e93f-4874-b2ea-2bc035f651df/1a4eab62-5da4-4d82-bfeb-4e1380a1c8e1/Untitled.png)

From the daily/monthly/weekly time series we can see that the number of purchases was constant (very shallow increase with oscillations ) in the beginning of the year (2011). afterwards, it started to increase sharply from August to November. In the end, we can see that at december the purchases decreases sharply. we can trace the differences in purchase type or categories in growth era and understand certain categories or customers that make the change and recommend the items to customers with same clusters so we do not lose the growth or maybe the decrease at the end of time is because of lack of data in December which we can check the dates and December. By analysing the last month we can see that there are only 9 day of this month in our data set, which means there might be no decrease in the purchases. We can divide the purchases of  each day(or week/month) to the mean value of the purchases to see the pure trend. (due to the lack of time I didn’t report the result of this part)

# Customer Segmentation

In this part I did the following steps:

1. Calculated the 'total_purchase_amount' for each customer by multiplying the 'Quantity' and 'UnitPrice' columns. 
2. Grouped the data by 'CustomerID' and aggregated the 'total_purchase_amount' and 'Quantity' columns to get the total purchase amount and total quantity per customer.
3. Standardized the 'total_purchase_amount' and 'Quantity' features using StandardScaler.
Applied K-Means clustering with 4 clusters to segment the customers.
Visualized the resulting clusters using a scatter plot.
4. Removing the outlier customers reaching for better clustering.
5. Analyzed the characteristics of each cluster by printing the average total purchase amount, average quantity, and the number of customers in each cluster.

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/8fb19179-e93f-4874-b2ea-2bc035f651df/a479b8a9-f5cd-4a24-aac8-c8b9811c5051/Untitled.png)

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/8fb19179-e93f-4874-b2ea-2bc035f651df/23857268-a36a-4c52-9a7e-9f4019fb76d0/Untitled.png)

<aside>
💡 Cluster 0: (Low-Value Customers)
Average total purchase amount: 963.46
Average quantity: 560.98
Number of customers: 4004    ———————————————

This group of customers has the lowest average total amount spent and the lowest quantity of items bought compared to the other groups we identified.

Recommendation: Look into why these customers aren't as engaged with us, like maybe they're having trouble when they try to shop or we don't have the right products for them. Come up with ways to encourage them, like special deals, rewards programs, or suggestions for products they might like, to get them to buy from us more often and spend more money.

</aside>

      

<aside>
💡 Cluster 1: (Moderate-Value Customers)
Average total purchase amount: 42878.28
Average quantity: 27154.42
Number of customers: 26 ——————————————

The customers in this group have an average amount they spend and the average number of things they buy, which means they could possibly spend more.

Recommendation: Look into how these customers shop and what they like to buy, so we can suggest other things they might want to buy or get them to spend more. we can try targeted marketing and product suggestions to get them to spend more overall.

</aside>

<aside>
💡 Cluster 2: (High-Value Customers )
Average total purchase amount: 122748.08
Average quantity: 71121.75
Number of customers: 8                ———————————————

This group of customers spends the most on average and buys the most items.

Recommendation: Focus on these really valuable customers by giving them special treatment, like personalized experiences, exclusive deals, and VIP service. Put effort into building strong relationships with them and keeping them loyal, so they keep spending a lot with us.

</aside>

<aside>
💡 Cluster 3: (Moderate-Value Customers)
Average total purchase amount: 8002.77
Average quantity: 4625.83
Number of customers: 299 ——————————————— Like cluster 1

</aside>
