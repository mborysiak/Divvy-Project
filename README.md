# Classifying Bike Share Trip Distance

## Summary
This project aims to predict the distance a user will ride a bike when using the Chicago-based Divvy Bike share program. Divvy makes trip datasets publicly available on their website: https://www.divvybikes.com/system-data. Using this data, I analyzed various feature transformations and machine learning algorithms in order to predict whether or not a user will ride less than or greater than 2 km for each trip, using only information that would be known at the beginning of the ride.

## Techniques Used
I relied on the standard Python stack (pandas, numpy, matplotlib, sklearn), as well as a few additional API's such as Google Maps and Weather Underground in order to generate my predictions. The machine learning models I explored include logistic regression, XGBoost, LightGBM, and Random Forest, along with K-means clustering. This notebook makes use of the 2016 year-long data. For validation and testing on the 2017 half-year data, see the additional Model Evaluation notebook.

## Results
In this notebook, I explored various methods for cleaning and modeling the data, focusing on feature reduction and machine learning algorithm selection. When I used one hot encoding for the departure station feature, it resulted in over 550 additional features. Using clustering and logistic weights, I reduced this information to 100 features with minimal loss in prediction accuracy.

My resulting models obtained a 5-fold cross-validated accuracy of 0.68 and 0.67 for out-of-sample 2016 data with the Random Forest and LightGBM algorithms respectively. Ensemble modeling and their performance on validation and test data from 2017 can be found in the Model Evaluation notebook.
