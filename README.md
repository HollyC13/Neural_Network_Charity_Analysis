# Neural_Network_Charity_Analysis
Module_19

## Overview
Using deep learning neural-network models on a dataset of more than 34,000 charitable organizations that have received funding over the years, create a binary classifier that is capable of predicting whether applicants will be successful if funded.


## Results
### Data Preprocessing
- What variable(s) are considered the target(s) for your model?</p>
The IS_SUCCESSFUL column is our target, as it indicates the outcome for organizations who received funding in the past.

- What variable(s) are considered to be the features for your model?</p>
Feature columns are APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, and ASK_AMT.

- What variable(s) are neither targets nor features, and should be removed from the input data?</p>
The EIN and NAME columns contain identification information that is not needed and have been removed from the dataset.


### Compiling, Training, and Evaluating the Model
- How many neurons, layers, and activation functions did you select for your neural network model, and why?</p>
The initial model included two hidden layers, the first with 30 neurons and the second with 15 neurons.  30 neurons were chosen based on the idea of using roughly 3 times the number of input values, two layers were included to create a multi-layer Perceptron, and ReLU was chosen for speed of processing.
In an attempt to reach the 75% accuracy threshold, additional models were created using fewer inputs, with additional neurons, an additional hidden layer, and using tanh rather than ReLu for activation.  The most accurate model was the one using fewer inputs with an accuracy score of 73.11%.

- Were you able to achieve the target model performance?</p>
No, none of the models achieved the target model performance level of 75% accuracy.

- What steps did you take to try and increase model performance?</p>
1) Reduced noise by removing two additional columns, STATUS and SPECIAL_CONSIDERATIONS, from the dataset

<img src="https://github.com/HollyC13/Neural_Network_Charity_Analysis/blob/21706ee78aeb985edfb002d63c0dc01332145831/Resources/Images/Img_less_noise.png"> 
</p>

2) Added additional neurons to existing two hidden layers

<img src="https://github.com/HollyC13/Neural_Network_Charity_Analysis/blob/21706ee78aeb985edfb002d63c0dc01332145831/Resources/Images/Img_add_neurons.png"> 
</p>

3) Added an additional hidden layer to the model

<img src="https://github.com/HollyC13/Neural_Network_Charity_Analysis/blob/21706ee78aeb985edfb002d63c0dc01332145831/Resources/Images/Img_add_layer.png"> 
</p>

4) Changed the activation function for all hidden layers from ReLU to tanh
          
<img src="https://github.com/HollyC13/Neural_Network_Charity_Analysis/blob/21706ee78aeb985edfb002d63c0dc01332145831/Resources/Images/Img_change_functions.png"> 
</p>

## Summary
None of the deep-learning neural network models achieved the desired accuracy of 75%.  This is likely due to overfitting.  I recommend using machine learning models on this dataset, beginning with Random Forest algorithm.
