# Platos Pizza Analysis
![picture intro](https://github.com/AsuquoGabby/Platos-Pizza-Analysis/blob/main/picture%20intro.png)

## Plato’s Pizza Analysis
Tools used: Power BI

Power Bi is a powerful business intelligence tool develop by Microsoft. It allows users to create interactive and visually appealing reports and dashboard using data from various form. With Power Bi, Users can connect to multiple data sources (Excels workbook, SQL Server, Web Text/CSV and many more) transform and clean data, and create beautiful visualization. With the Plato Pizza project a lot of Power Bi function was utilize including Connecting to a data source transforming and cleaning data, and creating dashboard.
## Problem Statement
Every Business needs a Data analyst, The role of a data analyst in a restaurant involves leveraging data to provide insights and support informed decision-making to improve operation and customers experiences. The Plato’s pizza restaurant deals with the sales of pizza of different size and type, the analysis would focus on understanding, analyzing and interpreting the data from the restaurant to provide room for improvement for the restaurant 

## Objectives 
The main objectives of the project are to Create room for improvement in the restaurant by looking for opportunities to drive more sales and work more efficiently. Below are a few questions the project would answers:
* What are our best and worst selling pizzas? 
* What's our average order value? 
* How much money did we make this year? Can we identify any seasonality in the sales?
* All these questions would help drive more sales and work more efficiently.
* What days and times do we tend to be busiest?
## Data Sources
The Plato’s Pizza Datasets was provided by Tina Okonkwo for the 14 Week learning Data Analysis Challenge on X. This Datasets Contain details about the sales of the pizza ranging from the pizza details, Orders details, Date and time the orders were made. All this together were made up of four different excel files (CSV files) order_details, orders, pizza_types and pizzas.
Load Data 
I downloaded the data from twitter as a zip file after unzipping it I imported it into power query (Power Bi Home > Get Data > Text/CSV) then select the datasets do this for all four datasets, it was successfully loaded into power query where I did some basic cleaning on the datasets like changing the data to the right datatype and many more 
## Data Modelling
Data Modelling is simply the act of organizing data into tables based on grouping and relationship to reduce redundancy and optimize efficiency.  Data Model are made up of Fact table and Dimension table. Fact tables are where the main business events are while the dimension tables are where the description (entities) of the business event are. Each table is made up of a primary key (unique identifiers) and foreign key as this would serve as a basic of linking with others table.

The Star Schema data model seems to be the best for this data modeling process, in Star Schema model the central fact table is connected to multiple dimension tables through foreign key relationships. I merge two tables to serve as the fact table (orders_details and pizza) to merge both tables while still on the orders_details in power query (power query home > Merge Queries >Merge Queries as new (a dialogue box would appear select the pizza table and click on pizza id from both table) > Click Ok) that would serve as the fact table since it contains the foreign key for others tables 
We would be left with three tables with as shown below

**Orders tables**

![001](https://github.com/AsuquoGabby/Platos-Pizza-Analysis/blob/main/01.png)

**Pizza_type table** 

![002](https://github.com/AsuquoGabby/Platos-Pizza-Analysis/blob/main/02.png)

**Fact tables**

![003](https://github.com/AsuquoGabby/Platos-Pizza-Analysis/blob/main/03.png)

Close and load data into power Bi, power Bi Automatically tries to create a data model.  You can edit the relationship to whatever seems pleasing to you 

![004](https://github.com/AsuquoGabby/Platos-Pizza-Analysis/blob/main/04.png)

It is important to check if the data Model is correct one way we can do so is by creating a table or matrix on the report view and Adding columns from different tables that should be related If you see unexpected repetitions or mismatched values, it indicates potential issues with your relationships.

## Write some Dax function
DAX (Data Analysis Expression) is a formula language and expression language used in Power bi and Microsoft Excel. Similar to Excel function but is more powerful and versatile, allowing users to create complex calculations, and manipulate data. Dax function can be used to create measure, calculated columns, and calculated tables. In the case of this project some basic Dax function was used to make the work easier. Some Dax function used in this project includes:
Create a Date Table to make working with date and time easier, creating an additional column in my fact table to calculate the total price which is the quality sold * price.

## Objectives 
### What are our best and worst selling pizzas


Knowing which pizza yields the highest sales would help the restaurant focus on producing and maintaining the quality of such pizza in the long run. I plotted the Total Price against Pizza name, which can easily help us identify the best-selling pizza and the worst-selling pizza, I filtered my chat and showed only the top ten (10) best-selling pizzas and top 10 Worst-selling pizzas. it was discovered that some pizzas performed well in terms of sales most likely because people enjoy having them more as the top selling pizza is one of the most expensive at Plato Pizza. They are as follows:

**The Thai Chicken Pizza** with a total quantity of 2371 sold and Total sales of $43,434 follow by **The Barbecue Chicken Pizza** with a total quantity of 2432 sold and Total Sales of $42768 and then **The California Chicken Pizza** with a total quantity of 2370 sold and Total sales of $41409.5. 

![006](https://github.com/AsuquoGabby/Platos-Pizza-Analysis/blob/main/06.png)

### Worst selling pizzas
Just as they are some pizzas performing well in sales some are still lagging behind, they include the following **The Brie Carre Pizza** with a total quantity of 490 sold and Total sales of $11588.50 follows by **The Green Garden Pizza** with a total quantity of 997 sold and Total sales of $13955.75 follows by **The Spinach Supreme Pizza** with a total quantity of 950 sold and Total sales of $15277.75.

![007](https://github.com/AsuquoGabby/Platos-Pizza-Analysis/blob/main/07.png)

I would recommend that Plato Pizza should focus more on pizza that yields really high sales while still producing those that yield little sales but in a small quantity.


## How much money did we make this year? Can we identify any seasonality in the sales?
A total of $817.86k was made for the year 2015, to better understand the sales trend for the year I plotted a line chart that shows the sales for each month for 2015 


![008](https://github.com/AsuquoGabby/Platos-Pizza-Analysis/blob/main/08.png)

They opened the 2015 sales year on a good note as sales for January were almost at $70K. However, there was a serious decline in sales for the month of February as it went below $65K. By March, the restaurant experienced an increase in sales which continued gradually until July. There was a decline in sales from August to September, with sales below $65K. For November, there was an increase in sales, though it was less than $70K but greater than $65K. Sadly there was a slight decline in sales in December as they closed their sales year with around $68K. 

Trend it was observed from the plot that the Restaurant tends to make more sales during Summer and this is most likely because the summer is for Outdoor Activities such as vacations, outdoor sports, festivals, and barbecues, and in this period, people tend to purchase fast food a lot. 

## What days and times do we tend to be busiest?
To best answer this question, I use a bar chat to show the number of sales for each day while using a heatmap to show the number of sales for each hour of the day.


![009](https://github.com/AsuquoGabby/Platos-Pizza-Analysis/blob/main/09.png)

From the plot above, we can easily tell what day and time we tend to be busiest. The shop opens at 9 a.m. daily, and from the above plot, the restaurant makes very little or, on some days, no sales during the first opening hour of the day, and likewise during the second opening hour of the day. By 11 a.m., it can be seen that there is an increase in the number of sales, and by 12 p.m. and 1 p.m., the restaurant receives more orders. This particular time can be said to be the busiest time of the day for Plato’s Pizza, as the number of sales sometimes amounts to over 1000. The order fluctuates after 1 p.m. until the restaurant closes. And Friday is the busiest day of the week.


Below is the Plato’s Pizza Dashboard 

![009](https://github.com/AsuquoGabby/Platos-Pizza-Analysis/blob/main/Dashboard.png)



