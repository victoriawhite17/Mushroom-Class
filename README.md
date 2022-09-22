# Mushrooms: To Eat or Not To Eat
## Using machine learning algorithms to classify whether a mushroom is edible or poisonous based on the different features of the mushroom.

Victoria White

## Mushroom Classification
Wild mushrooms are commonly gathered to be used for things such as cooking. When digesting these mushrooms could be a matter of life or death, we want an algorithm that can quickly classify whether those wild mushrooms are poisonous or edible.

## Data
For this project, I used data from UCI Machine Learning. 

Dua, D. and Graff, C. (2019). UCI Machine Learning Repository [http://archive.ics.uci.edu/ml]. Irvine, CA: University of California, School of Information and Computer Science.

This dataset is balanced between edible and poisonous mushrooms allowing us to gain a lot of information regarding features for classification. When classifying mushrooms, some important features to look at are odor, gill attachment, and spore print color. 

## Data Preparation
The only missing data was in stalk root. There were about 2400 entries as '?' or missing which is about 25% of our data for that feature. I dropped this feature because we have other feautures with characteristics of the mushroom stalk. Any method we use to fill in the missing data could result in a biased feature. The models used in this project are logistic regression and KNearest neighbor which both require the dataset to be scaled. However, all our data is categorical and will need to be OneHotEncoded which does not require any scaling. After the data is OneHotEncoded, it will be ready to use in our models.

## Results
The graph below shows the amount of poisonous (blue bar) and edible (orange bar) mushrooms in our dataset. We see that there are slightly more edible mushrooms than poisonous. 

![image](https://user-images.githubusercontent.com/106834973/191843627-a60a6c01-6ebc-4976-aa91-4a05199e7183.png)


The graph below shows whether a mushroom is poisonous (orange) or edible (blue) based on spore print color. We see that there are a few spore print colors that are definitely safe and a few that are more likely poisonous. 

![spore_print](https://user-images.githubusercontent.com/106834973/191844026-7d7e90dd-0da1-436b-8c55-912dacc10235.png)


## Model
KNeighbors model had the best predictions for this dataset. The KNN model has the least amount of false negative errors with 115 total. We want a lower false negative error because it is more costly to label a poisonous mushroom edible than it is to label an edible mushroom as poisonous.

![confusion_matrix_mushroom](https://user-images.githubusercontent.com/106834973/191845899-c4f75404-dfa8-4c27-a87e-73221af25051.png)

The logistic regression model had 212 false negatives whle the KNN model had 115. We were able to reduce the errors by 97.

## Recommendations
The KNN model had the best performance, but we could explore other models to see if we can get better predictions.

## Limitations 
The logistic regression model didn't perform better even after tuning the parameters. Another model could be used to better evaluate KNN's performance on our dataset. The KNN model was tuned, but we could explore other hyperparameters to see if any would help our predictions. 

## For further information
For additional questions, please contact victoria.white17@hotmail.com
