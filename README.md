# Alphabet Soup Neural Network Analysis

## Overview of project
Using nueral network machine learning, we were asked to analyse cryptocurrencies for an investment bank who is looking to offer a new
cryptocurrency investment portfolio for its customers.

### Resources
* Data Sources: 'crypto_data.csv' from CryptoCompare
* Software: Jupyter Notebook, Python, machine learning algorithms, hvplot, StandardScaler, MinMaxScaler, K-Means, PCA


## GitHub has disabled LFS for my account due to the fact that I have exceeded my data storage limit. 
### I have added "*.csv" to my .gitignore file, so my datafiles are not uploaded to my GitHub page.


## Results
Initial results using the given parameters of:
hidden_nodes_layer1 = 80
hidden_nodes_layer2 = 30
I selected "relu for the first hidden layer, and "relu" for the second hidden layer.  Output layer = "sigmoid".
Ran the inital model for 50 epochs.
![Initial Results](https://github.com/AndyHerron/Cryptocurrencies/blob/main/screenshots/elbow_curve.png)

Optimization attempt A results using the given parameters of:
hidden_nodes_layer1 = 40
hidden_nodes_layer2 = 20
I selected "LeakyReLU" for the first hidden layer, and "LeakyReLU" for the second hidden layer.  Output layer = "sigmoid".
Ran the inital model for 15 epochs.
![Optimization_1](https://github.com/AndyHerron/Cryptocurrencies/blob/main/screenshots/3D_scatter_with_clusters.png)

HVPLOT table
![hvplot_table](https://github.com/AndyHerron/Cryptocurrencies/blob/main/screenshots/hvplot_table.png)

2D Scaled Data Plot
![2D Scaled Data plot](https://github.com/AndyHerron/Cryptocurrencies/blob/main/screenshots/Scaled_data_plot.png)


