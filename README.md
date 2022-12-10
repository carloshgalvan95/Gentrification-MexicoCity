# Final-Project

## Presentation

### Increase in cost of living in Mexico City due to gentrification process

Recently, the government of Mexico City has signed a deal with Airbnb, the objective of this alliance is to capture 5% of the digital nomads in the world to move to Mexico City. The government of Mexico City estimates that this alliance would generate an economic spill of US$1.4 billion annually to various areas of the capital, it is expected that this will boost the local economy and promote the employment.

The increase in living costs, which includes housing prices, can cause a gentrification process and result in the expulsion of low-income households from the neighborhoods of greatest interest and popularity opens the door to real estate speculation.

In this context, we want to develop machine learning models to find which areas of Mexico City are the next to experiment a gentrification process in the close future.

#### Outline of the project

We been working in **develop machine learning models to find which areas of Mexico City are the next to experiment a gentrification process in the close future**. For this purpose, we begin to create the database and starting the data exploration analysis with these preliminary results:

1. For the price land unit ("Catastro") with the zip code and the lattitude and longitude coordinates of the areas ("colonias") of Mexico City, we clean the data and map where the value is higher by a heatmap:

![Grafica3.1](https://github.com/carloshgalvan95/Final-Project/blob/main/Control/Grafica1.3.PNG)

2. The Airbnb data that consist of the location of the apartments / houses / suites / lofts in Mexico City and their prices, we clean the data:

![Grafica3.2](https://github.com/carloshgalvan95/Final-Project/blob/main/Control/Grafica2.3.PNG)

3. As a measure of high-value business we use the number of starbucks and their locations, the database is clean now:

![Grafica3.3](https://github.com/carloshgalvan95/Final-Project/blob/main/Control/Grafica3.3.PNG)

#### Results

After the exploratory analysis, we deploy a the prediction model, the target was predicting the unit property value of the land given its characteristics, for this we determined radius of distance how many Airbnbs the neighbourhood had nearby as well as fetching the median price for one night stay, we also gathered all the starbucks located nearby. After building our initial database we use a multiple regression model to predict our target property value of the land given:

![Grafica3.4](https://github.com/carloshgalvan95/Final-Project/blob/main/Control/Grafica3.4.png)

With the predicted values, we map all the information to visualized the results. We can see in the next map the "original" price land (left) and the predicted price land (right), some areas turn more orange, that means that in this areas could experiment increases in the price land and takes to a increase of the cost of living:

![Grafica3.5](https://github.com/carloshgalvan95/Final-Project/blob/main/Control/Grafica3.5.PNG)

Also we could detect which areas (Colonias) could experiment increases of the price land, we took in consideration a growth rate between the "original" price land" and the predicted price land:

![Grafica3.6](https://github.com/carloshgalvan95/Final-Project/blob/main/Control/Grafica3.6.PNG)

#### Conclusions

As we collected the information and the databases for the project were completed, a data cleanup had to be carried out in order to work with this information.

Despite this, it was possible to develop a predictive model for the price land that provided us with useful information to be able to see which areas of Mexico City may undergo a gentrification process in the close future.

For more information, we did a presentation of the project on Google Slides is available [here](https://docs.google.com/presentation/d/1Ap996VHbBMpeXS1RzdqjnSDFi5lZDNWeR5sFTSoFnYE/edit?usp=share_link).

Also, we deploy a website for the project, is vailable [here](https://raulesqueda.github.io/test_web/).


