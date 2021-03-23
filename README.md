# Neural Network Charity Analysis
Determining where to donate the most impactful charitable gift
---

## Overview of the analysis 
Looking at a history of funding requests from Alphabet Soup, we should be able to predict whether future applicants will be successful.
To do this, features are ranked, sorting occurs within the category and a pattern of features should become evident.

----

## Results
Using bulleted lists and images to support your answers, address the following questions.

### Data Preprocessing
- What variable(s) are considered the target(s) for your model? IS_SUCCESSFUL
- What variable(s) are considered to be the features for your model? APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, ASK_AMT
- What variable(s) are neither targets nor features, and should be removed from the input data? "SPECIAL_CONSIDERATIONS" shoould be removed; it's more of a comment line that doesn't indicate whether the consider is positive or negative

### Compiling, Training, and Evaluating the Model
- How many neurons, layers, and activation functions did you select for your neural network model, and why? After several attempts to change neurons and layers, it didn't seem to increase the accuracy. Therefore the original layers and functions were retained.
- Were you able to achieve the target model performance? 
- What steps did you take to try and increase model performance? I tried removing features, adding a layer, increasing neurons on hidden layers, and altering an activation level.

----

## Summary
Overall, I found a learning model that achieved 69% accuracy by removing SPECIAL_CONSIDERATIONS, which isn't enough to make good predictions. Typically, you want a model that achieves at least 90%.

*AlphabetSoupCharity Accuracy Visual*

![AlphabetSoupCharity](https://github.com/emilymcdaniel/Neural_Network_Charity_Analysis/blob/main/Standard.PNG?raw=true)

*AlphabetSoupCharity_Optimization Accuracy Visual*

![AlphabetSoupCharity_Optimization](https://github.com/emilymcdaniel/Neural_Network_Charity_Analysis/blob/main/Optimization.PNG?raw=true)

I would recommend using the random forest model, as modifying single datapoints seemed to minimally impact accuracy. Random Forest would allow these seemingly minimal factors interact and readily find trends among features.

