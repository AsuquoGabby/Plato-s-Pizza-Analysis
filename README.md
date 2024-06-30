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

![002](https://github.com/AsuquoGabby/Platos-Pizza-Analysis/blob/main/03.png)
