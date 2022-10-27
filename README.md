# Neural_Network_Charity_Analysis
## Overview of the Analysis

Using Machine Learning and Neural Networks, we used the features in the dataset to create a binary classifier that would help in predicting which applicants had a higher chance of success funded by the Alphabet Soup charity. For this analysis we had a dataset containing various measures on 34,000 organizations that have been funded by Alphabet Soup. In order to achieve the desired outcome, we perfomed following tasks:

- Preprocessing the data for the neural network
- Compile, Train and Evaluate the Model
- Optimizing the model

# Results
## Data Preprocessing
Target Variable:   IS_SUCCESSFUL 
Feature Variables: Every remaining column which is left after clean up with the exception of IS_SUCCESSFUL 
Dropped Variables: EIN, NAME 

## Compiling, Training and Evaluating the Model

Initial Neural network model had 2 hidden layers. First layer had 90 neurons, the second had 30 neurons. Both layers used the 'relu' function and transfer function / activation function used was 'sigmoid'

The model was not able to reach the target 75%. The accuracy for this model was only 65.5%.

![Pic1](https://github.com/fouadZiaa/Neural_Network_Charity_Analysis/blob/c1cc2f9200a593ab8386519a3cfd103e003670cc/Resources/Accuracy%20Initial%20Model%2065.png)

## Optimization Attempts

Several attempts were made to optimize the model for higher accuracy, however as it can be seen below that none of the attempts were successful. 

Attempt 1: Removing an additional feature 'USE_CASE'. Model accuracy went down to 53%.

![Pic2](https://github.com/fouadZiaa/Neural_Network_Charity_Analysis/blob/c1cc2f9200a593ab8386519a3cfd103e003670cc/Resources/Accuracy%20Optimization%20Attempt%201.png)


Attempt 2: Additional neurons were added to the hidden layers and additional hidden layers were added as well. The accuracy went down again to 47%.

![Pic 3](https://github.com/fouadZiaa/Neural_Network_Charity_Analysis/blob/c1cc2f9200a593ab8386519a3cfd103e003670cc/Resources/Accuracy%20Optimization%20Attempt%202.png)


Attempt 3: Activation function of output layer was changed from "sigmoid" to "tanh." The accuracy of the model went down even more to 50%.

![Pic 4](https://github.com/fouadZiaa/Neural_Network_Charity_Analysis/blob/c1cc2f9200a593ab8386519a3cfd103e003670cc/Resources/Accuracy%20Optimization%20Attempt%203.png)


# Summary
The model ended up with the accuracy score of 50% after optimization. The initial neural network had a accuracy score of 69%. This loss in accuracy can be explained from the fact that the model overfitted. Furthermore, we could further also optimize our neural network by removing more features or simply adding more data to the dataset to increase accuracy. Since our accuracy score was not particularly up to the standard with neural networks, we could have used the Random Forest classifiers. This is because random forest is a robust and accurate model due to their sufficient number of estimators and tree depth. Also the random forest models have a faster performance than neural networks and could have avoided the data from being overfitted.
