# Mushrooms:To Eat or Not To Eat
##Using machine learning algorithms to classify whether a mushroom is edible or poisonous based on the different features of the mushroom.

Victoria White

##Mushroom Classification
Wild mushrooms are commonly gathered to be used for things such as cooking. When digesting these mushrooms could be a matter of life or death, we want an algorithm that can quickly classify whether those wild mushrooms are poisonous or edible.

##Data
For this project, I used data from UCI Machine Learning. 
Dua, D. and Graff, C. (2019). UCI Machine Learning Repository [http://archive.ics.uci.edu/ml]. Irvine, CA: University of California, School of Information and Computer Science.
This dataset is balanced between edible and poisonous mushrooms allowing us to gain a lot of information regarding features for classification. When classifying mushrooms, some important features to look at are odor, gill attachment, and spore print color. 

##Data Preparation
The only missing data was in stalk root. There were about 2400 entries as '?' or missing which is about 25% of our data for that feature. I dropped this feature because we have other feautures with characteristics of the mushroom stalk. Any method we use to fill in the missing data could result in a biased feature. The models used in this project are logistic regression and KNearest neighbor which both require the dataset to be scaled. Before I could scale the data I used a OneHotEncoder to change our categorical data for our models. 

##Results

