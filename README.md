# Neural_Network_Charity_Analysis

## Overview of the analysis

A neural network was used to try to predict whether applicants looking for funding from a foundation, Alphabet Soup, will be successful or not if funded. This will help Alphabet Soup best allocate their investments. 

## Results
### Data Preprocessing 

The **target variable** is the `IS_SUCCESSFUL` column, which tells us which applicants that received an investment from Alphabet Soup were successful. 

The **feature variables** were the following: 
![Features of Model](/FeatureVariables.png)

The identifier columns, `EIN` and `NAME`, were dropped because they are considered neither targets or features of the model. 


### Compiling, Training, and Evaluating the Model

How many neurons, layers, and activation functions did you select for your neural network model, and why?

The model parameters I selected to perform the best were:
- two layers
- 20 nodes in first layer, with Relu activation function
- 10 nodes in second layer, with Relu activation function
- Sigmoid activation function for output layer
- 120 epochs

I was not able to achieve a model target performance of 75%. The best I could do was 68% with the model parameters above. 

### Optimization Tests

I tried a few different ways to optimize the nueral model, but all failed to improve performance or hit the target performance. 

1. Increasing to 20 nodes in layer 1, 10 nodes in layer 2, and 120 epochs

[20 nodes, 10 nodes, 120 epochs](/Optimization2_20nodes%2B10nodes.png)

2. Adding three layers instead of two layers
_node values were 20, 10, and 5 for the consecutive layers_

[Three layers](/Opt4_ThreeLayers20_10_5.png)

3. Increasing to 25 nodes in layer 1 and 12 nodes in layer 2

[More nodes](/Opt5_inputs_25_12.png)

4. Different activation functions

I playeda round with a combination of Sigmoid, Relu, and Tanh activation functions for the input and output layers, and nothing worked better for me than sticking with the Relu activation function for the input layers and using the Sigmoid function for the output layers. All other combos I tried resulted in an accuracy score of around 50%. 


## Summary

Overall, the results of this model were not fantastic. I'm sure there is a way to acheive 75% accuracy, but I could not find the right combination of parameters to acheive that result unfortunately. 

I would next try a Logistic Regression or Random Forest Classifier model to see if they perform better in classifying the likelihood that an Alphabet Soup investment will be successful. The dataset is of medium size (34k rows) and isn't super complex, so hopefully one of those models would have enough data to find patterns in the feature variables to make more accurate predictions.

