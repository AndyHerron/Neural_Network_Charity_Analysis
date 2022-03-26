# Alphabet Soup Neural Network Analysis

## Overview of project
Using neural network machine learning, we were asked to analyse cryptocurrencies for an investment bank who is looking to offer a new
cryptocurrency investment portfolio for its customers.

### Resources
* Data Sources: 'charity_data.csv'
* Software: Jupyter Notebook, Python, Keras models


## GitHub has disabled LFS for my account due to the fact that I have exceeded my data storage limit. 
### I have added "*.csv" to my .gitignore file, so my datafiles are not uploaded to my GitHub page.


## Results

- IS_SUCCESSFUL is the target variable for our model
- Features of the model are: APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT  
- The variables EIN and NAME are neither features nor targets and were removed from the data.

Initial results using the given parameters of:
*hidden_nodes_layer1 = 80*
*hidden_nodes_layer2 = 30*
I selected "relu for the first hidden layer, and "relu" for the second hidden layer.  Output layer = "sigmoid".
Ran the inital model for **50** epochs.
![Initial Results](https://github.com/AndyHerron/Neural_Network_Charity_Analysis/blob/main/screenshots/Initial_Results.png)

**First changes:**
I tried to remove noisy variables.  I removed "AFFILIATION" and "ORGANIZATION" but the results only got worse.  The accuracy dropped to around 62%.
That's clearly not helping, so I put those variables back into the dataset.
Running the model took a long time.  50 epochs seemed like it was more than I needed, so I looked back through the output.
The model did not seem to be improving in accuracy after about 15 epochs, so I wanted to see what results I would get with fewer nodes and fewer epochs.
I kept the activations the same and tried it using 40 nodes on the first layer and 20 on the second layer, over 15 epochs.  The results were pretty close.
![Optimization_1](https://github.com/AndyHerron/Neural_Network_Charity_Analysis/blob/main/screenshots/Optimization_1.png)

Optimization attempt A results using the given parameters of:
*hidden_nodes_layer1 = 40*
*hidden_nodes_layer2 = 20*
I selected "LeakyReLU" for the first hidden layer, and "LeakyReLU" for the second hidden layer.  Output layer = "sigmoid".
Ran the inital model for **15** epochs.
![Optimization_A](https://github.com/AndyHerron/Neural_Network_Charity_Analysis/blob/main/screenshots/Optimization_A.png)

Optimization attempt B results using the given parameters of:
*hidden_nodes_layer1 = 40*
*hidden_nodes_layer2 = 20*
*hidden_nodes_layer3 = 20*
I selected "ReLU" for the first hidden layer, "LeakyReLU" for the second hidden layer, and "sigmoid" for the third hidden layer.  
Output layer = "sigmoid".  Ran the inital model for **15** epochs.
![Optimization_B](https://github.com/AndyHerron/Neural_Network_Charity_Analysis/blob/main/screenshots/Optimization_B.png)

Optimization attempt C results using the given parameters of:
*hidden_nodes_layer1 = 80*
*hidden_nodes_layer2 = 30*
*hidden_nodes_layer3 = 20*
I selected "ReLU" for the first hidden layer, "LeakyReLU" for the second hidden layer, and "tanh" for the third hidden layer.  
Output layer = "sigmoid".  Ran the inital model for **15** epochs.
![Optimization_C](https://github.com/AndyHerron/Neural_Network_Charity_Analysis/blob/main/screenshots/Optimization_C.png)

## Summary
I initially chose 80 and 30 neurons because that's what was shown in the provided starter code.  That seemed excessive and took a long time to run.
In my optimization attempts I significantly dropped the number of neurons, and the results stayed about the same. I was able to only very slightly improve
on the initial results, and could not achieve an accuracy of over 75%.  I tried dropping features, changing activation methods, played with the number of
neurons on each layer, and added a third layer.  Unfortunately the accuracy did not improve, and I do not know what else to recommend trying.  I can suggest 
several things that will make it worse, but that's not the goal. :joy:

