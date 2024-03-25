# Mavin-Toy-Dataset-Analysis
This is a Power BI Data Analytics Project for Mavin Toy Inc. 

![Intro Image jerry-wang-qBrF1yu5Wys](https://github.com/JoanUnachukwu/Mavin-Toy-Dataset-Analysis/assets/108992550/0db67b8b-d2ef-44eb-8e38-51cfc6eed6e2)


## Introduction

This is a Sales & inventory data for a fictitious chain of toy stores in Mexico called Maven Toys, including information about products, stores, daily sales transactions, and current inventory levels at each location.

## Problem Statement 
From the scenario, these are the problem statements to derive solutions for: 

- Which product categories drive the biggest profits? Is this the same across store locations? Electronics Category
- Can you find any seasonal trends or patterns in the sales data?
- Are sales being lost with out-of-stock products at certain locations? Yes. 
- How much money is tied up in inventory at the toy stores? How long will it last?

## Skills and Concepts Demostrated

- Power Query transformation
- Data modelling
- Calculated Measures
- Bookmarking
- Page Navigation
- Filters
- Tooltips
- Imported Icons & Toggle Buttons

## Visualization
The report comprises of 7 pages: 

1. Title Page
2. KPIs at a Glance
3. Top Selling Locations
4. Seasonal Trends
5. Out of Stock
6. Dashboard at a Glance
7. Insights

You can interact with the report [here]:(https://app.powerbi.com/links/Bt2PgR8MJh?ctid=124b8b49-ad03-4c2a-b001-cfbbe232a0cf&pbi_source=linkShare)

![Title Page Screenshot](https://github.com/JoanUnachukwu/Mavin-Toy-Dataset-Analysis/assets/108992550/e30a692d-8e49-4068-a2e7-7d9e500f9659)

Features:

A Power Point uniquely designed Title Page with the following features: 
- 6 Page Navigator Buttons with that navigates to the page with a similar name.
- A rectangular shaped element that embodies the title of the analysis.

## Data Sourcing
The data used is from a fictitious toy store derived from Maven Analytics. It is a folder containing for different 4 .csv files/tables namely inventory.csv, product.csv, stores.csv, sales.csv.

## Data Transformation

The dataset was extracted from source and transformed wuth the **Power Query Editor**.
The first row was made as headers and appropriately renamed for easy understanding. 

The following calculated measures were also created: 

1.	Total Units Sold = SUM(Sales[Units])

2. Total Revenue = SUMX(Sales, Sales[Units] * RELATED(Products[Product_Price]))

3. Cost Of Products Sold = SUMX(Sales, Sales[Units] * RELATED(Products[Product_Cost]))

4. Profit = [Total Revenue] — [Cost Of Products Sold]

5. Avg. Transcation Value = [Total Revenue] / COUNT(Sales[Sale_ID])

6. Gross Profit Margin = [Profit]/[Total Revenue]

8.	Avg. Revenue per Store = [Total Revenue] / COUNT(Stores[Store_Name])

9.	Total Inventory Amount = CALCULATE(SUM(products[Product Price]) * SUM(inventory[Stock On Hand]))


## Modelling
The data model is a star schema that creates relationships between the tables using primary and foreign keys. 


## Analysis & Visualizations

The Insights to the problem statement above are as follows (Screenshots Attached): 


1.  **Which product categories drive the biggest profits? Is this the same across store locations?**

    As Indicated on the "Top Sales by Category" bookmark, The TOY category had produced the biggest profits ($630,029)in the Downtown Location followed by the Electronics category driving reasonable profits of 
    $287,584 and $108,197 in the Commercial and Airport Locations respectively.
    For Gross profits generated, it is also indicated that the **Electronics categories** drive more percentage profits over time.

    ![Top Selling Locations](https://github.com/JoanUnachukwu/Mavin-Toy-Dataset-Analysis/assets/108992550/579c8820-849c-43cf-9168-c0d9ce6acbb1)


2.  **Can you find any seasonal trends or patterns in the sales data?**

    The  Sport and Outdoor departments generated low revenue in 2018 and 2017 compared to other categories. 
    The Electronics category experienced the lowest dip. However, the Arts category experienced a revenue surge in 2018 which could indicates a high demand due to creation of high demand toys.

    ![Seasonal Trends by Revenue andProfit](https://github.com/JoanUnachukwu/Mavin-Toy-Dataset-Analysis/assets/108992550/f35ec470-c3b9-4d55-9e4d-c4152e1bf336)


3.  **Are sales being lost with out-of-stock products at certain locations?**

    Yes. 
    About 39 stores currently have 0 products in certain locations.
    Downtown location has more stores with low stock (below 500 units) than other locations.

    ![Out of Stock](https://github.com/JoanUnachukwu/Mavin-Toy-Dataset-Analysis/assets/108992550/6bc046f9-85cc-4cd3-9e10-4a8683538e90)

4. **How much money is tied up in inventory at the toy stores? How long will it last?**

    There was over $15 million tied up in inventory from 1999 and lasted up until 2016.
   
![Out of Stock](https://github.com/JoanUnachukwu/Mavin-Toy-Dataset-Analysis/assets/108992550/cc9741e3-9f1f-4d91-a50d-c0253efb3f38)

## KPIs at a Glance

![KPIs at a Glance](https://github.com/JoanUnachukwu/Mavin-Toy-Dataset-Analysis/assets/108992550/42423d91-1ffa-468d-bbca-d4b48f799b6d)


## Final Dashboard Preview

![Dashboard at a glance](https://github.com/JoanUnachukwu/Mavin-Toy-Dataset-Analysis/assets/108992550/81d129a9-eb6a-40dc-9030-18a4c53b974c)


## Recommendations

- To avoid out of stock products, Mavin toy Store will have to increase their production capacity of highly sought products and distribute to respective locations. This might also be capital intensive and assets obtained. 

- For toy categories that generated low revenue like Sports and Outdoors, it is recommended to undertake a customer feedback survey and market survey to know the products desired by customers before production. 
  This will automatically improve sales for Sports and Outdoors category. 

