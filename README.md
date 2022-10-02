# Cryptocurrencies
Module 18 Challenge

## Overview

*Background and Purpose*
Accountability Accounting, a prominent investment bank, is interested in offering a new cryptocurrency investment portfolio for its customers. The company, however, is lost in the vast universe of cryptocurrencies. So, they’ve asked me to create a report that includes what cryptocurrencies are on the trading market and how they could be grouped to create a classification system for this new investment.

The data I will be working with is not ideal, so it will need to be processed to fit the machine learning models. Since there is no known output for what I'm looking for, I have decided to use unsupervised learning. To group the cryptocurrencies, I will be using clustering algorithm and use data visualizations to share the findings with the board.

## Analysis

*Deliverable 1: Preprocessing the Data for PCA*

The IsTrading column is dropped, rows that have null values are removed, and the CoinName column is removed. One main step is to standarize the features to prepare the data the next steps.

![Data Preprocessing](https://github.com/nadiezhdamhb/Cryptocurrencies/blob/main/Resources/Deliverable1.png)


*Deliverable 2: Reducing Data Dimensions Using PCA*

The PCA algorithm reduced the dimensions of the dataframe down to only three principal components. 

![PCA Dimensions](https://github.com/nadiezhdamhb/Cryptocurrencies/blob/main/Resources/Deliverable2.png)


*Deliverable 3: Clustering Cryptocurrencies Using K-means*

I created an elbow curve to be able to find the best K value. The elbow curve shows that a point at four is present which means that the data can be classified into four classes. 

![Elbow Curve](https://github.com/nadiezhdamhb/Cryptocurrencies/blob/main/Resources/Deliverable3.png)

By using the K-means algorithm, predictions of the K clusters can be made for the data provided for cryptocurrency.

![Table](https://github.com/nadiezhdamhb/Cryptocurrencies/blob/main/Resources/Deliverable3_df.png)

*Deliverable 4: Visualizing Cryptocurrencies Results*

The three clusters are shown in three different colors. 

![Clusters](https://github.com/nadiezhdamhb/Cryptocurrencies/blob/main/Resources/Deliverable4_fig.png)

The table contains 532 tradable cryptocurrenies.

![Table of Tradable Crypto](https://github.com/nadiezhdamhb/Cryptocurrencies/blob/main/Resources/Deliverable4_table.png)

The scatterplot shows TotalCoinsMined vs. TotalCoinSupply by class. When you hover over each point, you are able to see more information on the class type, totalCoinsMine, totalCoinSupply, and CoinName.

![Scatter Plot](https://github.com/nadiezhdamhb/Cryptocurrencies/blob/main/Resources/Deliverable4_fig2.png)


![Hovering](https://user-images.githubusercontent.com/102566199/184518578-8fa80e98-5177-44a4-a26a-83b9f01a947f.png)

## Summary

The majority of the crytocurrencies were either Class 0 or Class 1 which are the dots in blue and red on the previous scatter plot shown. These two classes are clustered near the origin of the graph. However, Class 2 is really far from the origing and it's seen as an outlier in the graph (dot in yellow) whereas class 3 (green dots) is close to the origing near class 1 (red dots) but you can see a few of them and not as many as blue and red dots.


*Recommendations*

For future analysis, I suggest removing the class 2 and class 3 crytocurrencies to help improve the scatter plot and create a better scaled visualization. 
