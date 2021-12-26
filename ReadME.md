## Overview of the analysis
- Usage of pandas to create a dataframe of values to the perform Principle Component Analysis of the dataset. 

## Resources
- Program language: crytocurrancy datafile,Python3, pandas, Jupyter notebook  <br> 
 


## Results 
##### Deliverable 1 
All cryptocurrencies that are not being traded are removed  <br>
![Figure 1](https://github.com/davidhyongae2/Crypto_currancy/blob/main/Figure1.png) <br>
The IsTrading column is dropped  <br>
![Figure 2](https://github.com/davidhyongae2/Crypto_currancy/blob/main/Figure2.png) <br>
All the rows that have at least one null value are removed  <br>
![Figure 3](https://github.com/davidhyongae2/Crypto_currancy/blob/main/Figure3.png) <br>
All the rows that do not have coins being mined are removed <br>
![Figure 4](https://github.com/davidhyongae2/Crypto_currancy/blob/main/Figure4.png) <br>
The CoinName column is dropped  <br> 
![Figure 5](https://github.com/davidhyongae2/Crypto_currancy/blob/main/Figure5a.png) <br>

A new DataFrame is created that stores all cryptocurrency names from the CoinName column and retains the index from the crypto_df DataFrame  <br> 
![Figure 6](https://github.com/davidhyongae2/Crypto_currancy/blob/main/Figure6.png) <br>

The get_dummies() method is used to create variables for the text features, which are then stored in a new DataFrame, X  <br>
![Figure 7](https://github.com/davidhyongae2/Crypto_currancy/blob/main/Figure7.png) <br>

The features from the X DataFrame have been standardized using the StandardScaler fit_transform() function  <br>
![Figure 8](https://github.com/davidhyongae2/Crypto_currancy/blob/main/Figure8.png) <br>


##### Deliverable 2 Requirements

The PCA algorithm reduces the dimensions of the X DataFrame down to three principal components  <br> 
![Figure 9](https://github.com/davidhyongae2/Crypto_currancy/blob/main/Figure9b.png) <br>


The pcs_df DataFrame is created and has the following three columns, PC 1, PC 2, and PC 3, and has the index from the crypto_df DataFrame  <br> 
![Figure 10](https://github.com/davidhyongae2/Crypto_currancy/blob/main/Figure10.png) <br>

##### Deliverable 3 Requirements


The K-means algorithm is used to cluster the cryptocurrencies using the PCA data, where the following steps have been completed:
An elbow curve is created using hvPlot to find the best value for K <br>
![Figure 11](https://github.com/davidhyongae2/Crypto_currancy/blob/main/Figure11.png) <br>

Predictions are made on the K clusters of the cryptocurrencies’ data  <br>
![Figure 12](https://github.com/davidhyongae2/Crypto_currancy/blob/main/Figure12.png) <br>

A new DataFrame is created with the same index as the crypto_df DataFrame and has the following columns: Algorithm, ProofType, TotalCoinsMined, TotalCoinSupply, PC 1, PC 2, PC 3, CoinName, and Class  <br>
![Figure 13](https://github.com/davidhyongae2/Crypto_currancy/blob/main/Figure13.png) <br>

##### Deliverable 4 Requirements


The clusters are plotted using a 3D scatter plot, and each data point shows the CoinName and Algorithm on hover  <br> 

![Figure 14](https://github.com/davidhyongae2/Crypto_currancy/blob/main/Figure14.png) <br>

A table with tradable cryptocurrencies is created using the hvplot.table() function <br> 

![Figure 15](https://github.com/davidhyongae2/Crypto_currancy/blob/main/Figure15.png) <br>
The total number of tradable cryptocurrencies is printed  <br>
![Figure 16](https://github.com/davidhyongae2/Crypto_currancy/blob/main/Figure16.png) <br>

A DataFrame is created that contains the clustered_df DataFrame index, the scaled data, and the CoinName and Class columns <br> 
![Figure 17](https://github.com/davidhyongae2/Crypto_currancy/blob/main/Figure17.png) <br>

A hvplot scatter plot is created where the X-axis is "TotalCoinsMined", the Y-axis is "TotalCoinSupply", the data is ordered by "Class", and it shows the CoinName when you hover over the data point  <br> 
![Figure 18](https://github.com/davidhyongae2/Crypto_currancy/blob/main/Figure18a.png) <br>
