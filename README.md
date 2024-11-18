# Building a K-Means Clustering Model


---

## Introduction
A real estate firm that has been utilizing the King County dataset is currently engaging with potential buyers. Each buyer expresses interest in specific properties; however, due to various factors, such as a property being removed from the market, they may not secure their preferred options. Consequently, the real estate agent must suggest alternative properties that closely resemble the buyers' initial selections. Determining what constitutes "similar" is complex, given the multitude of factors influencing a buyer's preferences.

Previously, a machine learning model was developed to forecast housing prices, which was a supervised learning task due to the presence of a target variable (price). Nonetheless, the dataset can be leveraged for various analytical challenges beyond price prediction. In this instance, the goal is to categorize or cluster properties based on the similarity of their characteristics. Since there is no specific label to predict, this scenario falls under unsupervised learning, which will be tackled using k-means clustering techniques.

This examination will allow classifying wines as being a particular type.

This project will scope, analyze, prepare, plot data, and seek to explain the findings from the analysis.

**Feature Information**

- id—Unique identifier for each house sold.
- date—Date of the house's most recent sale.
- price—Price the house most recently sold for.
- bedrooms—Number of bedrooms in the house.
- bathrooms—Number of bathrooms. A room with a toilet but no shower is counted as 0.5.
- sqft_living—Square footage of the house's interior living space.
- sqft_lot—Square footage of the lot on which the house is located.
- floors—Number of floor levels in the house.
- waterfront—Whether the property borders on or contains a body of water. (0 = not waterfront, 1 = waterfront)
- view—An index from 0 to 4 representing the subjective quality of the view from the property. The higher the number, the better the view.
- condition—An index from 1 to 5 representing the subjective condition of the property. The higher the number, the better the condition.
- grade—An index from 0 to 14 representing the quality of the building's construction and design. The higher the number, the better the grade.
- sqft_above The square footage of the interior housing space that is above ground level.
- sqft_basement—The square footage of the interior housing space that is below ground level.
- yr_built—The year the house was initially built.
- yr_renovated—The year of the house's last renovation.
- zipcode—What zipcode area the house is located within.
- lat—Latitude of the house's location.
- long—Longitude of the house's location.
- sqft_living15—The square footage of interior housing living space for the nearest 15 neighbors.
- sqft_lot15—The square footage of the lan
  
Here are a couple of questions that this project seeks to answer:

- How many houses are present in each cluster?
- What factors contributed to the formation of the clusters in relation to their geographical location?
- What elements influenced the creation of clusters in relation to price per square foot?
- Is this model effective in addressing the challenge of suggesting comparable homes to buyers interested in a particular property?
- What are some potential reasons that could necessitate the retraining of this model over time?


**Data Sources:**
- kc_house_data_prep.pickle
- kc_house_data_prep_norm.pickle



## Project Goals
The objective is to categorize or cluster residences by analyzing the similarities in their characteristics.g

#### Why use a k-means clustering algorithm to?
K-means clustering is an unsupervised machine learning algorithm designed to categorize similar data points into distinct groups, thereby uncovering underlying patterns within the dataset. Each data point is assigned to the cluster whose centroid, or central point, is nearest to it. As a result, the algorithm produces clusters of data that demonstrate statistical similarities. K-means clustering is therefore appropriate for grouping data based on likeness especially in situations where traditional classification and regression models are defective.


## Data
An anonymized dataset that can be used to train the machine-learning model has been found. It is a CSV file containing 21,609 housing records. 


## Conclusions

- How many houses are present in each cluster?
    - Number of houses in cluster 0 = 5522
    - Number of houses in cluster 1 = 8649
    - Number of houses in cluster 2 = 1665
    - Number of houses in cluster 3 = 3490
    - Number of houses in cluster 4 = 2283
      
- What factors contributed to the formation of the clusters in relation to their geographical location?
    - Each cluster appears to be its own quadrant on the map, with cluster 0 representing the southwest; cluster 1 representing the northwest; cluster 2 representing the northeast; and cluster 3 representing the southeast.
      
- What elements influenced the creation of clusters in relation to price per square foot?
    - Cluster 3 includes the lowest-priced homes; cluster 0 includes the second lowest-priced homes; cluster 2 includes the second highest-priced homes; and cluster 1 includes the highest-priced homes. Other than the heatmap, this is also exhibited in the fact that the size of each data point corresponds to its total price.


- Is this model effective in addressing the challenge of suggesting comparable homes to buyers interested in a particular property?
    - Given its unsupervised nature, it's very difficult to evaluate the performance of a clustering model. The best weapons are knowing what is desired out of the model and performing clustering analysis. In this case, the number of clusters isn't supported much by domain knowledge; in other words, there's no set number of groups that houses need to fall into. However, one might argue that more clusters will be helpful to the real estate agents, as they will narrow down the houses more. Still, one may have to trust in analysis methods like silhouette analysis and elbow plots. Although the former was chosen to influence the final model, you could choose the latter and it would be no less valid. There might also be some value found in doing further analysis by plotting the clusters in more than just the latitude and longitude dimensions. Going back to domain knowledge and what you desire out of the model, you may determine that some features are more important than others, which might influence your clustering decisions.

  
- What are some potential reasons that could necessitate the retraining of this model over time?
    - There are several factors that could potentially require a retrain of this clustering model, most of which have to do with the dataset. In particular, this dataset was captured at a certain point in time, and therefore may not reflect future changes. For example, housing trends come and go, and what may have been a desirable trait when this data was collected may not be as desirable in the future. Likewise, changing economic factors can greatly affect the value of a house from year to year, so you'll likely need to update the model to account for this.

