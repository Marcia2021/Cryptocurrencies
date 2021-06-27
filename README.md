# Cryptocurrency Analysis – Unsupervised Machine Learning

## Overview 

Unsupervised machine learning helps us explore data when there is no clear output to look for. For this project, we will be applying the knowledge of unsupervised machine learning to create a report that includes what cryptocurrencies are on the trading market, and use clustering algorithm to decide how they could be grouped to create a classification system for this new investment.

-	Preprocessing the data for PCA
-	Reducing data dimensions using PCA
-	Clustering Cryptocurrencies using K-means
-	Visualizing Cryptocurrencies results

## Results

1.	There are 532 records and 5 columns remined in the crypto data after conducted data preprocessing to keep all the cryptocurrencies that are being traded, have a working         algorithm, all of the columns with non-missing values, and the records where coins are mined. 

    ![inst1](https://user-images.githubusercontent.com/79289806/123530684-476d9080-d6cb-11eb-9b18-592696de1c41.png)
    
    Use get_dummies() to create variables for text features, and Standardize the data with StandardScaler().

2.	Used PCA to reduce dimension to three principal components. Then create a DataFrame with these three principal components. 

    ![inst2](https://user-images.githubusercontent.com/79289806/123530685-476d9080-d6cb-11eb-806d-5ee304b8d0ac.png)

3.	Created an elbow curve to find the best value for K.

    ![inst3](https://user-images.githubusercontent.com/79289806/123530686-476d9080-d6cb-11eb-8be0-eb4c039d8e2b.png)

    Based on the data of the three principal components, the best value for K is 4.

    Created a DataFrame including predicted clusters and cryptocurrencies features.

    ![inst4](https://user-images.githubusercontent.com/79289806/123530687-476d9080-d6cb-11eb-8d72-26397504a97a.png)

4.	Used scatter_cd() to create a 3D-Scatter with the PCA data and the clusters.
 
    ![inst5](https://user-images.githubusercontent.com/79289806/123530688-48062700-d6cb-11eb-8045-18b11af432e5.png)

    Used MinMaxScaler() and fit_transform() to scale the data with tradable cryptocurrencies. Then used the scaled data to create hvplot.scatter plot. From the plot below, there     are outliers from Class 2 and 3.

    ![inst6](https://user-images.githubusercontent.com/79289806/123530689-48062700-d6cb-11eb-8e04-fbb75faaf641.png) 

## Summary

After preprocess the data, we were able to standardize the data and use PCA to reduce the number of features. We used both K-means and Hierarchical clustering algorithm to analyze the data. For this analysis, both of these algorithms have four clusters of cryptocurrencies. With the current information provided from the analysis, further analysis could be done by limit to certain type of cryptocurrencies based on potential interests. 
