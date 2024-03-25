<br>
Predicting housing prices of California districts derived from the 1990 census 
<br>
**Introduction:**
<br>
Introduction:
My goal was to use the 1990 Census of California houses to determine the relationship between median house values and various variables that could affect it, such as ocean proximity and room ratio. 

I wanted to determine what attributes of a house has and can determine its price range.

<br> 

Data derived from: https://www.kaggle.com/datasets/camnugent/california-housing-prices?resource=download

**Methods**
1. In order to preprocess the data, I converted categorical features (i.e. ocean proximity - <1 hour away, inland, near bay>)
into binary values. Segregating proximity by 0 and 1, within 1 hour distance and farther than 1 hour distance (respectively).

2. I then added new features to create a smoother data structure by including how many a bedroom ratio (how many bedrooms per room) and a household rooms (how many rooms per household) to help provide information on a components that contribtue to a house's monetary value/customer appeal.

3. After pre-procesisng of the data had been complete, I trained a linear regression model first to model the relationship between our control, median house value and other various
independent variables, such as the ones mentioned above. This produces a regressor score (coefficient of determination) of : TBA

4. After this was done, I then converted to using a RandomForestRegressor and scaling it to fit and transform. RandomForestRegressor is a more appropriate measure of my specific analysis goal since it can:
a. capture non-linear relationships between features and the
target variable. The data has complex non-linear interactions and patterns
b. can handle categorical variables directly w/o needing one-hot encoding like linear regression
c. it's more flexible due to the ability to capture complex interactions w/ the data. 

I understood that random forests can someones have an issue with overfitting, but for now i'm going to pretend that it's not an issue - for the sake of convenience :)

**Findings**
If a house is closer to the coast, it is more likely to be more expensive. Check out the map:
