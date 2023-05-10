# Bike Sharing Assignment (Multiple Linear Regression)

## Problem Statement

This assignment requires building a multiple linear regression model to predict the demand for shared bikes. 

### Background

Bike-sharing systems provide short-term bike rentals to individuals for a fee or free of charge. Users can borrow a bike from a "dock" and return it to another dock belonging to the same system. However, the Corona pandemic has caused a significant decline in the revenues of a US bike-sharing provider, BoomBikes. To prepare for the end of the lockdown and the restoration of the economy, BoomBikes wants to understand the factors affecting the demand for shared bikes in the American market.

### Objectives

BoomBikes has contracted a consulting company to understand the significant variables that affect the demand for shared bikes and how well they describe the bike demands. The company wants to know:

-   Which variables are significant in predicting the demand for shared bikes.
-   How well those variables describe the bike demands.

### Dataset

Based on various meteorological surveys and people's styles, the service provider firm has collected a large dataset on daily bike demands across the American market based on some factors.

### Business Goal

The primary goal of this assignment is to model the demand for shared bikes using the available independent variables. This model will help the management understand how the demands vary with different features, allowing them to manipulate the business strategy to meet the demand levels and meet the customer's expectations. Furthermore, the model will enable the management to understand the demand dynamics of a new market.

### Data Preparation

1.  We can observe in the dataset that some of the variables like '**weathersit'** and '**season'** have values as 1, 2, 3, 4 which have specific labels associated with them (as can be seen in the data dictionary). These numeric values associated with the labels may indicate that there is some order to them , hence we  convert such feature values into categorical string values before proceeding with model building.   
    
2.  We notice the column  **'yr'**  with two values 0 and 1 indicating the years 2018 and 2019 respectively. At the first instinct, we might think it is a good idea to drop this column as it only has two values so it might not be a value-add to the model. But in reality, since these bike-sharing systems are slowly gaining popularity, the demand for these bikes is increasing every year proving that the column 'yr' might be a good variable for prediction. Hence it will not be dropped.

### Dataset characteristics

day.csv have the following fields:
	
	- instant: record index
	- dteday : date
	- season : season (1:spring, 2:summer, 3:fall, 4:winter)
	- yr : year (0: 2018, 1:2019)
	- mnth : month ( 1 to 12)
	- holiday : weather day is a holiday or not (extracted from http://dchr.dc.gov/page/holiday-schedule)
	- weekday : day of the week
	- workingday : if day is neither weekend nor holiday is 1, otherwise is 0.
	+ weathersit : 
		- 1: Clear, Few clouds, Partly cloudy, Partly cloudy
		- 2: Mist + Cloudy, Mist + Broken clouds, Mist + Few clouds, Mist
		- 3: Light Snow, Light Rain + Thunderstorm + Scattered clouds, Light Rain + Scattered clouds
		- 4: Heavy Rain + Ice Pallets + Thunderstorm + Mist, Snow + Fog
	- temp : temperature in Celsius
	- atemp: feeling temperature in Celsius
	- hum: humidity
	- windspeed: wind speed
	- casual: count of casual users
	- registered: count of registered users
	- cnt: count of total rental bikes including both casual and registered
	

**Dataset License:**

Use of this dataset in publications must be cited to the following publication:

[1] Fanaee-T, Hadi, and Gama, Joao, "Event labeling combining ensemble detectors and background knowledge", Progress in Artificial Intelligence (2013): pp. 1-15, Springer Berlin Heidelberg, doi:10.1007/s13748-013-0040-3.

@article{
	year={2013},
	issn={2192-6352},
	journal={Progress in Artificial Intelligence},
	doi={10.1007/s13748-013-0040-3},
	title={Event labeling combining ensemble detectors and background knowledge},
	url={http://dx.doi.org/10.1007/s13748-013-0040-3},
	publisher={Springer Berlin Heidelberg},
	keywords={Event labeling; Event detection; Ensemble learning; Background knowledge},
	author={Fanaee-T, Hadi and Gama, Joao},
	pages={1-15}
}


Contact

For further information about this dataset please contact Hadi Fanaee-T (hadi.fanaee@fe.up.pt)


### Author
Godwin Paul Vincent