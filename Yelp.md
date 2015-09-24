* Read yelp.csv into a DataFrame.

`import pandas as pd`
`yelp=pd.read_table('yelp.csv', sep",")`

* Explore the relationship between each of the vote types (cool/useful/funny) and the number of stars.

`yelp.describe()`

There was more hat I wanted to do here. Questions I had were: How many instances occur where all three votes exist at least once? and How more likely was a rating to gt a particular vote based on stars?

* Define cool/useful/funny as the features, and stars as the response.

So here I began by dropping all values that weren't numeric:
`yelp.drop(['business_id', 'date', 'user_id', etc...], axis=1, inplace=True)`
And then I turned my stars column into a string
`yelp.stars.astype('string')`

I'm not sure if I was going in the right direction here. I was a bit lost from here. Will be asking questions.

* Fit a linear regression model and interpret the coefficients. Do the coefficients make intuitive sense to you? Explore the Yelp website to see if you detect similar trends.

* Evaluate the model by splitting it into training and testing sets and computing the RMSE. Does the RMSE make intuitive sense to you?

* Try removing some of the features and see if the RMSE improves.
