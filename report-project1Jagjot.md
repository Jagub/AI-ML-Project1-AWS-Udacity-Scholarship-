# Report: Predict Bike Sharing Demand with AutoGluon Solution
Jagjot Singh

## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
At the first model I was predicting count without adding any features it was just a preset model just to test how much good it performs also before submittingthe model all negative values were set to 0 because kaggle will reject it.

### What was the top ranked model that performed?
The Top Ranked model was that was trained and tuned with Hyperparameters I got a score of 0.46806

## Exploratory data analysis and feature creation
### What did the exploratory analysis find and how did you add additional features?
In the exploratory analysis with no new features I got a score of 1.796913 after that to improve the model I seperated the datetime into hour,day,month ,year after adding this feature with season,weather data type as category after training i got a score of 0.67826

### How much better did your model preform after adding additional features and why do you think that is?
By adding these seperating datetime as a new feature I improved my score from 1.796913 to 0.67826

## Hyper parameter tuning
### How much better did your model preform after trying different hyper parameters?
So by adding some new features to get it to next level to improve the score there is hyperparameter optimization so firstly i used rf model having 'n_estimators': [100,125,150] ,'max_depth': [5, 7,10],'min_samples_split': [2, 5, 10],'min_samples_leaf': [1, 2, 4],'max_features': ['auto', 'sqrt', 'log2'] and gbm having  'num_boost_round':85, 'max_depth':5 after the fine tuning with tune_kwargs having two number trails I got score of 0.46806

### If you were given more time with this dataset, where do you think you would spend more time?
I was given some more time I would have some more time in hyperparameter tuning and try to tune the model with different hyperparameter to finf out which performs well. 

### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.
|model|hpo1|hpo2|hpo3|score|
|--|--|--|--|--|
|initial|'default_vals'|'default_vals'|'default_vals'|1.79691|
|add_features|'default_vals'|'default_vals'|'default_vals'|0.67826|
|hpo|'n_estimators: 100,125,150'|'max_depth:5, 7, 10'|'num_boost_round:85'|0.46806|

### Create a line plot showing the top model score for the three (or more) training runs during the project.

TODO: Replace the image below with your own.

![model_train_score.png](Udacity-AI-ML-scholarship-project1/model_train_score.png)

### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.

TODO: Replace the image below with your own.

![model_test_score.png](Udacity-AI-ML-scholarship-project1/model_test_score.png)

## Summary
The first model that i trained was the initial model with not any features in it then i got a kaggle score of 1.796913 after that to improve the score i added a new feature to split up the datetime into year,month,day,hour and season and weather as datatype category i got the score of 0.67826 and after hyperparameter training and tuning i got my best score till now of 0.4
