# deep-learning-challenge
Module 21 Challenge


## Neural Network Model 

The purpose of this model is to assist the nonprofit group Alphabet Soup in predicting whether or not applicants will be successful if receiving funding through them.


Data Preprocessing:

    The target variable used in this model is:
    * IS_SUCCESSFUL—Was the money used effectively


    The feature variables used in this model are:
    * AFFILIATION—Affiliated sector of industry
    * CLASSIFICATION—Government organization classification
    * USE_CASE—Use case for funding
    * ORGANIZATION—Organization type
    * STATUS—Active status
    * INCOME_AMT—Income classification
    * SPECIAL_CONSIDERATIONS—Special considerations for application
    * ASK_AMT—Funding amount requested

    The following variables were removed and not used in the model:
    * EIN—Identification number
    * NAME—Identification name


The final model consists of 4 Layers:
* The first hidden layer contains 150 neurons, with a __ activation function
* The second hidden layer contains 100 neurons, with a __ activation function
* The third hidden layer contains 50 neurons, with a __ activation function
* The output layer contains 1 neuron, with a Sigmoid activation function - for binary classification.


I was not able to achieve the target model accuracy of 75%. 

The accuracy of the 6 models I ran are as follows:
* Initial model: 72.7%
* 1st Optimization model: 72.7%
* 2nd Optimization model: 72.6%
* 3rd Optimization model: 72.7%
* 4th Optimization model: 72.9%
* 5th Optimization model: 72.6%



My First attempt to optimize the initial model entailed:
* Reducing the number of bins in the APPLICATION_TYPE variable
* Increasing the number of neurons in the hidden layers

My Second attempt to optimize the initial model entailed:
* Increasing the number of neurons in the hidden layers
* Changed the activation function of all hidden layers to Tanh

My Third attempt to optimize the initial model entailed:
* The addition of a third Hidden Layer
* Increasing the number of neurons in all hidden layers
* Changed the activation function of all hidden layers to Tanh

My Fourth attempt to optimize the initial model entailed:
* The addition of a third Hidden Layer
* Changed the activation function of first hidden layers to Tanh (2nd and 3rd are relu)
* Increasing the number of neurons in all hidden layers
* Increase Epochs to 250

My Fifth attempt to optimize the initial model entailed:
* The addition of a third Hidden Layer
* Increasing the number of neurons in all hidden layers
* Changing the activation function of the 2nd hidden layer to Tanh (1st and 3rd are relu)
* Reducing the number of bins in the CLASSIFICATION Variable
* Increased the number of bins in the APPLICATION_TYPE variable


The final model does not reach the target goal of 75% accuracy. My recommendation would be to choose a random forest model and determine feature importance. This would give you a better idea of which variables are contributing to machine learning, and which are not as important.


Sources:

https://lightning.ai/docs/pytorch/stable/api/lightning.pytorch.callbacks.ModelCheckpoint.html \
    for ModelCheckpoint to save weigths.