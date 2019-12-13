# Read Me 
***

## Problem Statement
The zillow data analytics team has hired my consulting company to create a model to predict housing prices in Ames Iowa. I used Root MSE and R^2 as the metrics of evaluation. 
***


## Data Dictionary
https://www.kaggle.com/c/dsi-us-9-project-2-regression-challenge/data
***

## Methodology 
1. Data Cleaning 
    a. Convert column title and names to lower case, remove the spaces and replace them with underscores
    b. Identified the null values with scatterplots and scatterplots and depending on the thresholds they were eliminated 
    c. Dummy or dictionary the columns 
        i. I chose to dictionary the quality and condition variables and dummy the rest of the relevant columns 
2. Feature Selection/ Interaction 
    a. The first thing I did was look up which factors affected home price the most and tried to find variables within the dataset that corresponded to that search 
    b. I identified five different feature interaction potentials 
        i. Garage Combined: an aggregate of garage area and garage cars 
        ii. Deck and Porch: the multiplication of wood deck square footage and porch square footage 
        iii. Quality and Condition interactions for Basement, Garage, and Exterior
3. Power Transformation and Model Making 
    a. I transformed all of my training data in order to make it look more normal 
    b. I tested three models: linear regression, ridge, and lasso (though I will focus more on ridge and linear regression as my lasso scores were ridiculous) 

## Outlier removal: 
I removed outliers from the following columns: 
    1. Ground Living Area 
    2. First Floor SF 
    3. Basement SF 
    4. Masonry Veneer Area 
    5. 2nd Floor SF 
    6. Garage Combined Score 
    7. Lot Area 
    8. Total Basement SF 
    9. Wood Deck Sf 
    10. Sale price 
    11. Null Values 

***
## Feature Description 
The features I used were the top numeric variables that correlated highly with sale price up to a threshold of .3, as anything below is not worth inputting into the model. 

## Business Conclusions/ Recommendations 
Ridge was the best model by a small margin over linear regression in kaggle but in the notebook, linear regression edged it out by a thousand. Lasso was not considered. 

### Takeaways 
   1. Location obviously was the largest coeficient for sale price 
   2. Functionality is a huge factor when it comes to sale price 
   3. The most negative features were poor home functionality and a lack of basic amenities such as lack of a sewer system. 

### Recommendations 
   1. More data is needed to create a better model, each city is affected differently by different features
   2. A better location metric is needed other than neighborhoods. Maybe street, zipcode, or address might be better 
   3. Some of the features are generalizable but, location data is not. 



