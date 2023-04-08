# Ch_19_Cryptocurrencies
Part 1: Preprocessing the Data for PCA / Part 2: Reducing Data Dimensions Using PCA / Part 3: Clustering Cryptocurrencies Using K-means / Part 4: Visualizing Cryptocurrencies Results

* Data Analysis of Cryptocurrencies

** Introduction:

In this report, we will be analyzing the cryptocurrency market data to create a classification system that can be used for a new investment portfolio for Accountability Accounting. We will be using unsupervised learning to group the cryptocurrencies and will be utilizing machine learning techniques such as PCA and K-means algorithm to process and cluster the data.

** Part 1: Preprocessing the Data for PCA

We started by importing the dataset from CryptoCompare into the Jupyter notebook as a Pandas DataFrame named crypto_df. Then, we removed the rows that have at least one null value, kept all the cryptocurrencies that are being traded and filtered the DataFrame so it only has rows where coins have been mined. Afterward, we removed the IsTrading column and CoinName column from the crypto_df DataFrame as it's not going to be used on the clustering algorithm.

Next, we used the get_dummies() method to create variables for the two text features, Algorithm and ProofType, and stored the resulting data in a new DataFrame named X. After that, we used the StandardScaler fit_transform() function to standardize the features from the X DataFrame.

** Part 2: Reducing Data Dimensions Using PCA

We applied PCA to reduce the dimensions to three principal components. We created a new DataFrame named pcs_df that includes the following columns, PC 1, PC 2, and PC 3, and used the index of the crypto_df DataFrame as the index.

** Part 3: Clustering Cryptocurrencies Using K-means

Using the pcs_df DataFrame, we created an elbow curve using hvPlot to find the best value for K. We found that the best value for K was 4. We then used the pcs_df DataFrame to run the K-means algorithm to make predictions of the K clusters for the cryptocurrencies’ data.

** Part 4: Visualizing Cryptocurrencies Results

We created a scatter plot to visualize the different clusters of cryptocurrencies based on the PCA algorithm. The scatter plot shows the relationship between PC1, PC2, and PC3, where the size of the data points is based on the TotalCoinSupply and the colors are based on the K-means predicted clusters.

** Conclusion:

In this report, we analyzed the cryptocurrency market data using unsupervised learning techniques such as PCA and K-means algorithm to process and cluster the data. We found that the best value for K was 4, and we created a scatter plot to visualize the different clusters of cryptocurrencies based on the PCA algorithm. This report provides a classification system that can be used for a new investment portfolio for Accountability Accounting.
