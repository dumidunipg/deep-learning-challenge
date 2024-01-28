# Report on the Neural Network Model

## Overview 
The purpose of this analysis is to evaluate how well the binary classifier can predict whether applicants will be successful if funded by the nonprofit foundation Alphabet Soup.

## Results:
* Data Preprocessing
    * What variable(s) are the target(s) for your model?
        * The target variable is IS_SUCCESSFUL
    * What variable(s) are the features for your model?
        * The features are APPLICATION_TYPE,AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT
    * What variable(s) should be removed from the input data because they are neither targets nor features?
        * EIN and NAME were removed from the input data because they are neither targets nor features.
* Compiling, Training, and Evaluating the Model
    * How many neurons, layers, and activation functions did you select for your neural network model, and why?
        * Initial Model
            * There were 3 layers comprising of 10, 5, and 1 neuron(s). The first and second hidden layer uses the ReLU activation function while the output layer uses the sigmoid activation function. I wanted to start off with a small amount of layers and neurons to see if increasing it would make the accuracy of the model higher later on. 
            * Accuracy of the model: .7289
        * Optimization. Model 1
            * The bins for application type and classification were increased
            * There were 100 epochs in the training regimen
            * There were 4 layers comprising of 80, 30, 60, and 1 neuron(s). The first, second and third hidden layers use the ReLU activation function while the output layer uses the sigmoid activation function. I increased the neurons and hidden layers to see if the accuracy of the model increased.
            * Accuracy of the model: .7282
        * Optimization Model 2
            * The bins for application type and classification remained the same as optimization attempt 1.
            * There were 1000 epochs in the training regimen
            * There were 5 layers comprising of 90, 80, 80,  60, and 1 neuron(s). The first, second, third, and fourth hidden layers use the ReLU activation function while the output layer uses the sigmoid activation function. I increased the neurons and hidden layers to see if the accuracy of the model increased.
            * Accuracy of the model: .7266
        * Optimization Model 3
            * The bins for application type and classification increased and the special consideration column was dropped. 
            * There were 100 epochs in the training regimen
            * There were 4 layers comprising of 5, 5, 5, and 1 neuron(s). The first, second and third hidden layers use the ReLU activation function while the output layer uses the sigmoid activation function. I decreased the neurons to see if adding more bins, removing a feature and decreasing neurons would increase the accuracy of the model. 
            * Accuracy of the model: .7291
    * Were you able to achieve the target model performance?
        * I was not able to achieve the target model performance, however my optimization attempt 3 led to the highest accuracy of the model thus far at .7291.
    * What steps did you take in your attempts to increase model performance?
        * In optimization model 1, the bins for application type and classification were increased, and the number of layers and neurons were increased. In optimization model 2 the bins for application type and classification remained the same as optimization attempt 1, but the layers and neurons were increased as well as the number of epochs used in the training regimen. In optimization model 3, the bins for application type and classification increased and the special consideration column was dropped. The number of neurons were decreased within 4 layers.

## Summary
Overall, the results indicate that the model could be optimized to perform better so that it reaches a target predictive accuracy of 75%.  The resulting models were at about 72% accuracy. Perhaps a different model that isn’t overly complex and with a different activation function could enhance the performance of the model. A simpler model with less neurons and a different activation function would be used to avoid overfitting issues which can lead to a decrease inaccuracy of the model. 



