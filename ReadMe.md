# **A summary of findings and insight**

#### The objective of this analysis was to identify distinct energy consumption profiles in the dataset using clustering algorithms. And this happened by dividing the data into clusters to give us meaningful insights. Also, we try to understand the patterns in the consumption data, and this summary will explain the findings and insights got from the analysis.


# **Key Findings and Insights**




#### We started by loading the dataset and importing the necessary packages for the project. The first step in data preparation involved feature engineering a pivot DataFrame that consists of energy consumption values, with 24 columns representing each hour of the day.

#### Next, we checked the dataset for any null values. To handle missing data, we used interpolation methods and then filled any remaining NaN values with the mean. This ensured that our dataset was free from null values, which is crucial for generating accurate insights.

#### We then visualized the average energy consumption per hour to gain a better understanding of the dataset and its trends. Afterward, we normalized the data to eliminate redundancy and address any inconsistencies.

#### We proceeded by plotting a boxplot of the dataset and histograms for each hour. These visualizations helped us identify important patterns and anomalies in the data. Upon reviewing these, it became clear that there were many outliers present in the data.

#### At this stage, we faced a decision on which scaler to use: Standard Scaler, Min-Max Scaler, or Robust Scaler. To assist in this decision, we plotted boxplots for the dataset after applying each scaler and found that Robust Scaler performed best, as it handles outliers more efficiently.

#### With the data normalized and prepared, we implemented the K-Means clustering algorithm. We used the Elbow method to determine the optimal value of k (the number of clusters). Based on the graph, we identified that the best value of k was 3.

#### After selecting the optimal k, we fitted the K-Means model, predicted the clusters, and added a new column called "clusters" to both the scaled DataFrame and the original DataFrame. We then calculated the cluster centers and used these to plot the average daily profiles for each cluster. Additional visualizations, such as pie charts and bar charts, were also created to further illustrate these findings.

#### To explore the effects of different k values, we conducted a comparison between k=3 and k=4. We visualized the results using PCA, heatmaps, average daily profiles, and cluster distribution over time graphs. This allowed us to see the differences between these k values and assess which one was more effective in defining meaningful clusters.

#### Next, we advanced our methods by using the silhouette score to determine the optimal k value. We repeated the process for the new optimal k, again visualizing the results with PCA, heatmaps, average daily profiles, and cluster distribution graphs.

#### To further enhance our visualizations, we applied both t-SNE and PCA techniques.

#### We then analyzed the data based on different time periods, including weekdays vs. weekends, months, and quarters. This allowed us to better understand how energy consumption varied across these different dimensions. Additionally, we plotted the energy usage for specific time periods (morning, afternoon, evening, and night) and visualized the differences in energy usage between weekdays and weekends, as well as across months and quarters.

#### Finally, we experimented with alternative clustering algorithms, including GMM (Gaussian Mixture Model), Agglomerative Clustering, and DBSCAN, to see if they could outperform K-Means. While these algorithms yielded good results, none surpassed K-Means in terms of producing high-quality insights from the dataset.

#### This process allowed us to thoroughly explore the data and extract meaningful insights about energy consumption patterns.



####################


we loaded the dataset and the required packages just to start on the data preperation. we feature engineered a pivot Dataframe that consists of the value of energy consumption and 24 hours as a columns.
then we started to check if the data contains any null values and used interpolate methods to fill the missing values and then made sure to fill the NaN values with mean value to make sure that the dataset contains no NaN, because it will have an affect on the insights we produce.

we then started to visualize the avg. energy consumption per hour from the dataset to have a better understanding of what are we dealing with

then we normalize the data to eliminate redundancy and inconsistent dependency.

we plotted a boxplot of the dataset and a histrogram of each hour to have some observations that will be useful in the future

now, there are a confusion on which scaler to use whether it's Standard scaler, Min Max scaler or Robust scaler

we plotted a boxplot for the dataset and plotted each one of the scalers to see how does it change based on the graph we plotted (boxplot of dataset)

based on the previous boxpolt and histrogram, we observed that that data got a lot of outliers and the best scaler to use is the Robust scaler because it can deal with the outliers effciently


after normalizing and preparing our data, we start to implement the K-Means clustering Algorithm

first we used elbow method to get the optimal value of k (K means number of clusters) and we observed from the graph that the best value of K is 3

After knowing the optimal k value, we start to fit and predict the K-Means and add the Cluster labels to a column called clusters to both the scaled DataFrame and the original DataFrame

after getting the centers of a cluster and adding them to a DataFrame to plot the average daily profiles for each culster then add another graphs like pie chart, bar chart.

we wanted to compare the difference between using optimal k and another k value, So we made a comparison between k= 3 and 4.

we visualized a PCA, heatmap, average daily profiles and clusters distribuation over time graph for each k value.

these graphs showed us the real difference between the k values and which one was better in defining the dataset as clusters to obtain high quality insights


then we wanted to advance our methods to get the optimal k value using a silhouette score and the number with highest score will be the optimal k value

moreover, we did the same with the new optimal k and visualized a PCA, heatmap, average daily profiles and clusters distribuation over time graph.


then we wanted to add more visulaization, that's why we used t-sne and pca


then we tried to analyize the data by identifying weekends and weekdays, months and quarter, we plotted each to understand the dataset more and more


then we started to represent our clusters with time periods over 4 time periods (morning, afternoon, evening and night)

then we used the weekend and weekdays to graph the energy usage per each.

then we applied the same concept to the months and quarters


finally we started to use different clustering algorithms (GMM, Agglomerative, DBSCAN) to see if they can outperform the K-means and it tuns out that they gave use a very good results but not better than K-Means.
