## Overview:
AlphabetSoup is not for profit organization, which helps business by funding them towards there goals. This project aims to create a deep nueral net model that is capable of predicting whether applicants will be successful if funded by Alphabet Soup. The model should have target predictive accuracy higher than 75%.

Alphabet Soup’s business team, has provided a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization, such as the following:

      EIN and NAME—Identification columns
      APPLICATION_TYPE—Alphabet Soup application type
      AFFILIATION—Affiliated sector of industry
      CLASSIFICATION—Government organization classification
      USE_CASE—Use case for funding
      ORGANIZATION—Organization type
      STATUS—Active status
      INCOME_AMT—Income classification
      SPECIAL_CONSIDERATIONS—Special consideration for application
      ASK_AMT—Funding amount requested
      IS_SUCCESSFUL—Was the money used effectively

## Results:

### 1. Data Preprocessing:

What variable(s) are considered the target(s) for the model?
Column IS_SUCCESSFUL— 'Was the money used effectively' is considred as target for the model.

What variable(s) are considered to be the features for the model?
All other columns except IS_SUCCESSFUL, EIN, and NAME.

What variable(s) are neither targets nor features, and should be removed from the input data?
EIN, and NAME columns can be removed as they add no value to model.

### 2. Compiling, Training, and Evaluating the Model:

The model had one input, two hidden layers, and one outer layer. First hidden layer has 8 neurons, and the second hidden layer has 6 neurons. "relu" activation function is used for hidden layers, and "sigmoid" is used for output layer.

![](https://github.com/div1085/Neural_Network_Charity_Analysis/blob/abf46d25c4be43c81e224b432f8ba6da77965d03/Resources/nn_model.png)

Model performance: Model returned accracy score of 72%, below then the desired result of 75%.

![](https://github.com/div1085/Neural_Network_Charity_Analysis/blob/abf46d25c4be43c81e224b432f8ba6da77965d03/Resources/acc_score.png)

Steps taken to optimize the model:

1. Running model with less features, and more neurons in model, and dataset with higher binning for application and classification column.

**Results:**

![](https://github.com/div1085/Neural_Network_Charity_Analysis/blob/7292f60edad03e3957ed3f9e71c8ed43395b0cb7/Resources/md1.png)

2.Running model with 3 hidden layers and epoch=30

**Results:**

![](https://github.com/div1085/Neural_Network_Charity_Analysis/blob/7292f60edad03e3957ed3f9e71c8ed43395b0cb7/Resources/md2.png)

3. Running model with activation function on hidden layers to changed "tanh" and output layer changed to "sigmoid"

**Results:**

![](https://github.com/div1085/Neural_Network_Charity_Analysis/blob/7292f60edad03e3957ed3f9e71c8ed43395b0cb7/Resources/md3.png)

## Summary:

The initial model returned accuracy of 72% whereas, models which were optimized return much lower accuracy within range of 60-64%. Thus, the initial model should be trained with expanded dataset to review the performance, as neural networks fares better when more data is available.
