# Clustering product features

## Background
Worked on a project as part of product marketing that involved identifying an approach/framework to nudge users to try a higher plan. I was using an existing dataset with adoption ratings displayed for each feature used by a specific customer account. This project uses a representation of the dataset and explores a better approach to nudge customers based on their product usage to try a higher plan.

## Problem
* Customers in the top paid plans use key features together to achieve a specific goal, but it is not straightforward to identify clusters of features and map them to a customer goal. 
* Not mapping features to top goals can make it difficult to segment customers and nudge them towards trying a higher plan based on their product usage.  

## Solution
Used hierarchical clustering to identify product feature clusters which can then be mapped to a specific customer goal. This involved:

* Transforming categorical values of adoption rating under each feature (high, medium, low) to numerical values using ordinal encoding.
* Creating a correlation table to identify features that have high correlation based on their encoded adoption rating.
* Using the correlation table in the hierarchical clustering model to identify all possible feature clusters from the dataset.
* Reducing the dimensions of the correlation table using PCA to represent the feature clusters in a two dimensional space in the form of a scatter plot.

## Result
Features like analytics and custom fields are clustered together in the scatter plot since they can be mapped to a customer goal of 'tracking team performance'. From here, any customer who has a high adoption rating for custom fields, which is available in the lower plan, can be nudged to try the analytics module in the higher plan to achieve the goal of tracking team performance. GTM team engagement efforts can also be aligned to these insights. 
