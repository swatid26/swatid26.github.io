## Pizza place sales analysis using Alteryx

**Project Description:** 
Here I am using data from Pizza sales company to analyze the trends in pizza orders received in the year 2015. 
The data has information about types of pizza, their ingredients, prices, quantity ordered, time and date of order. The data is distributed in 4 different tables 
for which I used Alteryx to cleanse, combine and summarize the data.

The objectives for this analysis are below:
1. Best and worst selling pizzas: Which Sizes and category of pizza are most popular?
2. Increase Revenue: 
   A: How much sales was gathered by each size category pizza in the year 2015?
   B: How the sales were spread across various months of the year 2015?
3. Improve Productivity: How the orders were distributed across months, days and time during the year?
4. Understand customer purchase behaviour: What is average order value on various days in a month?

The image below shows overall workflow created in Alteryx to achieve the desired results
<img src="images/Screenshot 2023-02-02 150023.png"/>

### 1. Best and worst selling pizzas: Which sizes and category of pizza are most popular?

The data is distributed in 4 different tables. To get this information I combined order details, orders, pizza types and pizza tables in Alteryx using join tool.
Order_id, pizza_id and pizza_type_id are common fields in 2 tables hence I used the join tool twice to get a master table which has information from all the 4 tables.

<img src="images/Screenshot 2023-02-01 152550.png"/>
<img src="images/Screenshot 2023-02-01 155235.png"/>

### 2. Increase revenue: 
A:How much sales was gathered by each size category pizza in the year 2015?

The master table created has information about sizes and maximum prices for each size of pizza. I filtered the data to show the sizes, category, prices and quantities ordered, Then Total sales gathered was calculated by creating a formula in Alteryx, multiplying quantities by prices. The data is then sorted in ascending order of sales revenue. 

<img src="images/Screenshot 2023-02-01 154150.png"/>
<img src="images/Screenshot 2023-02-01 154211.png"/>

B: How the sales were spread across various months of the year 2015?

The data has dates formatted in MM-DD-YYYY format. Using formula function in Alteryx, month number is extracted from the date. To understand the sales spread in more intuitive way, another table is created in Alteryx using Text Input command which contains information about month number and month name. Using join tool, and sorting the sales information in descending order, desired output is obtained.

<img src="images/Screenshot 2023-02-01 094104.png"/>

<img src="images/Screenshot 2023-02-02 133823.png"/>

### 3. Improve Productivity: How the orders were distributed across months, days and time during the year?
Extracting data about monthly orders, we can see that October month shows the least number of pizza quantities with highest in July. month of July shows 13% increase in pizza sales compared to October.

<img src="images/Screenshot 2023-02-02 133715.png"/>

Looking at the distribution among days in a month, we can see most orders come in middle of the month, with least at the end of the month.

<img src="images/Screenshot 2023-02-02 180611.png"/>
<img src="images/Screenshot 2023-02-02 180631.png"/>

Data below clearly shows most orders are concentrated around meal times (lunch hours from 12 pm to 1 pm) and dinner hours from 4 pm to 7 pm.

<img src="images/Screenshot 2023-02-02 175458.png"/>

### 4. Understand customer purchase behaviour: What is average order value on various days in a month?
While each pizza category has different prices, we can calculate AOV (Average Order Value) which represents on average how much the customer is willing to spend each time they place an order at the pizza place. 
We can easily see that customers are spending around $16-17 per order.

<img src="images/Screenshot 2023-02-02 142838.png"/>
<img src="images/Screenshot 2023-02-02 142856.png"/>

### Insights
1. Looking at the sales report based on various sizes of pizza, Large size pizzas are the most popular. Interrestingly, the trend does not seem to be because of price of the large pizzas (small and medium pizzas are cheaper than large pizzas). 
2. XXL pizzas are least popular with only handful of orders in the entire year with minimal revenue generated. So, the pizza place can evaluate if they want to hold off producing XXL size pizzas and allocate those respources to producing more L size pizzas.
3. Large size pizzas in chicken category are the single most popular which fetched maximum orders in the entire year to generate maximum sales, when they are priced at $20.75 per pizza
4. Also, it is interesting to note that small size pizzas in classic category are ahead in number of total orders. However when we look at the breakdown of small size classic pizzas by price, classic small sized pizzas priced at $12 per pizza are the most popular
5. To efficiently manage resources, the pizza place can allocate more resources in the month of October and in general around middle of the months. Meal times (Lunch and dinner) are the busiest, so it is best to consider stock, seating capacity and resources to be prepared to serve more customers during these times. The pizza place can also manage influx of orders concentrated around meal times by setting up pre-orders, takeout or drive through options to efficiently distribute resources.
6. Customers are willing to pay around $16-17 each time they place the order. We can compare it with the major competition to understand if our prices are competitive to attract and retain the customers.

Data Source https://www.kaggle.com/datasets/mysarahmadbhat/pizza-place-sales
