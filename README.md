# kNN_ANN_Cluster
This is an assignment I did for the course Machine Learning in Business. I need to construct models to give predictions and consultation for a client called FoodieBay -  an Indian multinational restaurant aggregator that operates a digital platform for food ordering, delivery services, and customer reviews and ratings across many cities in various countries. The platform offers information on partner restaurants, including menus, online ordering and table booking
options, the average cost for two, and user reviews and ratings. I explored the FoodieBay dataset, a subset of data generated from the FoodieBay platform, concerning their partner restaurants in India and user ratings.The client wants to better understand the factors that influence restaurant ratings (the rate column in the dataset) for two analytical tasks: data insights and machine learning opportunities, as follows.
Regarding the former, the client has requested the following:
1. How many restaurants offer table booking, and what impact does it have on ratings (rate)?
2. How many restaurants offer online ordering, and what impact does it have on ratings (rate)?
3. What is the effect of the average cost for two (in INR) and average customer review ranking (ave_review_ranking in the dataset) on overall ratings (rate)?
4. How do ratings (rate) and average cost for two vary among the restaurant types?
5. Any additional insights about the restaurants, cities, and cuisines; for example, but not necessarily, what are the best- or worst- performing restaurants, or which city has the greatest number of restaurants
Regarding the latter, the client is interested in machine learning opportunities to predict restaurant ratings (rate) or categorise groups of similar restaurants. At this stage, one machine learning model is required.

## Process and explore data
I wrangle, pre-process data with handling missing values, one-hot encoding for categorical data, do exploratory data analysis to understand data in more details. I use Count Vectorizer to count the frequency of each word in each row in the column 'cuisines' because I think each word will represent a category of cuisines and can influence the rating.

## Model Development
* Supervised Machine Learning
  I fit 2 predictive supervised machine learning models into the dataset: kNN and Artificial Neural Networks ( do cross-validation) . I fit for the full dataset (baseline model) and the dataset with vectorizing "cuisines".

  The results show that:

  *kNN model* : average RMSE 0.14 , average R2: 0.88 (baseline model) ; average RMSE 0.11 , average R2: 0.93 (model with vectorizing "cuisine")

  *ANN model*: RMSE 0.266 ,   R-squared 0.581 (baseline model) ;  RMSE 0.23 , R-squared 0.68 ( model with vectorizing "cuisine")

* Unsupervised Machine Learning
  I clustered the dataset with K-Means Clustering based on : restaurant type and ave_review_ranking and k=7. The clusters categorizes restaurants into clearly different types: casual dining, quick bites, cafe,...
  
  
  
  
