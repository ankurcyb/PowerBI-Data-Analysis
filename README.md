# Sales Data Analysis of Chocolate Company through Power BI

We have sales data from a chocolate company, which includes information about each salesperson, the locations where they sell chocolate, the types of chocolate they sell, the quantities sold, details about the salespersons, teams, and cost details. 
First, we are cleaning the data, transforming the raw data into a more usable format. This includes removing null values and restructuring the schema according to our requirements. We are also linking different tables to create visualizations that are easy to understand. 
Next, we are analyzing data on sales, types of chocolate, quantities, locations, salespersons, teams, and sales details. 
Finally, we are performing trend analysis using forecasts to predict future sales of chocolate and amount of customers for the year 2022.



## Goals

  1. Data Clean up
  2. Data Analysis
  3. Trend Analysis using Forecasting


## Measure used

  1. Total Amount = SUM(sales[Amount])
  2. Total Boxes = SUM(sales[Boxes])
  3. Amount per Box = [Total Amount]/[Total Boxes]
  4. Total Customers = SUM(sales[Customers])



# Process

1. Data Cleanup 

  1. Load and Transform Data
  
     First we are going to load our excel sheet into Power BI and Transform our data according to our use case and requirements.
  
     ![image](https://github.com/ankurcyb/PowerBI-Data-Analysis/assets/141453942/3534b3ab-1c42-474d-bdbc-c3880579f992)
  
     Here we can see we have different data in different tables.
  
     ![image](https://github.com/ankurcyb/PowerBI-Data-Analysis/assets/141453942/5a8c1432-de73-4add-9423-2ca0fdf8e144)
  
     ![image](https://github.com/ankurcyb/PowerBI-Data-Analysis/assets/141453942/6be21606-2697-4f27-b532-ff955a8b21af)
  
     ![image](https://github.com/ankurcyb/PowerBI-Data-Analysis/assets/141453942/62eebdd3-029a-4257-a915-24c182215d39)
  
     ![image](https://github.com/ankurcyb/PowerBI-Data-Analysis/assets/141453942/4035146d-32ec-4e06-a7bb-7eaa44326fdd)
  
  2. Linking the tables in Model view with different names.
  
     In our data we can see in Locations table geography is named as Geo and in sales table it is geography, they have the same data. So we are going to link the table based on Geo and geography.
  
     ![ezgif-5-01724528ba](https://github.com/ankurcyb/PowerBI-Data-Analysis/assets/141453942/3318e135-5ad1-4241-80a8-6a2f0da55cd9)
  
  3. Number of Countries chocolates are sold to
  
     For this we will be creating a bar char based on Amount of chocolate is sold to each countries.
  
     ![image](https://github.com/ankurcyb/PowerBI-Data-Analysis/assets/141453942/c48af781-63b8-4495-939d-f0775a31183e)
  
     There is a blank value in country field, we will be fixing it by cleaning the data in Power BI.
  
     ![trim](https://github.com/ankurcyb/PowerBI-Data-Analysis/assets/141453942/4de1237c-3bc7-45d8-ada8-567e8fcbcbb8)
  
     Chart after cleaning the data.
  
     ![image](https://github.com/ankurcyb/PowerBI-Data-Analysis/assets/141453942/06a0a757-44c8-4de7-90db-b1d8d1386b04)
  
  
  4. Sales of chocolate by team
  
     For this, Bar chart is the perfect representation for Team sales.
  
     Here we can see that there is a blank data.
     
     ![image](https://github.com/ankurcyb/PowerBI-Data-Analysis/assets/141453942/10b528b1-e116-4862-ba57-aead2d59f8c0)
  
     So, if we click on the blank chart, we can see their number of sales in each countries.
  
     ![image](https://github.com/ankurcyb/PowerBI-Data-Analysis/assets/141453942/e23f2a36-caba-4f2b-bcf7-09e49f7f088c)
  
     Thus we can, conclude that they are not part of any team that is why they are in blank.
  
     ![image](https://github.com/ankurcyb/PowerBI-Data-Analysis/assets/141453942/2210a6d0-f50d-4cf2-b75f-6ea0583dc260)
  
     The table shows the people who are not a part of team.
  
     Through our Analysis we know that people with no team are showing up in blank. So, we are going to transform the data by replacing the null values with special to show the people who are not part of team comes in   
     special clause.
  
     ![ezgif-1-eed19aac81](https://github.com/ankurcyb/PowerBI-Data-Analysis/assets/141453942/135daa56-5dfe-466c-a759-83d2e10f5b4f)
  
     Results after cleanup.
  
     ![image](https://github.com/ankurcyb/PowerBI-Data-Analysis/assets/141453942/7bd36b35-99f1-49a3-9f63-61a9a318a1ef)



2. Data Analysis

    1. Analyzing the Sales Person Performance

       We will create a table to analyze the sales done by each sales person.

       ![image](https://github.com/ankurcyb/PowerBI-Data-Analysis/assets/141453942/a3efe922-c980-48b5-8b0d-20db507227ca)

       We will create calculation logic to do the analysis. We will create a new measure.

       Total Amount = SUM(sales[Amount])

       This measure basically calculates the total amount wherever the total amount is applied.

       Table after applying measure.

       ![image](https://github.com/ankurcyb/PowerBI-Data-Analysis/assets/141453942/8c2c376e-161d-48fa-9dee-26f0fb73ecdb)

       To add further customization, to sales according to team selected we will add a slicer.

       ![ezgif-6-2f3508bcd8](https://github.com/ankurcyb/PowerBI-Data-Analysis/assets/141453942/336723ed-fde0-4527-b94f-61ff29995d2f)

       ![image](https://github.com/ankurcyb/PowerBI-Data-Analysis/assets/141453942/3f3c8487-6218-434b-aaea-7eabfbcbeac2)

   2. Total Boxes

      We will create a new measure to calculate the total boxes.

      Total Boxes = SUM(sales[Boxes])

      ![image](https://github.com/ankurcyb/PowerBI-Data-Analysis/assets/141453942/705172b6-21be-4b2c-85e7-ab57ebecd557)

   3. Amount Per Box

      We will create a new measure to calculate the cost of every box.

      Amount per Box = [Total Amount]/[Total Boxes]

      ![image](https://github.com/ankurcyb/PowerBI-Data-Analysis/assets/141453942/8244d505-6d8e-4df1-b90f-82fe3847e997)

   4. Adding Display of sales Person for better visualization
  
      For this step, we will be transforming by adding custom URL to original data.

      ![image](https://github.com/ankurcyb/PowerBI-Data-Analysis/assets/141453942/6a5a265e-2e42-4ad8-9bc9-d862e643e396)

   5. Sales According to type of chocolate sold by each Sales Person and location
  
      We will be adding a column chart to show the type of chocolate sales of each sales person by selecting the the sales person and adding a filter to see the amount of each chocolate sold by them.
      
      ![ezgif-6-aff6510558](https://github.com/ankurcyb/PowerBI-Data-Analysis/assets/141453942/758511af-e646-40f1-9f8b-3b85c77082d1)

      we will add column chart to filter out location.

      ![ezgif-4-7b8c3194e1](https://github.com/ankurcyb/PowerBI-Data-Analysis/assets/141453942/ac399471-7562-4ac8-a682-566120eb1f8a)


   6. Final Dashboard

      The Final Dashboard is a visualization of the sales of each Sales person by their location, type of chocolate, Teams they belongs to, and amount sold by them.
      We can filter data of each sales person visually by interacting with the charts or selecting anything.

      ![image](https://github.com/ankurcyb/PowerBI-Data-Analysis/assets/141453942/6ff3b729-f6a7-4c0f-b466-d68e51a643f1)



3. Trend Analysis

   The sales data of chocolate has time and amount attached to it also with customers and amount of boxes sold per customer. We have sales data of the year 2021, and we will perform some trend analysis to Forecast the   
   sales of the year 2022.

   1. Customers serverd on daily basis Year 2021

      We will create a line chart to see the trend of the year 2021.
      We are putting Date on X-Axis and we want to know how many customers we are serving on that date. For this we will create a measure for total customers served.

      Total Customers = SUM(sales[Customers])
      We will put this measure on Y-Axis.

      Yearly Trend

      ![image](https://github.com/ankurcyb/PowerBI-Data-Analysis/assets/141453942/e46844a6-6731-40ef-86c8-8ccc3581dcee)

      Quarterly Trend

      ![image](https://github.com/ankurcyb/PowerBI-Data-Analysis/assets/141453942/11b23ede-1888-4dd4-8940-ac4a417420a9)

      Monthly Trend

      ![image](https://github.com/ankurcyb/PowerBI-Data-Analysis/assets/141453942/e5ff72af-ba32-4a3c-ba3f-535e80d04330)

   2. Filtering Trend based on type of chocolate
  
      We are adding a filter category in the legend of the graphy, so we can see the trend of each type of chocolate.

      ![image](https://github.com/ankurcyb/PowerBI-Data-Analysis/assets/141453942/fac0b3fe-c879-4167-977a-0ea312cfded8)

   3. Forecast for customers
  
      Here, we are forecasting the amount of customers for the next three months based on previous data, with a 95% confidence interval, meaning there is a 5% chance of error. Essentially, this means there is a 5% chance       that the actual sales will differ from the forecast. The forecast indicates that customoer amount will dip in January and remain stable in February and March, according to the trend line.

      ![image](https://github.com/ankurcyb/PowerBI-Data-Analysis/assets/141453942/1e6fc046-1092-42e1-866c-90f245aec414)

   4. Forecast for Total Amount

      Here, we are forecasting the Total amount of sales for the next three months based on previous data, with a 95% confidence interval, meaning there is a 5% chance of error. Essentially, this means there is a 5%     
      chance that the actual sales will differ from the forecast. The forecast indicates that sales will dip in January and remain stable in February and March, according to the trend line.

      ![image](https://github.com/ankurcyb/PowerBI-Data-Analysis/assets/141453942/9c043359-26f2-44b6-90c8-0392ecef2fb8)


# Conclusions

The project presents various visualizations of sales data, including information on customers, chocolate types, and locations. Through our analysis, we identified the interests of different customers in various locations for specific types of chocolate and discovered trends related to sales, locations, and chocolate types. We also performed a forecast to predict the growth of the customer base and the amount of chocolate sold. This forecast data can be used to determine customer needs and the types of chocolates to be sold to them.


# Acknowledgement

This Data Analysis and Power BI visualization is inspired through YouTube channel called [Chandoo](https://www.youtube.com/@chandoo_). 

  
