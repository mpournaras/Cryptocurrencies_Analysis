# Cryptocurrency Analysis Challenge:
Unsupervised Machine Learning and Cryptocurrencies

![Splash](https://github.com/mpournaras/Cryptocurrencies_Analysis/blob/main/Images/splash.jpg)

## Purpose: 
A client asked for a list of tradable cryptocurrencies and wants to be able to pick them from a classification system.    

1. Describe the differences between supervised and unsupervised learning, including real-world examples of each.
2. Preprocess data for unsupervised learning.
3. Cluster data using the K-means algorithm.
4. Determine the best number of centroids for K-means using the elbow curve.
5. Use PCA to limit features and speed up the model.

## Deliverables:

* Deliverable 1: Preprocessing the Data for PCA
* Deliverable 2: Reducing Data Dimensions Using PCA
* Deliverable 3: Clustering Cryptocurrencies Using K-means
* Deliverable 4: Visualizing Cryptocurrencies Results

## Results:

### Deliverable 1:

In this section I was able to clean the data by:

* Removing all cryptocurrencies that are not being traded from the crypto_df DataFrame.
* The IsTrading column is dropped from the crypto_df DataFrame.
* Removing all cryptocurrencies with at least one null value from the crypto_df DataFrame.
* Removing all the rows that do not have coins being mined from the crypto_df DataFrame.
* Dropping the "IsTrading" column from the crypto_df DataFrame.
* Dropping the "CoinName" column from the crypto_df DataFrame.
* Creating a new DataFrame that stores the names of all cryptocurrencies from the "CoinName" column and has the index from the crypto_df DataFrame.
* Using the get_dummies() method to create variables for all of the text features, which are then stored in a new DataFrame.
* Standardized the features from the X DataFrame using the StandardScaler fit_transform() function.

**The imported DataFrame before cleaning, 1252 rows of data:**

![Pic 1](https://github.com/mpournaras/Cryptocurrencies_Analysis/blob/main/Images/initial_df.PNG)

**The list of tradable cryptocurrencies after cleaning, 532 rows of data:**

![Pic 2](https://github.com/mpournaras/Cryptocurrencies_Analysis/blob/main/Images/clean_df.PNG)

### Deliverable 2:

Using my knowledge of how to apply the Principal Component Analysis (PCA) algorithm, I reduced the dimensions of the X DataFrame to three principal components and placed these dimensions in a new DataFrame.

![Pic 3](https://github.com/mpournaras/Cryptocurrencies_Analysis/blob/main/Images/PCA.png)

### Deliverable 3:

Using my knowledge of the K-means algorithm, I created an elbow curve using hvPlot to find the best value for K from the pcs_df DataFrame created in Deliverable 2. Then, I ran the K-means algorithm to predict the K clusters for the cryptocurrencies’ data.

**Applying the Principal Component Analysis:**

![Pic 4](https://github.com/mpournaras/Cryptocurrencies_Analysis/blob/main/Images/PCA_df.PNG)

**K-means Clustering Algorithm, Elbow Curve:**

![Pic 5](https://github.com/mpournaras/Cryptocurrencies_Analysis/blob/main/Images/elbow_curve.PNG)

### Deliverable 4:

Using my knowledge of creating scatter plots with Plotly Express and hvplot, I visualized the distinct groups that correspond to the three principal components I created in Deliverable 2, then I created a table with all the currently tradable cryptocurrencies using the hvplot.table() function.

**3D Scatterplot with Clusters, Visualizing Tradable Cryptocurrencies:**

![Pic 6](https://github.com/mpournaras/Cryptocurrencies_Analysis/blob/main/Images/3D_model.png)

**Number of Tradable Cryptocurrencies:**

![Pic 7](https://github.com/mpournaras/Cryptocurrencies_Analysis/blob/main/Images/tradable_crypto_count.PNG)

**DataFrame to plot results:**

![Pic 8](https://github.com/mpournaras/Cryptocurrencies_Analysis/blob/main/Images/crypto_df.PNG)

**Tradable Cryptocurrencies:**  

![Pic 9](https://github.com/mpournaras/Cryptocurrencies_Analysis/blob/main/Images/tradable_crypto_results.png)
