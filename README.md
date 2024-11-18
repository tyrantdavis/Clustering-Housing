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

TBD..
