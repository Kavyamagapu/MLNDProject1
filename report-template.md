# Report: Predict Bike Sharing Demand with AutoGluon Solution
#### NAME HERE
Kavya Magapu

## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
TODO: Add your explanation

when i tried to submit the predictions, I realize that some predictions may be negative and kaggle won't accept that so I set the negative values to ZERO

### What was the top ranked model that performed?
TODO: Add your explanation
My top ranked model is Weighted_Ensemble_L3 with lowest root mean square error with the new feature added data. 

## Exploratory data analysis and feature creation
### What did the exploratory analysis find and how did you add additional features?
TODO: Add your explanation
I find some features were nearly normally distributed such as [temp, atemp, humidity, windspeed],some features were categorical such as [season, weather] it also seemed that the data was nearly uniformly distributed among the 4 seasons.

I followed the notebook suggestion of adding the hour feature to the data which seemed reasonable since it is a more general feature and might give the trained models more intuition to which hours of the day in general might have the largest bike share demand without specifying a certain year, month or day.

### How much better did your model preform after adding additional features and why do you think that is?
TODO: Add your explanation
After adding new feature, evaluation metric root mean square error changed from 53.09 to 30.87.I thought it is a good change.  

## Hyper parameter tuning
### How much better did your model preform after trying different hyper parameters?
TODO: Add your explanation
After performing hyperparameter optimization using the data with the added hour feature, the model's training rmse increased from 30.870803 to 30.870803. And I did not get how to additionally tune the parameters in order to improve the result.


### If you were given more time with this dataset, where do you think you would spend more time?
TODO: Add your explanation

I spend time to find and add new features as adding hour feature gives a better result and also transform the season column.

### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.

    model     timelimit      presets     hp-method            score
0  initial        600       'best_quality'    None            1.79255
1  add_features   600       'best_quality'    None            0.73429
2  hpo            600       'best_quality' hyper-parameters   0.54523

### Create a line plot showing the top model score for the three (or more) training runs during the project.

TODO: Replace the image below with your own.

![model_train_score.png](nd009t-c1-intro-to-ml-project-starter/model_train_score.png)

### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.

TODO: Replace the image below with your own.

![model_test_score.png](nd009t-c1-intro-to-ml-project-starter/model_test_score.png)

## Summary
TODO: Add your explanation

In summary, both EDA and feature engineering plays an important role in increasing the model accuracy and hyper parameter tuning works great when we find the best parameters by fine tuning them.
