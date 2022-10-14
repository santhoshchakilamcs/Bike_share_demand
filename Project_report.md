# Report: Predict Bike Sharing Demand with AutoGluon Solution
#### Santhosh Chakilam

## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
When I tried to submit the predictions, I saw the values of the predictions where there were negative values which I thought the score would be high and there might be correlation between independent variables and I changed the negative values to zero and still the model did not provide with low RMSE.

### What was the top ranked model that performed?
 WeightedEnsemble_L3 is the best model that gave less RSME score for the unchanged dataset, added features dataset and hypermeters tuned dataset.

## Exploratory data analysis and feature creation
### What did the exploratory analysis find and how did you add additional features?
After seeing the histogram, I thought if I could add a month feature for the remaining features that would make sense. Because, in which month the bike sharing has happened more will be apt one.

### How much better did your model preform after adding additional features and why do you think that is?
The model performed really well after adding features and the RSME is reduced around 0.5 from initial RSME.

## Hyper parameter tuning
### How much better did your model preform after trying different hyper parameters?
I think the hyperparameters tuning did not give much effect after adding the features the RSME is almost the same.

### If you were given more time with this dataset, where do you think you would spend more time?
Yes, I might add few features, drop few features, check correlation and tune with multiple hyperparameters.

### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.
|model|hpo1|hpo2|hpo3|score|
|--|--|--|--|--|
|initial|"default_values"|"default_values"|"default_values"|1.80877|
|add_features|"default_values"|"default_values"|"default_values"|1.32921|
|hpo|"NN_options"|"GBM_options"|"default_values"|1.30702|

### Create a line plot showing the top model score for the three (or more) training runs during the project.


![model_train_score.png](Bike_Share/project/model_train_score.png)

### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.


![model_test_score.png](Bike_Share/project/model_test_score.png)

## Summary
Initially, the model performed week on the dataset and on adding feature the model performed better than before. The hyperparameter did not give much effect to the model and the RSME is almost equal. I think the hyperparameters aren't tuned very well. I should try different hyperparameters to get the good results.  
