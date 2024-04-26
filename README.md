# MIST4610GroupProject2Team2
## Team Name:
21484 Group 2
## Team Members
1. Kush Santosh [@kushsantosh](https://github.com/kushsantosh)
2. Megan Aldinger [@meganaldinger](https://github.com/meganaldinger)
3. Patrick Daws [@PatrickD93](https://github.com/PatrickD93)
4. Priya Dey [@priyaadey](https://www.github.com/priyaadey)
5. Lucy Moon [@lucymoon505](https://github.com/lucymoon505/4610GroupProject1)
6. Ansley Williams [@ansleymw](https://github.com/ansleymw/ansley4610)

## Description of Data Set
The Real Estate Sales 2001-2021 dataset is an extensive record of real estate transactions compiled annually from October 1 to September 30 in Connecticut. It encompasses all sales exceeding $2,000 within this period, detailing vital information like the sale's town, property address, date, property type (ranging from residential to commercial and vacant land), sales price, and property assessment.

In essence, this dataset includes columns such as Serial Number, List Year, Date Recorded, Town, Address, Assessed Value, Sale Amount, Sales Ratio, Property Type, Residential Type, Non-Use Code, Assessor Remarks, OPM Remarks, and Location. Serial Number uniquely identifies each sale, List Year denotes the listing year, and Date Recorded marks the official recording date. Town and Address specify the property's location, while Assessed Value and Sale Amount are numerical representations of property value and sale price. Sales Ratio calculates the relationship between the sale amount and assessed value. Property Type and Residential Type detail property and residential subtype (e.g., single-family, condo).

Moreover, the dataset includes Non-Use Codes for designated properties, Assessor Remarks and OPM Remarks for additional notes, and Location for geographic coordinates. These latter attributes often contain null values, with only a few rows featuring actual strings.

Regarding data types, Serial Number, Assessed Value, and Sale Amount are all of type Integer. List Year and Date Recorded are both of type Date. Town, Address, Property Type, Residential Type, Non-Use Code, Assessor Remarks, and OPM Remarks are all Strings. Lastly, Location represents Geospatial Coordinates, which we have stored as strings.

## Question 1
Question: What is the comparison between the median sales amount of the various property types in Connecticut over time?

Importance: Our dataset includes property sales from 2006 to 2019. This is an important question because different-sized family homes might have different levels of change in sales, reflecting the growing class divide in the economy over time. This graph also clearly shows when the entire property market is affected by major economic events, like the 2007-2009 recession, where the median value for each property type declines together during that period. 

We needed to manipulate the dataset because when we first modeled it, we noticed a large gap in the line graph after the year 2019. It appears that the researchers who created this dataset decided to include entirely new property types, which skewed our data. Therefore, we decided to exclude them on our model. We did this by filtering the list year on our tableau model and deselected the years after 2019. The graphs show that 3 and 4-family homes show a sharp decline and rise in sales compared to single-family homes. This implies that individuals who live in lower-priced, multi-family homes may be more affected by changes in the economy than those who live in single-family homes. 

With 2020 and 2021: 
![Screenshot 2024-04-25 at 11 18 34 AM](https://github.com/kushsantosh/MIST4610GroupProject2Team2/assets/165107122/8486a7f4-4349-45c4-b9f7-358ba829a452)

Without 2020 and 2021: 
![Screenshot 2024-04-25 at 11 19 20 AM](https://github.com/kushsantosh/MIST4610GroupProject2Team2/assets/165107122/ee3ef238-7382-4671-b140-71f8e7e921bd)

## Question 2
Question: What is the average assessed value versus the average sale amount in Connecticut over time?

Importance: This is important, as we would like to see if the assessed value is a significant predictor of the average sale amount of properties in Connecticut. We found that this was not the case in the particular dataset, as both p-values were not less than .05 (Top p-value: 0.0918608 Bottom p-value: 0.421791). If this was actually the case, and average assessed value was a good predictor, we can see that the properties’ appraised values closely aligned with their final sales prices, therefore demonstrating a healthy and stable real estate market where both buyers and sellers have clear expectations. 

Again, we filtered out all null values to clean up the data. In the top line graph, we included property listings from 2006-2019 and forecasted through 2021. In the bottom line graph, we included the actual property listings from 2020 and 2021 as opposed to the forecasted values.  This is important because it shows that the actual values were much different than the forecast, which shows that the housing market can be volatile depending on the economy. While this cannot be entirely determined, we predict it could have been caused by things like COVID-19 and the beginning of a slight recession. This shows that a forecast is reliable in some circumstances but cannot account for all future factors that may impact the dataset. 

With 2020 and 2021:
![Screenshot 2024-04-25 at 11 23 20 AM](https://github.com/kushsantosh/MIST4610GroupProject2Team2/assets/165107122/f61ef5f4-765b-4f29-9190-b04c556dec8e)
Top p-value: 0.36889
Bottom p-value: 0.489951

With 2020 and 2021 Forecasted:
![Screenshot 2024-04-25 at 11 23 48 AM](https://github.com/kushsantosh/MIST4610GroupProject2Team2/assets/165107122/0b87efd6-16ab-4cbd-bf5c-87acbaf32fcb)
Top p-value: 0.0918608
Bottom p-value: 0.421791

## Tableau Packaged Workbook
The packaged workbook containing the visualizations shown above is attached to this repository.
