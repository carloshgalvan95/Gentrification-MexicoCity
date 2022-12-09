# How to answer our questions
Why did we use Starbucks and Airbnb as our input data? Given that gentrification doesn’t have a set metric to evaluate, and considering that the initial thought for people from other countries is “if this city satisfies all of my needs and it’s cheaper to live there why not move in?” we assumed that one of this needs is going to be looking for the same franchises available there and what better example of this than Starbucks.

# Defining our variables
The thought process behind using Airbnb is mainly due to a correlation in growth observed in google trends for both searches in Mexico, Airbnb had a surge in popularity in 2017 that we can perfectly pair to the moment the term “gentrification” started to appear in searches in Mexico.

# Turning words into action
For the prediction model, the target was to focus on two main target variables. For the first one, the target variable was to predict the unit property value of the land given its characteristics.

For this, we chose to center the analysis on using the information we gathered and paired using a previously determined radius of distance how many airbnbs the neighborhood had nearby as well as fetching the median price for one night stay. We also gathered all the Starbucks locations nearby.

After constructing our initial database we use a multiple regression model to predict our target property value of the land given, as previously mentioned the no. of Starbucks within the radius, the no. of airbnbs, and the median price of those airbnbs.

Afterward, to test our model further we used a decision tree model and pass a column of “flag Airbnb” and “flag_starbucks” to see if, given our predicted data, we could also predict the existence of either an Airbnb or Starbucks nearby.
