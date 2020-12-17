 # CO2 Emissions Final Project

This repository contains data on carbone dioxyde around the world. The data of two websites are being scrapped to be able to analyze more accurately how a country's population affects the quantity it produces. When only one factor is taken to draw conclusions on 

You can view visualizations of these data on the [my deployed website at: ](https://emissionsproject.herokuapp.com/). Additional data related to CO2 Emissions is available via [List of countries by Carbon Dioxide Emissions](https://en.wikipedia.org/wiki/List_of_countries_by_carbon_dioxide_emissions) and [List of countries by population in 2005](https://en.wikipedia.org/wiki/List_of_countries_by_carbon_dioxide_emissions). 

Data are preliminary and subject to change. My goal is to learn more about how to automate my page so the data gets scrapped and updated live. 

***

This Readme includes:
- Important changes (by date)
- Key Technical notes
- Contents

***
## Important: Changes on December 1, 2020

After finalizing the decision on which sites I was going to scrape I was able to:
- Create a py script that when call will start the scraping process, clean the data and organize it in a presentable way before returning it to my import_script.py to create the database.


## Important: Changes on December 5, 2020

- The class to create my database was created to include the attributes that will generate each column


## Important: Changes on December 7, 2020

- The finalization of my import_script.py completed the database creation. 

## Important: Changes on December 9, 2020

- Once my database was functional, the next step was concentrating in my API

- I created a total of 6 routes that will return the data stored in my database illustrated in different formats.

## Important: Changes on November 9, 2020

- My API was launched to the web using Heroku as my deployment Platform.

***
