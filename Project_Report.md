# Bike-Sharring-Demand-Project
Udacity's AWS Machine Learning Engineering Scholarship's first project on Bike Sharing Demand on kaggle.

# Report: Predict Bike Sharing Demand with AutoGluon Solution
#### NAME HERE
IKWUONWU JONATHAN UKAEGBU
## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results? 
TODO: Add your explanation
I relized that there were three(3) negative values in the prediction series. i had to change the negative values in the prediction series to zero.
### What was the top ranked model that performed?
TODO: Add your explanation
WeightedEnsemble_L3 -115.262223 
## Exploratory data analysis and feature creation
### What did the exploratory analysis find and how did you add additional features?
TODO: Add your explanation
it gave me a better understanding of the dataset i was working with, the mean values, standard deviation and the maximum and minimum value of the train dataset.i added additional feature to the train and test data set with this line of code:
train["month"] = pd.to_datetime(train.loc[:, "datetime"]).dt.month
test["month"] = pd.to_datetime(test.loc[:, "datetime"]).dt.month

### How much better did your model preform after adding additional features and why do you think that is?
TODO: Add your explanation
There was no much difference between the initial result and the result after i added a new feature, i feel this was because the feature i chose was not the best fit for the project.
## Hyper parameter tuning
### How much better did your model preform after trying different hyper parameters?
TODO: Add your explanation
it performed far better than both the intial result and the result after i added the new feature
### If you were given more time with this dataset, where do you think you would spend more time?
TODO: Add your explanation
i will spend more time on feature creation, i would have added additional features to the dataset
### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.
|model|hpo1|hpo2|hpo3|score|
|--|--|--|--|--|
|initial|Defalt|default|default|1.31150|
|add_features|default|Default|Default|1.40399|
|hpo|NN epochs[10], activation:['relu', 'softrelu',n'tanh'], Layers:[[100],[1000],[200, 100],[300,200,100]]|?|?|1.31150|

### Create a line plot showing the top model score for the three (or more) training runs during the project.

TODO: Replace the image below with your own.

![image](https://user-images.githubusercontent.com/86266982/152699424-e968dbad-e94a-4c14-a59b-b646a0c07c57.png)



### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.

TODO: Replace the image below with your own.

![image](https://user-images.githubusercontent.com/86266982/152699441-2d701d24-a643-4383-a0ca-b105cfc65f76.png)


## Summary
TODO: Add your explanation
this is my first time using the amazon sagemaker with Autogloan, and i hope to learn and understand more as i continue to practise. also hyperparameter turning may work better if we understand the ML model better.i was able to go
