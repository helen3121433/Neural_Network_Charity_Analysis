# Neural_Network_Charity_Analysis

## Overview of the analysis: Explain the purpose of this analysis.

- Used features in the dataset from Alphabet Soup to help Beks create a binary clasifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup. Dataset includeds more than 34,000 organizations that have recieved funding from Alphabet Soup over the years.

Columns: 
- EIN and NAME—Identification columns
- APPLICATION_TYPE—Alphabet Soup application type
- AFFILIATION—Affiliated sector of industry
- CLASSIFICATION—Government organization classification
- USE_CASE—Use case for funding
- ORGANIZATION—Organization type
- STATUS—Active status
- INCOME_AMT—Income classification
- SPECIAL_CONSIDERATIONS—Special consideration for application
- ASK_AMT—Funding amount requested
- IS_SUCCESSFUL—Was the money used effectively

## Results: Using bulleted lists and images to support your answers, address the following questions.

### Data Preprocessing
What variable(s) are considered the target(s) for your model?
- The target is "IS_SUCCESSFUL" - was the money used effectively

What variable(s) are considered to be the features for your model?
- Features are all encoded variables(encoded from object variables), and int64 variables

What variable(s) are neither targets nor features, and should be removed from the input data?
- Removed the catergorical variable lists that dtype = objects. Objects variable are neither targets nore features.

### Compiling, Training, and Evaluating the Model
- I tried couple different ways such as change neurons values, add hidden layers and change activation funcions.I first increaseed the neurons to 100 units for layer one, but not much change. 
![](https://github.com/helen3121433/Neural_Network_Charity_Analysis/blob/main/Resources/Neuron_changed.PNG)
- Then I tried add a hidden layers with neuron units = 10, and used relu as activation funcions. The accuracy looks the same.
![](https://github.com/helen3121433/Neural_Network_Charity_Analysis/blob/main/Resources/Hidden_layer_added.PNG)

- Next I changed the activation function of the hidden layers, looks like we have a bit improvement there.
![](https://github.com/helen3121433/Neural_Network_Charity_Analysis/blob/main/Resources/Activation_changed.PNG)

- At last try, I set first hidden layers with units = 6 and activation funcions as "tanh". Set second hidden layer with units = 6 andactivation functions as "relu". Set third hidden layer with units = 3 and activation functions as "relu". Accuracy and loss has bit improve.
![](https://github.com/helen3121433/Neural_Network_Charity_Analysis/blob/main/Resources/All_three_changed.PNG)


## Summary: Summarize the overall results of the deep learning model. 
- Unfortunely, I failed to increase the predictive accuarcy over 75%. we could try other model such as Balanced Random Forest Classifer, and Easy Ensemble Classifier and see if we can get a better result.