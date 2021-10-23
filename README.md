# Credit_Risk_Analysis
## Overview of the analysis:
Credit risk is very tough to predict. In this project we want to take a look at how all the factors in our loan_stats csv help predict whether someone is low or high risk status. One method that data scientists use for this type of issue is creating a model and then evaluate and train the models that they create. In this specific project we are using imbalanced-learn and scikit-learn libraries to build models and evalute them using a resampling method. In the first couple of models I oversampled the data using randomoversampler and smote algorithms and undersample the data with the clustercentroid algorithm. In the remaining models I used a combination approach to over and undersample the data using smoteenn. Finally, I compared two machine learning models that minimize bias, balancedrandomforestclassifier and easyensembleclassifier.

## Results:
* Naive Random Oversampling results: Our balanced accuracy test it 67%, the precision for the high_risk has a very low positivity at 1% and the recall is 74%

![image](https://user-images.githubusercontent.com/86137857/138539621-ab54b90f-1652-435c-8a99-6e05b4166f63.png)

* SMOTE oversampling results: the accuracy score is 66.2%, the precision for the high_risk loans has a low positvity again at 1% and recall is 69% overall

![image](https://user-images.githubusercontent.com/86137857/138539630-fc891d1e-3537-4921-b03a-a8eb3452af4f.png)

* Undersampling results: balanced accuracy score is 51.3% overall, the precision is at 99% and the recall is 42%

![image](https://user-images.githubusercontent.com/86137857/138539641-cbd25bd4-b29b-401b-b766-7db584787da4.png)

* Combination(over and undersampling) results: balanced accuracy score is 68.1% the precision is 99% and the recall is 60% overall

![image](https://user-images.githubusercontent.com/86137857/138539653-4ca8a129-5ca4-44d2-9247-6d3432bd0b5c.png)

* Balanced Random Forest Classifier results: the accuracy score is 64.81% the precision is 99% and the recall is 88%

![image](https://user-images.githubusercontent.com/86137857/138539769-bfe0095f-b32e-4b51-9f12-24c1402cc98c.png)

* Easy Ensemble AdaBoost Classifier results: the accuracy score is 92.2% the precision is 99% and the recall is 94%

![image](https://user-images.githubusercontent.com/86137857/138539779-99ba0b52-1f3b-4fa9-bbf6-8c9d43b1365a.png)

## Summary:
All the models used to perform the credit risk analysis show weak precision in determining if a credit risk is high. The Ensemble models brought a lot more improvment specially on the sensitivity of the high risk credits. The EasyEnsembleClassifier model shows a recall of 92% so it detects almost all high risk credit. On another hand, with a low precision, a lot of low risk credits are still falsely detected as high risk which would penalize the bank's credit strategy and infer on its revenue by missing those business opportunities. For those reasons I would not recommend the bank to use any of these models to predict credit risk.
