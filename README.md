# heartbeat-diagnosis-categorization
The goal of the problem is to predict the target variable, called condition.

It has only two unique associated values, so let's treat this a binary classification problem.

The dataset contains quite a lot of features to choose from for building our model(s) but we first need to investigate the dataset.

Bivariate histograms are split into several categories of similar similarity General patient,ECG,Blood,Pain related features, hue for both condition is compared.

ECG features whilst being important, don't seem like the only features that are needed to create a reasonable model for the prediction of target variable condition. The addition of more features will likely improve the model

The ECG feature model reached only a peak mean cross validation score of 0.72 using 10-fold CV

The addition of polynomial features didn't improve the model

Standard train_test_split resulted in a very similar training and test scores (0.74,0.72)

The standalone Blood Related Feature Model did slightly worse than the ECG model created earler

Optimal values of theta lie slightly higher than the previous model, whilst sigma was roughtly idential to the previous model.

An ensemble approach, using the ECG model output was used in the input of the Blood Related Model, which resulted in the highest model score up to now (0.76)
