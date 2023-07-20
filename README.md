# Mushrooms: To Eat or Not To Eat
## Using machine learning algorithms to classify whether a mushroom is edible or poisonous based on the different features of the mushroom.

Victoria White

## Mushroom Classification
Wild mushrooms are commonly gathered to be used for things such as cooking. When digesting these mushrooms could be a matter of life or death, we want an algorithm that can quickly classify whether those wild mushrooms are poisonous or edible.

## Data
For this project, I used data from UCI Machine Learning. 

Dua, D. and Graff, C. (2019). UCI Machine Learning Repository [http://archive.ics.uci.edu/ml]. Irvine, CA: University of California, School of Information and Computer Science.

The graph below shows the amount of poisonous (blue bar) and edible (orange bar) mushrooms in our dataset. We see that there are slightly more edible mushrooms than poisonous. 

![image](https://user-images.githubusercontent.com/106834973/191843627-a60a6c01-6ebc-4976-aa91-4a05199e7183.png)


## Data Preparation
The only missing data was in stalk root. There were about 2400 entries as '?' or missing which is about 25% of our data for that feature. I dropped this feature because we have other feautures with characteristics of the mushroom stalk. Any method we use to fill in the missing data could result in a biased feature. The models used in this project are logistic regression and KNearest neighbor which both require the dataset to be scaled. However, all our data is categorical and will need to be OneHotEncoded which does not require any scaling. After the data is OneHotEncoded, it will be ready to use in our models.

## Results


The graph below shows whether a mushroom is poisonous (orange) or edible (blue) based on spore print color. We see that there are a few spore print colors that are definitely safe and a few that are more likely poisonous. 

![spore print](https://user-images.githubusercontent.com/106834973/193132790-314dc224-b08b-4bf7-81f6-80d19c413739.jpg)

## Model
KNeighbors model had the best predictions for this dataset. The KNN model has the least amount of false negative errors with 0 errors.. We want a lower false negative error because it is more costly to label a poisonous mushroom edible than it is to label an edible mushroom as poisonous.

![confus_mushroom](https://user-images.githubusercontent.com/106834973/193132522-31f143a1-e507-4aef-a045-a66b321168b2.jpg)

The logistic regression model had 26 false negatives whle the KNN model had 0. 

## Recommendations
When classifying mushrooms, some important features to look at are odor and spore print color. If a mushroom has any odor, it is more likely poisonous than edible. If a mushroom has a buff, orange, purple, or yellow spore print, that mushroom is safe to eat! Mushrooms with chocolate, green, or white spore prints are more likely to be poisonous than edible. 

## Limitations 
This dataset has a high correlation between features. This correlation could make our model perform poorer on new data that provides new information.

## For further information
For additional questions, please contact victoria.white1317@gmail.com
