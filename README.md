# Title

**Authors**: Daniel Arthur, Sumedh Bhardwaj, Emiko Naomasa



## Overview
The objectives of this project are twofold. (1) Create a prediction model that will help our stakeholder (Zillow’s) to predict future home prices. (2) provide an inferential analysis to be fed into on our prediction model.  

## Business Understanding 

The stakeholders are Zillow. They are the most used online real estate site. The current model they use to evaluate the price of homes has a median error rate of 1.9%. However, this error rate increases to 2.3% in Washington. This results in 9.8% of houses being at or above a 10% error rate. This can equate to 10s of thousands of dollars on an individual scale and millions at a company level. We are creating a model to reduce the errors in the Washington area. Having a better model will encourage use of the site and increase revenue.

## Data
We use a housing sales dataset from King County, which includes Seattle. The dataset includes the prices of houses sold between May 2014 and May 2015.
We cleaned the following 12 variables from the dataset, and we evaluated the outliers, the missed entries of data, and other issues in each variable.\
•	**id:** Unique identification (ID) for each sold house \
•	**date:** Date the house was sold \
•	**price:** Price of the house sold \
•	**bedrooms:** Number of bedrooms \
•	**bathrooms:** Number of bathrooms \
•	**sqft_living:** Square footage of the house’s interior living space\
•	**sqft_lot:** Square footage of the land space\
•	**floors:** Number of floors\
•	**waterfront:** A dummy variable for whether the house is on a waterfront \
•	**condition:** An index from 1 to 5 on the overall condition of the house. Related to maintenance of house. \
•	**grade:** An index from 1 to 13 on the grade of the house, where 1 means poor construction and design, and 13 means high quality. It is related to the construction and design of the house. \
•	**vintage:** House vintage (years) = the year the house was sold - the year the house was built
   
## Modeling

First, we conducted inferential analysis to find the key determinants with which to predict the housing market prices. For this analysis, we used a linear regression model to determine the relationships between housing prices and the other housing features. Using the findings from the inferential analysis, we ran a price-prediction model using a linear regression model.
 
  
## Regression Results

  ### Inferential Analysis

   We used a linear regression model for the inferential analysis. We started with a single linear regression of price and size of living area and then kept adding other housing features one by one from among the features highly related with price. We used R-squared score as the main measure with which to select a model. We kept adding features until the R-squared score stop increasing with additional features.

   Following the above rule, we selected a model that included a size of living space, a dummy variable for above-average house grade, number of floors, and a dummy for waterfront property. 


  ### Predictive Model: Model to support Zillow's price prediction for a new house
  
   Using infomation gained from the inferential models, we made a several predictive models. developed the price-prediction model using the results of the inferential analysis. The first model was a dummy regressor, which is equal to a random selection model. Then, we included all of the features and tweaked the variables using a machine-learning algorithm and insights from the inferential analysis. 
    
   However the models we made performed less well than the model currently in use by our client. By running the predictive models with differenct data points selected by through our inferential modeling process, we were able to improve the accuracy of our model. We outperformed our baseline model, but our mrse is nearly 40% of our target.
  
  
## Conclusion
  
   In conclusion we recomend that Zillow continues to use their current model. The model they currenly use has an error rate of 2.3%. Our model had an error rate near 40%. The lack of homoskedasity and linear correlation suggests that linear regression models are not a good fit for this problem. Further infomation would help as well. Getting data about income in the area, population trends, and a myraid of other factors would reduce model error. 
   
  
  
## For More Information 
Please review our full analysis in our Jupyter Notebook or our presentation.
For any additional questions, please contact: [Daniel Arthur](https://www.linkedin.com/in/daniel-arthur-472b59224/), [Sumedh Bhardwaj](https://www.linkedin.com/in/sumedh-bhardwaj-932767202/), [Emiko Naomasa](https://www.linkedin.com/in/emiko-n-58782158/) 

  
## Repository Structure

```
├── README.md                           <- The top-level README for reviewers of this project
├── title.ipynb                         <- Concise summary of the project with all data science steps
├── Project 2.pdf                       <- PDF version of project presentation
├── Data                                <- Both sourced externally and generated from code, includes exploratory notebooks
└── Images                              <- Both sourced externally and generated from code
```  
Note: Large or sensitive files are listed in .gitignore and not pushed to GitHub.

  
  
  
