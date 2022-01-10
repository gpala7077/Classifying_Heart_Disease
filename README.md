# Classifying_Heart_Disease
An ML classification project aimed at classifying Heart Disease

# Summary of Results
A total of 42 different models were built around predicting heart disease in a patient. With a total of 11 unique
features that were composed of both categorical and continuous values. Two different data set samples were experimented
with, one using one-hot encoding for the categorical features and the other using Weight of Evidence transformation.
Each of the data samples were trained in three ways. First, by training the model using the default values. Second, by
performing a randomized search for hyper-parameters tuning; and lastly by performing feature selection.

## What are your findings?
All the models attained a test accuracy score between 82% - 86% and AUC values between 0.82 - 0.86. Shown below are the
summarized table of results for all the models trained. Data1 represents the data sample using one-hot encoding
transformation while Data2 represents the data sample using Weight of Evidence transformation. The 42 models were
trained between 7 different classifiers. Unfortunately there is not one model that truly outperforms the others as all
models achieved very similar scores with marginal improvements between each other. What stands out the most is how
balanced the models are in predicting either class. Nearly all cases were biased towards patients with heart disease.
Meaning, the model would most likely classify as having heart disease. This is due to the unbalanced nature of the data
where the split was around 55%/44% having and not having heart disease. Two of the most generalizable models were the
random forest classifier and XGBoost classifier. Those two models had the most balanced probability distributions and
had balanced metrics between classes. They did not have the highest accuracy or AUC such as Catboost, but they had the
most balanced performance metrics as shown by the F-1 scores, confusion matrices and probability distributions. The
highest performance model is the Catboost model trained on Data2, Weight of Evidence tranformation. However, as stated
before, it is biased towards heart disease. Since the results are only a marginal improvement over all the other models,
the final model would have to be either random forest or XGBoost due to their generalizability and efficiency. Additionally, experimenting between one-hot encoding and weight of evidence had marginally similar results where the dataset trained by the data sample transformed by weight of evidence performed better than one-hot encoding. In other words, transforming the categorical variables into weight of evidence enabled a marginally better more parsimonious model. Lastly,
another interesting finding between the models was the constant overlap between selected features during feature
selection. In nearly every case 3-5 features were consistently selected as important features using sequential feature
selection. It appears that sex, chest pain type, fasting blood sugar, old peak, and st slope, are important predictive
features in determining heart disease.
