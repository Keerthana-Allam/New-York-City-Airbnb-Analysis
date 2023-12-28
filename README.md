# New-York-City-Airbnb-Analysis: Project Overview
New York City Airbnb Market Analysis and Price Prediction
Analyzing the dynamic NYC Airbnb market: Predicting prices, exploring geographical trends, and understanding key factors. Utilized predictive modeling and interactive dashboards for comprehensive insights. Team project by [@Nihith Nath Kandikattu](https://github.com/nihith-nath), [@Keerthana Allam](https://github.com/Keerthana-Allam), Hithesh Kumar Duttuluri, and Charan Sai Pandaraboyina.

# Problem Statement   

In the ever-changing landscape of the New York City Airbnb market, our project aims to analyze data and predict prices, offering valuable insights for potential investors and discerning customers. Our main goal is to discover patterns that reveal areas with the highest number of listings, understand the factors influencing different costs, and grasp the preferences of both hosts and guests. By exploring the complex interactions between neighborhood characteristics, seasonal demand, and pricing dynamics, our research aims to equip new investors with decision-making tools and provide customers with a strategic advantage in selecting listings based on their preferences and budget constraints. This project provides a comprehensive understanding for hosts and guests, offering a valuable resource for strategic decision-making in the dynamic and popular Airbnb market.   

## Key  Focus  Areas:   
Investigating geographical distribution, pricing  dynamics, customer experiences, and  availability patterns in the dataset to inform strategic decisions for both hosts and guests to enhance the overall Airbnb experience.  

## Data Utilization:   
Employing latitude/longitude coordinates for geographical visualization and analyzing essential metrics such as price, reviews, and availability to derive meaningful insights from the dataset.  

# Code and Resources Used:   
## Dataset   
The dataset was obtained from [Kaggle](https://www.kaggle.com/datasets/thedevastator/airbnbs-nyc-overview). It comprises a dataset of size [48896*16] with columns including listing names, host details, location coordinates, pricing, and availability metrics.   

**Python Version:** 3.10   

**Packages:** sqlite3, pandas, numpy, tabulate, folium, matplotlib, seaborn, plotly, dash, scikit-learn, scipy

# Metadata   

| Column Name                    | Description                                           |   
| ------------------------------ | ----------------------------------------------------- |   
| listing_id                     | The unique id of the Airbnb listing. (Integer)        |   
| listing_name                   | The name of the Airbnb listing. (String)              |
| host_id                        | The id of the host of the Airbnb listing. (Integer)   |
| host_name                      | The name of the host of the Airbnb listing. (String)  |
| neighbourhood_grp              | The neighbourhood group the Airbnb listing is located in. (String) |
| Neighborhood                   | Neighborhood information for each listing (String)    |
| latitude                       | The latitude coordinate of the Airbnb listing. (Float) |
| longitude                      | The longitude coordinate of the Airbnb listing. (Float)|
| room_type                      | The type of room offered by the Airbnb listing. (String)|
| price                          | The price per night of the Airbnb listing. (Integer)  |
| minimum_nights                 | The minimum number of nights required for booking the Airbnb listing. (Integer) |
| number_of_reviews              | The total number of reviews the Airbnb listing has received. (Integer) |
| last_review                    | The date of the last review the Airbnb listing has received. (Date) |
| reviews_per_month              | The average number of reviews the Airbnb listing receives per month. (Float) |
| calculated_host_listings_count | The total number of listings the host has. (Integer)  |
| availability_365               | The number of days the Airbnb listing is available for booking in a year. (Integer) |   

# Data Cleaning
• Parsed the TSV file to extract the header and listing data.   
• Cleaned the data by renaming columns, removing unwanted columns, and handling missing values.   
# Normalization
• Created an SQLite database and set up tables for Host, Neighborhood, and Listings.   
• Normalized the data to eliminate transitive dependencies, improving data integrity.    
• We have created a normalized database comprising 3 tables: a Host Table (HostID primary key), a Neighborhood Table (NeighborhoodID primary key), and a Listing Table (ListingID primary key) that has both HostID and NeighborhoodID as Foreign keys.

![Relational Schema](https://github.com/Keerthana-Allam/New-York-City-Airbnb-Analysis/assets/150170576/aec40a63-2ed5-42f7-8e9e-36e660aa997c)
## Host Table:   
+---+--------+----------+------------------+
|   | HostID | HostName | NumberOfListings |
+---+--------+----------+------------------+
| 0 |  2438  |  Tasos   |        1         |
| 1 |  2571  |  Teedo   |        1         |
| 2 |  2787  |   John   |        6         |
| 3 |  2845  | Jennifer |        2         |
| 4 |  2868  | Letha M. |        1         |
+---+--------+----------+------------------+








