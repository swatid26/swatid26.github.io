## Pizza sales analysis using Alteryx

**Project description:** 
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



### 2. How much sales was gathered by each size category pizza in the year 2015?

The master table created has information about sizes and maximum prices for each size of pizza. I filtered the data to show the sizes,prices and quantities ordered, Then Total sales gathered was calculated by creating a formula in Alteryx, multiplying quantities by prices. The data is then sorted in descending order of sales revenue. 

<img src="images/Screenshot 2023-02-01 093551.png"/>

### 3. How the sales were spread across various months of the year 2015?



### Interactive dashboard using excel

The data cleaning, manipulation and extraction was done in Alteryx to extract the data in the form of an excel sheet. Further the visualization capabilities of excel are used to create an interactive dashboard which summarizes observations mentioned above.



For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).
