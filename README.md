# Credit Risk Analysis
## Overview
In this analysis, Python was utilized to use several supervised machine learning models to predict credit risk. In order to achieve this, the RandomOverSampler and SMOTE algorithms were used to oversample to data. Then, the ClusterCentriods algorithm was utilized to undersample the data. A combinatorial approach of over- and undersampling using the SMOTEENN algorithm was used. In order to reduce bias, we used two machine learning models (BalancedRandomForestClassifier and EasyEnsembleClassifier).
The purpose of this analysis is to evaluate the performance of both of these models and determine whether they should be used to predict credit risk or not. 

## Results

#### RandomOverSampler Model
![naive random 1](https://user-images.githubusercontent.com/79758494/128095540-7f37f69a-022c-4173-9a22-475fccd732d1.PNG)

![Naive random 2](https://user-images.githubusercontent.com/79758494/128095543-8a5620ad-42f5-4bad-975e-7c0a650bfd41.PNG)

The balanced accuracy score for the RandomOverSampler model is 65%. The precision is 100% for the low_risk population, with the recall being 69%. 

#### SMOTE Model
![smote 1](https://user-images.githubusercontent.com/79758494/128095571-1a2abe03-3aec-4064-8589-76e5b8ccde69.PNG)

![smote 2](https://user-images.githubusercontent.com/79758494/128095583-b6a69cc9-e6c0-4ab9-ac88-009276c60e6d.PNG)

Similarly to the RandomOverSampler model, the SMOTE Model has a balanced accuracy score of 66%. Again, the precision for the low_risk precision is 100% with recall being 69%. 

#### ClusterCentroids Model
![Undersampling 1](https://user-images.githubusercontent.com/79758494/128095599-93b7362f-dea0-4d79-bae1-0783a25c6d9f.PNG)

![undersampling 2](https://user-images.githubusercontent.com/79758494/128095610-1a697d79-038c-44a8-be07-71f97e0112ad.PNG)

The ClusterCentroids model, the balanced accuracy score is identical to that of the SMOTE model's balanced accuracy score. Again, the low_risk precision is at 100%, with a recall of 40%. 

#### SMOTEENN Model
![combonation 1](https://user-images.githubusercontent.com/79758494/128095619-8031f872-f9d4-4900-96f8-14f2aea14952.PNG)

![combonation 2](https://user-images.githubusercontent.com/79758494/128095629-74cf6182-5b44-4f87-a8a3-f0ab639979c4.PNG)

For the SMOTEENN Model, the balanced accuracy score dropped to 54%. Precision remains the same for both the low_risk and high_risk populations, while the average recall is at 58%. 

#### BalancedRandomForestClassifier Model
![Forest 1](https://user-images.githubusercontent.com/79758494/128095645-a2e0bd62-6ae0-485f-96ba-1fcb7c49f97b.PNG)

![forest 2](https://user-images.githubusercontent.com/79758494/128095651-19826a18-c1d5-43c2-a77e-da34898fab03.PNG)

The balanced accuracy score is around 78%. the high_risk precision is at 3%, with a 68% recall. The low_risk recall is at 88% with 100% precision. This could be attributed to a lower number of false positives. 

#### EasyEnsembleClassifier Model
![Adaboost 1](https://user-images.githubusercontent.com/79758494/128095661-66fe2f94-3b4e-4a47-9f92-7677e1369ea3.PNG)

![adaboost 2](https://user-images.githubusercontent.com/79758494/128095667-270529e1-d1b6-4597-a43c-4e3828d8c637.PNG)

With the EasyEnsembleClassifier model, the balanced accuracy score jumped to 93%. The high_risk precision score  is still fairly low at 9%, but with 92% recall. The low_risk precision is at 100% with a recall of 94%. This, again, can be attributed to a lower number of false positives. 

## Summary

All the models used to perform the credit risk analysis show weak precision in determining if a credit risk is high.  
The Ensemble models brought a lot more improvement specially on the sensitivity of the high risk credits.  
The EasyEnsembleClassifier model shows a recall of 92% so it detects almost all high risk credit. On another hand, with a low precision, a lot of low risk credits are still falsely detected as high risk. For these reasons I do not believe the bank should use any of these models to predict credit risk.
