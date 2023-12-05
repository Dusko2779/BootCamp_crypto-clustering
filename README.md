# Module_19_Crypto_Clustering

### Instructions
Rename the Crypto_Clustering_starter_code.ipynb file as Crypto_Clustering.ipynb.

Load the crypto_market_data.csv into a DataFrame.

Get the summary statistics and plot the data to see what the data looks like before proceeding.

![image](https://github.com/Dusko2779/BootCamp_crypto-clustering/assets/134830906/39ec2428-6b3a-4846-9557-69dcaa985c36)


Prepare the Data
Use the StandardScaler() module from scikit-learn to normalize the data from the CSV file.

Create a DataFrame with the scaled data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame.

![image](https://github.com/Dusko2779/BootCamp_crypto-clustering/assets/134830906/0e90746e-d034-403f-ada7-1a816209e264)


The first five rows of the scaled DataFrame should appear as follows:

The first five rows of the scaled DataFrame

Find the Best Value for k Using the Original Scaled DataFrame
Use the elbow method to find the best value for k using the following steps:

![image](https://github.com/Dusko2779/BootCamp_crypto-clustering/assets/134830906/de40bbf8-8252-4025-aea0-d2ac363ff22c)


Create a list with the number of k values from 1 to 11.
Create an empty list to store the inertia values.
Create a for loop to compute the inertia with each possible value of k.
Create a dictionary with the data to plot the elbow curve.
Plot a line chart with all the inertia values computed with the different values of k to visually identify the optimal value for k.
Answer the following question in your notebook: What is the best value for k?

![image](https://github.com/Dusko2779/BootCamp_crypto-clustering/assets/134830906/ba2134b2-adb8-4930-b68a-a258c5e4a64b)


Cluster Cryptocurrencies with K-means Using the Original Scaled Data
Use the following steps to cluster the cryptocurrencies for the best value for k on the original scaled data:

Initialise the K-means model with the best value for k.
Fit the K-means model using the original scaled DataFrame.
Predict the clusters to group the cryptocurrencies using the original scaled DataFrame.

![image](https://github.com/Dusko2779/BootCamp_crypto-clustering/assets/134830906/88586bc0-9ba5-4e80-9d77-2de588d61074)


Create a copy of the original data and add a new column with the predicted clusters.
Create a scatter plot using hvPlot as follows:
Set the x-axis as "PC1" and the y-axis as "PC2".
Colour the graph points with the labels found using K-means.
Add the "coin_id" column in the hover_cols parameter to identify the cryptocurrency represented by each data point.
Optimise Clusters with Principal Component Analysis
Using the original scaled DataFrame, perform a PCA and reduce the features to three principal components.
