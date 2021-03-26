
Model 1:

Using the R script provided, split and sample your DHS persons data and evaluate the AUC - ROC values you produce. Which "top_model" performed the best (had the largest AUC)? Are you able to use the feature selection penalty to tune your hyperparameter and remove any potentially irrelevant predictors? Provide justification for your selected penalty value? Finally, provide your ROC plots and interpret them. How effective is your penalized logistic regression model at predicting each of the five wealth outcomes.

The AUC curve for model 1 is below:

![lr_plot](https://user-images.githubusercontent.com/78227412/112562092-ef15b280-8dac-11eb-88d8-7ea4e73b91a2.png)

At the start the AUC begins to already slowly decrease before picking up speed around the 10th model.  After wards the decline begins to steeper before falling off a metaphorical cliff at the 23rd model where the penalty value was ~.025.  Therefore, we can assume that the predictors that are mostly irrelevant are gradually gone from the model from the first to the 21st models, then after the 21st the reason why the AUC drops off so steeply is because significant predictors were dropped.  Therefore, I am choosing the 9th model with the penalty value of ~.001 because afterward the dropoff steepens increasingly.  This means that the 9th model is one of the final ones with all or most of the significant predictors.

Model 1's ROC plot is below:

![lr_auc](https://user-images.githubusercontent.com/78227412/112562089-ede48580-8dac-11eb-9c1a-c3a04884711e.png)

From the above ouput it appears that the model handles wealth level 5 and 1 the best, with 5 having the edge.  However, when it comes to predicting wealth level 4 the model is rather mediocre, and it is rather abysmal at predicting welath levels 2 and 3. The model's Area under the Curve is ~.6


Model 2:  

Using the R script provided, set up your random forest model and produce the AUC - ROC values for the randomly selected predictors, and the minimal node size, again with wealth as the target. How did your random forest model fare when compared to the penalized logistic regression? Provide your ROC plots and interpret them. Are you able to provide a plot that supports the relative importance of each feature's contribution towards the predictive power of your random forest ensemble model?

When it comes to relative preformance between model 1 and 2, it is very similiar.  The values of the mean, ROC, AUC, and almost every other metric is practically the same.  Model 1 is arguably better because of the slight difference between Model 1's AUC is .62 while the AUC for model 2 is .61.  However, this is not a significant enough difference to matter in the end.

![lr_auc](https://user-images.githubusercontent.com/78227412/112562089-ede48580-8dac-11eb-9c1a-c3a04884711e.png)






Model 3:

Using the python script provided, train a logistic regression model using the tensorflow estimator API and your DHS data, again with wealth as the target. Apply the linear classifier to the feature columns and determine the accuracy, AUC and other evaluative metrics towards each of the different wealth outcomes. Then continue with your linear classifier adding the derived feature columns you have selected in order to extend capturing combinations of correlations (instead of learning on single model weights for each outcome). Again produce your ROC curves and interpret the results.

Model 3 is a logistic regression which utilizes gender, age, education, and family size to predict people's relative Wealth level.
Here are the evaluative metrics as they appear in python:

{'accuracy': 0.8678867, 'accuracy_baseline': 0.86151326, 'auc': 0.80184686, 'auc_precision_recall': 0.377051, 'average_loss': 0.31925312, 'label/mean': 0.13848676, 'loss': 0.31925312, 'precision': 0.58536583, 'prediction/mean': 0.14456409, 'recall': 0.15779093, 'global_step': 100}


Below is the ROC Curve for model 3:

![ROC_FIRST](https://user-images.githubusercontent.com/78227412/112573147-10cd6480-8dc2-11eb-822d-3f2cd5dffa03.png)

Below is for the predicted probabilities for model 3:

![pred-prob-first](https://user-images.githubusercontent.com/78227412/112562101-f6d55700-8dac-11eb-8f17-f25add592cca.png)

What the above 2 plots indicate is firstly, that most of the predicted values are heavily clustered towards the lower values.  This indicates that there was systematic overprediction for lower values.  Also, the ROC plot has an AUC of .78 according to evaluative metrics, which indicates that it is relatively better than random chance, which would have a value of ~.5.



Model 4:

Using the python script provided, train a gradient boosting model using decision trees with the tensorflow estimator. Provide evaluative metrics including a measure of accuracy and AUC. Produce the predicted probabilities plot as well as the ROC curve for each wealth outcome and interpret these results.

Below are the evaluation metrics reformatted for viewing pleasure:

accuracy	0.812676
accuracy_baseline	0.812676
auc	0.741234
auc_precision_recall	0.300026
average_loss	0.373733
label/mean	0.140112
loss	0.365871
precision	0.000000
prediction/mean	0.156752
recall	0.000000
global_step	100.000000

Below is the ROC Curve for model 4:

![ROC_Curve_Second_Script](https://user-images.githubusercontent.com/78227412/112562119-fd63ce80-8dac-11eb-9371-54fc5c11261e.png)

Below is for the predicted probabilities for model 4:

![pred-prob_second](https://user-images.githubusercontent.com/78227412/112562098-f50b9380-8dac-11eb-9820-9dcc0c9cd6cf.png)

The predicted porabilites shows that most of the values are more evenly spread out across the distribution than for model 3.  This indicates a probably more fair evaluation of the predicted values than for the previous model, which most likely overpredicted the lower values.  Also, for the ROC curve the AUC was .81, which was the highest out of any model I had, indicating that potentially this model would be the best as it's predictave power is significantly better than simple random chance.



Analyze all four models. According to the evaluation metrics, which model produced the best results? Were there any discrepancies among the five wealth outcomes from your DHS survey dataset?


The model that preformed the best was the final one, Model 4, the gradient boosting model using decision trees.  Its AUC was .81 which was higher than I expected for any of my models.

There were some discrepancies found.  For instance, it was best at predicting the extremes of the data, as in those with the lowest and highest relative wealth levels.  However, when it came to the middle brackets, it struggled to properly predict better than random chance.  Perhaps this indicates something within Ghana or even more generally that the middle wealth brackets are more non-homogenous groups than the extremes. of individuals who fall somewhere in the middle. This discrepancy in performance suggests that the Philippines may have very high income inequality, given that the lowest and highest income brackets seem to be so far from the middle brackets.


