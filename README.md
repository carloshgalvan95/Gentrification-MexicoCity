# Final-Project

## Presentation

### Increase of the cost of living in Mexico City due to gentrification process

#### Background

Gentrification is often described as the change in the socioeconomics of a neighborhood, it is also defined as the replacement of low-value businesses by high-value businesses. <sup> 1 <sup> 

Recently, the goverment of Mexico City has signed a deal with Airbnb, the objective of this alliance is to capture 5% of the digital nomads in the world to move to Mexico City. The goverment of Mexico City said that this alliance would generate an economic spill of US$1.4 billion anually to various areas of the capital, it is expected that this will boost the local economy and promote the employment. <sup> 2 <sup>

In the last 17 years, the average increase in housing prices in the Mexico City Metropolitan Area, which includes Mexico City, part of the State of Mexico and Hidalgo has been 235%, 64% above inflation, according to the Federal Mortgage Society (SHF). <sup> 3 <sup>

The increase in living costs, which includes housing prices, can cause a gentrification process and result in the expulsion of low-income households from the neighborhoods of greatest interest and popularity opens the door to real estate speculation.

In this context, we want to **develop machine learning models to find which areas of Mexico City are the next to experiment a gentrification process in the close future.**

For this purpose, we built a database based on these sources:

1. From the goverment of Mexico City, we took the open data related to "Información Catastral de la Ciudad de México". As the cost of living, we use the mean of the unit value of land ("Valor unitario del suelo") with the zip code and the lattitude and longitude coordinates of the areas ("colonias") of Mexico City. <sup> 4 <sup>

2. The Airbnb data used for the database consist of the location of the apartments / houses / suites / lofts in Mexico City and their prices, the data comes from listings <sup> 5 <sup>

3. As a measure of gentrification, we use the number of startbucks and their locations, the data are from the Starbucks Locations Worldwide database. <sup> 6 <sup>

Then, with the data, the analysis and the deployment of the models, we want to answer the following questions:

- Which areas of Mexico City could be gentrificated?

- How much the value of land could change?

- Could the presence of high value business accelerate the process of gentrification?

## Machine Learning Model

The chosen model to use for this prediction of value price given the amount of Airbnbs and Starbucks nearby within a set radius from the property is a Multiple Regression model. The reason for choosing this type of model is given that we expect to predict a numeric value in the form of property price.

The metodology is quite straightforward:
1. First parsing every row of our property database (db_catastro.csv) using Google Maps Geocoding API, declaring in the parameters the type : *Cafe* then using regex, determining if the cafe found is indeed an starbucks, counting how many we can find for every property.

2. Then using our airbnb database (airbnb.csv) with the values of latitude and longitude, utilizing once again the geocoding API and pairing it with our property databse to parse for Airbnbs within the radius chosen and counting how many we can find for each.

3. Finally appending those two values into columns in our catastro_df Pandas DataFrame.

4. Declare independent variables in *X* (Number of Starbucks per property, Number of Airbnbs per property).

5. Declaring our target variable in *y* (Property Value).

6. Splitting our data into train and test groups.

7. Generating and fitting the model to then also generate our predictions.


## Communications Protocol

For the final project we made a chat group in Slack with all the members of the team, we defined this channel as the first option to communicate all our findings to the team and share information.

Everytime we upload files to github we have to communicate this in the Slack chat.

To have meetings, we use zoom to chat and work on this project.

 #### Bibliography
 
<sup> 1 <sup>     

Hawkins, Ahmed, Roorda, & Habib (2022), Measuring the process of urban gentrification: A composite measure of the gentrification process in Toronto. Cities, Volume 126, Available in: https://doi.org/10.1016/j.cities.2022.103708 

<sup> 2 <sup> 

Gobierno de la Ciudad de México (2022), Unen esfuerzos Gobierno capitalino, UNESCO y Airbnb para convertir a la Ciudad de México en capital del turismo creativo. Available in: https://www.jefaturadegobierno.cdmx.gob.mx/comunicacion/nota/unen-esfuerzos-gobierno-capitalino-unesco-y-airbnb-para-convertir-la-ciudad-de-mexico-en-capital-del-turismo-creativo

<sup> 3 <sup>

Washington Post (2022), Airbnb agrava una crisis de vivienda que ya existía en Ciudad de México. Available in: https://www.washingtonpost.com/es/post-opinion/2022/11/10/airbnb-cdmx-departamentos-gentifricacion-desplazamiento/ 

<sup> 4 <sup>
 
 Gobierno de la Ciudad de México (2022), Información Catastral de la Ciudad de México. Available in: https://datos.cdmx.gob.mx/dataset/informacion-catastral-de-la-ciudad-de-mexico

<sup> 5 <sup>

Inside Airbnb (2022), Get Data. Mexico City, Distrito Federal, Mexico. Available in: http://insideairbnb.com/get-the-data/
 
<sup> 6 <sup>

Kaggle (2017), Starbucks Locations Worldwide. Available in: https://www.kaggle.com/datasets/starbucks/store-locations
