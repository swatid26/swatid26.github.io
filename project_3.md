## Pizza place sales analysis using Alteryx

**Project Description:** 
Here I am using data from Pizza sales company to analyze the trends in pizza orders received in the year 2015. 
The data has information about types of pizza, their ingredients, prices, quantity ordered, time and date of order. The data is distributed in 4 different tables 
for which I used Alteryx to cleanse, combine and summarize the data.

The objectives for this analysis are below:
1. Which Sizes and category of pizza are most popular?
2. How much sales was gathered by each size category pizza in the year 2015?
3. How the sales were spread across various months of the year 2015? 

The image below shows overall workflow created in Alteryx to achieve the desired results
<img src="images/Screenshot 2023-01-31 170602.png"/>

### 1. Which sizes and category of pizza are most popular?

The data is distributed in 4 different tables. To get this information I combined order details, orders, pizza types and pizza tables in Alteryx using join tool.
Order_id, pizza_id and pizza_type_id are common fields in 2 tables hence I used the join tool twice to get a master table which has information from all the 4 tables.

<img src="images/Screenshot 2023-02-01 152550.png"/>
<img src="images/Screenshot 2023-02-01 155235.png"/>

### 2. How much sales was gathered by each size category pizza in the year 2015?

The master table created has information about sizes and maximum prices for each size of pizza. I filtered the data to show the sizes, category, prices and quantities ordered, Then Total sales gathered was calculated by creating a formula in Alteryx, multiplying quantities by prices. The data is then sorted in ascending order of sales revenue. 

<img src="images/Screenshot 2023-02-01 154150.png"/>
<img src="images/Screenshot 2023-02-01 154211.png"/>

### 3. How the sales were spread across various months of the year 2015?

The data has dates formatted in MM-DD-YYYY format. Using formula function in Alteryx, month number is extracted from the date. To understand the sales spread in more intuitive way, another table is created in Alteryx using Text Input command which contains information about month number and month name. Using join tool, and sorting the sales information in descending order, desired output is obtained.

<img src="images/Screenshot 2023-02-01 094104.png"/>

### Insights
1. Looking at the sales report based on various sizes of pizza, Large size pizzas are the most popular. Interrestingly, the trend does not seem to be because of price of the large pizzas (small and medium pizzas are cheaper than large pizzas). 
2. XXL pizzas are least popular with only handful of orders in the entire year.
3. Large size pizzas in chicken category are the single most popular which fetched maximum orders in the entire year to generate maximum sales, when they are priced at $20.75 per pizza
4. Also, it is interesting to note that small size pizzas in classic category are ahead in number of total orders. However when we look at the breakdown of small size classic pizzas by price, classic small sized pizzas priced at $12 per pizza are the most popular


For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).
