# Deep-Learning-Challenge Report
## Ryan Kincheloe


## Overview
This analysis is an attempt to gain a deeper understanding of which funding appicants, for Alphabet Soup, have the best chances for success.


## Results

* Data Preprocessing
    * The target variable for this model is the  "IS_SUCCESSFUL" column which is a binary measure of whether an Alphabet Sout funded venture was successful.
    * The features in this model include:
        * APPLICATION_TYPE 
        * AFFILIATION
        * CLASSIFICATION
        * USE_CASE
        * ORGANIZATION
        * STATUS 
        * INCOME_AMT 
        * SPECIAL_CONSIDERATIONS
        * ASK_AMOUNT
    * The variables that should be removed as they are neither targets nor features are the EIN number and the name of the Organization.

* Compiling, Training and Evaluating the Model
    * To create the final version of the model, I used three total layers, two hidden and one output. The first and second layers have 16 neurons each and my output layer has 1 neuron. I settled on these in an attempt to construct a simple model and not over clutter the network.
    * I did not meet the performance target of 75% accuracy, my model reached 0.730 accuracy with a 0.549 loss.
    * To increase model performance I took the following steps
        * Re-process the data to ensure critical information was correctly passed to the model (i.e. transformed ask amount into a float from a string)
        * Adjusted the learning rate
        * Introduced a callback function to help the model adjust if it was getting stuck
        * Experimented with activation functions, neurons, and activation layers
        * experimented with epochs
        * added and removed other regularizations

## Summary

The deep learning model constructed utilizes two hidden sequential layers, each having 16 neurons, and an output layer with a sigmoid activation function. The tanh activation function was used for the hidden layers. The training data has 804 samples, and the model was trained over 100 epochs. The final training accuracy achieved was approximately 73.9%. This indicates that the model generalizes well on unseen data and isn't overfitting.

While the deep learning model performs well there's always room for improvement. One recommendation could be to try a Random Forest classifier; which can handle a mix of categorical and numerical data and aggregate the decisions from multiple decision trees to make a final decision. This can lead to more accurate and robust results.