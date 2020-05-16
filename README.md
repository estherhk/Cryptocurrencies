# Cryptocurrencies

## Project Overview
Accountability Accounting, an investment bank, is interested in offering new cryptocurrencies investment portfolios.  Used unsupervised learning to process the data to fit maching learning models. Data preprocessing, PCA, and K-Means, and data visualizations(i.e. 3D scatter plot, hvplot.table, and 2D scatter plot) were used to present the results of which cryptocurrenices to invest in. Data was retrieved from CryptoCompare.

## Resources
1. Data Source:
- Cryptocurrencies.ipynb
- crypto_data.csv

2. Software:
- Jupyter Notebook
- Python

## Data Steps
### Data Pre-processing includes:
1. Remove Null Values
2. Convert all text values into numerical values
3. Scale the data

### Data Dimensions Using PCA
PCA is a model that minimizes the number of columns so it would be easier to read the dataset.  What is used is pca = PCA(n_components=3). 3 is the value that we are using so only 3 principal components and columns appear. Then fit_transform is used to get the principal components and then to result in a dataframe that has the 3 columns. 
Initialized PCA model to reduce the 98 columns to a value of 3(i.e.g n_components=3).  


<img width=“500” alt=“” src="https://github.com/estherhk/Cryptocurrencies/blob/master/images/PC.png">

### Clustering K-Means
To cluster the data, K-Means is used. Before finding the K-Means, elbow curve is used to find the K value(the number of clusters), which in this case is 4.  When the graph dips to a horizontal line, that was how 4 was determined to be the n_clusters. 
Use n_clusters=4 to in the K-means model to predict the clusters and class.


<img width=“500” alt=“” src="https://github.com/estherhk/Cryptocurrencies/blob/master/images/elbow_curve.png">

### Visualizing Results
1. 3D Scatter Plot
Created to demonstrate the 98 columns into 3 principal components and display the clusters. When hovering over points, the CoinName and data appear.

<img width=“500” alt=“” src="https://github.com/estherhk/Cryptocurrencies/blob/master/images/3D.png">

2. HvPlot Table
The hvplot table displays which class output is connected to the original dataset prior to applying the PC dataset.

<img width=“500” alt=“” src="https://github.com/estherhk/Cryptocurrencies/blob/master/images/hvplot_t.png">

3. 2D Scatter Plot
MinMaxScaler was used to fit and transform the dataframe to display the different clusters in a 2D scatter plot(hvplot.scatter()) with X = TotalCoinsMined and Y = TotalCoinsSupply.

<img width=“500” alt=“” src="https://github.com/estherhk/Cryptocurrencies/blob/master/images/2D.png">

## Investment Recommendations
Based on the 2D scatter plot,  Class 3 that includes "Waves" and "Acute Angle Cloud", would not be a good investment due to low TotalCoinsMined and TotalCoinsSupply.  It would also be a recommendation to remove outliers as they are products built on block chain, but not cryptocurrencies.
