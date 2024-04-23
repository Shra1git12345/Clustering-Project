# Clustering-Project
you will categorise the countries given in a data set using some socio-economic and health factors that determine the overall development of the country. Understand the problem statement carefully before solving the problem. After that, you can go through the solution and understand one way of solving it.   
Problem Statement
HELP International is an international humanitarian NGO committed to fighting poverty and providing the people of backward countries with basic amenities and relief during the time of disasters and natural calamities. It regularly runs operational projects, along with advocacy drives, to raise awareness and for funding purposes.

 

After the recent funding programmes, they were able to raise around $10 million. Now, the CEO of the NGO needs to decide how to use this money strategically and effectively. The significant issues that arise while taking these decisions are mostly related to choosing the countries that are in dire need of aid.

 

This is where you come in as a data analyst. Your job is to categorise the countries using some socio-economic and health factors that determine the overall development of the country. Then, you need to suggest the countries that the CEO needs to focus on the most. The data sets containing those socio-economic factors and the corresponding data dictionary are provided below.

Note: The inflation definition in the data dictionary has a typo. The correct definition would be the measurement of the annual growth rate of the GDP deflator.

 Objectives
Your main task is to cluster the countries by the factors mentioned above and then present your solution and recommendations to the CEO using a PPT. The following approach is suggested:

 
Start off with the necessary data inspection and EDA tasks suitable for this data set – data cleaning, univariate analysis, bivariate analysis, etc.
You must perform the outlier analysis on the data set. However, you do have the flexibility of not removing the outliers if it suits the business needs or a lot of countries are getting removed. All you need to do is find the outliers in the data set, and then choose whether to keep them or remove them, depending on the results you get.
Try K-means clustering on this data set to create the clusters.
Analyse the clusters and identify the ones that are in dire need of aid. You can analyse the clusters by comparing how these three variables (gdpp, child_mort and income) vary for each cluster of countries, and recognise and differentiate the clusters of developed countries from the clusters of underdeveloped countries.
Also, you need to perform visualisations on the clusters that have been formed. You can do this by choosing any two of the three variables mentioned above on the X–Y axes and plotting a scatter plot of all the countries and differentiating the clusters. Make sure you create visualisations for all the three pairs. You can also choose other types of plots like boxplots.
Make sure that you report at least five countries that are in dire need of aid from the analysis work that you perform.




Some pre info :
Briefly explain the steps of the K-means clustering algorithm.
1. Steps of K-Means Algorithm
K-Means algorithm is the process of dividing the N data points into K groups or
clusters. The steps of the algorithm are:
(a) Start by choosing K random points, the initial cluster centres.
(b) Assignment Step: Assign each data point to their nearest cluster centre, i.e., the
cluster centre having the minimum Euclidean distance from the data point.
(c) Optimisation Step: For each cluster, recompute the new cluster centres which
will be the mean of all cluster members that were assigned in the previous step.
(d) Now re-assign all the data points to the different clusters by using the new cluster
centres.
(e) Keep iterating through step (c) & (d) until there are no further changes possible.

How is the value of ‘k’ chosen in K-means clustering? Explain both the statistical as well as the business aspect of it.
 The value of K can be chosen in 2 ways. Either by using statistical analyses or by
using the business aspect. Both are explained below.
Statistical Analyses
You can use either the silhouette score or the elbow curve to find the optimal value of K. At this value, the most stable clusters are formed. The silhouette value is a
measure of how similar an object is to its own cluster (cohesion) compared to other clusters (separation). The silhouette ranges from −1 to +1, where a high value indicates that the object is well matched to its own cluster and poorly matched to neighbouring clusters.
The elbow curve method uses the sum of square distances method to find the most
optimal clusters at the point where there is not much change in the inertia, i.e., where distinct elbows are being formed.
Business Aspect
This is mostly oriented for situations where the business understanding of the problem dictates as to how many clusters need to be created. For example, if a food
delivery company wants to create 5 hubs in a city, it needs to find the 5 most optimal points as to where it needs to be located so that the fastest delivery can happen. So, in this case you need to create 5 clusters, irrespective of whether the statistical analyses give a different result.


Explain the necessity of scaling/standardisation before performing clustering.
Standardisation is the process of converting all the columns in any dataset to a comparable scale before applying the method of clustering. This is done to offset the
effect of very large-scale variables on those having low scale.
For example, if you want to cluster a list of employees based on the salary that they earn and the avg. hours that they work per day, then you’d find that the salary column
would have a scale that is at least a thousand times more than the hours column. Now, clustering algorithms use Euclidean distance to compute the similarity between two
points, this measure would be heavily influenced by the salary column only due to its larger scale. Therefore, to make sure that the employees are getting clustered properly
using both the columns, we use standardisation - to bring the mean of each column to 0 and standard deviation 1.
 
