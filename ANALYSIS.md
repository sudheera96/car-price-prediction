# Methodologies and Results

We utilized several classic and state-of-the-art methods, including ensemble learning techniques, with a 70-30 split on test and training data.

## 1. Linear Regression

Linear Regression model is used on dataset and evaluated the model with mean square error and R square and also improved the model performance by choosing other regressions like 
- Ridge Regression
- Lasso Regression
- Elastic Net Regression


| Learning Algorithm     | R Sqaure Value |
| ----------- | ----------- |
| Linear Regression     | 85%     |


- our R square is 85%, meaning, 85% variance of prices is explained by all the independent variables we have choosen.
- Also, there are few features with a high coefficient, meaning features having higher coeffiecients have better prices.

## Magnitude of coefficients

![](https://github.com/sudheera96/badges/blob/main/m.PNG?raw=true)

enginelocation_rear having highest coeffiect magnitude because of it we can say that our prices of car will be more by this feature. We use other regressions to overcome this problem.

### a. Ridge Regression

| Learning Algorithm     | R Sqaure Value | Alpha Value |
| ----------- | ----------- | ------ |
| Ridge Regression     | 82%     |0.75|
| Ridge Regression     | 81%     |1 |

![](https://github.com/sudheera96/badges/blob/main/z.PNG?raw=true)

If we increase the alpha value greater than 0.75 our magnitude of coeffiecients are reaching to zero also R sqaure is decreases which is not a good sight. so we fix for ridged resgression alpha value as 0.75

### b. Lasso regression

| Learning Algorithm     | R Sqaure Value | Alpha Value |
| ----------- | ----------- | ------ |
| Lasso Regression     | 86%     |5|

There is decrease in mse and increase r square value so it might be good model to use.

![](https://github.com/sudheera96/badges/blob/main/l.PNG?raw=true)

So as we increase alpha value few features coeffecients are going to zero which means it selecting few features as a feature selection so in ridge regression also we observed little bit in same manner but in lasso R square is increasing.

### c.Elastic Net Regression

| Learning Algorithm     | R Sqaure Value | Alpha Value |
| ----------- | ----------- | ------ |
| Elastic Net Regression     | 76%     |1|

![](https://github.com/sudheera96/badges/blob/main/e.PNG?raw=true)

Elestic net regression is working very well because mse value is decreased a lot and also R sqaure value decreased and feature coefficient values also performed good way rather than focusing only one one feature now most of the features of dataset are important.

### Link
[linear_regression](https://github.com/44-599-MachineLearning-S21/project-machine-learning-s21-sudheera96/blob/main/linear_regression.ipynb)

## 2. Decision Tree
```
Accuracy is  0.993006993006993
Precision is  0.9931113662456946
Sensitivity is  0.993006993006993
F1 is  0.9930065916405812
```
1. Total there are 28 nodes.
2. First split in the sample is [11, 66, 66]
3. Total leaf nodes are 14

![](https://raw.githubusercontent.com/44-599-MachineLearning-S21/project-machine-learning-s21-sudheera96/main/balance.png?token=AFK2ONMQJRB4GO7BL3ND6PTARA7GQ)

### 5 fold cross validation
```
Cross validation accuracies are:  [0.9310344827586207, 0.7931034482758621, 0.896551724137931, 0.8928571428571429, 0.8928571428571429]

Cross validation f1 scores  are:  [0.9312239484653277, 0.7931034482758621, 0.8927203065134101, 0.893015873015873, 0.8919704433497537]
```
These are good, but not quite as good as before. We definitely had overfitting occurring

## 3. SVM Classifier

### a. Linear

```
Cross validation accuracies are:  [0.7586206896551724, 0.7241379310344828, 0.7931034482758621, 0.8928571428571429, 0.8214285714285714]

Cross validation f1 scores  are:  [0.7255912273748184, 0.6735632183908047, 0.7632183908045976, 0.8869565217391305, 0.8068783068783069]
```

### b. RBF

```
Cross validation accuracies are:  [0.7586206896551724, 0.7241379310344828, 0.7931034482758621, 0.8928571428571429, 0.8214285714285714]

Cross validation f1 scores  are:  [0.7255912273748184, 0.6735632183908047, 0.7632183908045976, 0.8869565217391305, 0.8068783068783069]
```
### c. Polynomial

```
Cross validation accuracies are:  [0.7931034482758621, 0.7931034482758621, 0.8620689655172413, 0.8571428571428571, 0.8571428571428571]

Cross validation f1 scores  are:  [0.7863044605018445, 0.794088669950739, 0.860919540229885, 0.8498813014942047, 0.8571428571428571]
```
### Sigmoid

```
Cross validation accuracies are:  [0.7586206896551724, 0.7241379310344828, 0.7931034482758621, 0.8928571428571429, 0.8214285714285714]

Cross validation f1 scores  are:  [0.7255912273748184, 0.6735632183908047, 0.7632183908045976, 0.8869565217391305, 0.8068783068783069]
```
## Comparing the results
| Linear  |RBF   |Polynomial   |Sigmoid   |   |
|---|---|---|---|---|
| Accuracy is  0.9230769230769231|Accuracy is  0.7972027972027972|Accuracy is  0.8321678321678322|Accuracy is 0.20279720279720279|
|Precision is  0.9235617323852616|Precision is  0.8094985985674246|Precision is  0.8404354266423232|Precision is  0.14564777327935222|
|Sensitivity is  0.9230769230769231|Sensitivity is  0.797202797202797|Sensitivity is  0.8321678321678322|Sensitivity is  0.20279720279720279|
|F1 is  0.9228563567787569  |F1 is  0.7795675084883028|F1 is  0.8307458507275668|F1 is  0.16863228304875902|

Among all kernels Linear kernel having best results followed by polynomial kernel. Also in test evaluation linear and polynomial kernel gave best accuracy values.

So overall linear kernel SVM gave best accuracy values.

### Link
[classification.ipynb](https://github.com/44-599-MachineLearning-S21/project-machine-learning-s21-sudheera96/blob/main/classification.ipynb)

## 4. Random Forest

| Learning Algorithm     | R Sqaure Value train dataset | R square Value test data set |
| ----------- | ----------- | ------ |
| Random Forest    | 98%     |89%|

It's good but it's overfitting.

### Link
[RandomForest.ipynb](https://github.com/44-599-MachineLearning-S21/project-machine-learning-s21-sudheera96/blob/main/RandomForest.ipynb)

## 5. K means with PCA

There is a lot of variation in the magnitude of the data. Variables like wheelbase and carlength have high magnitude whereas variables like boreratio, stroke, compressionratio, etc. have a lower magnitude.

Since K-Means is a distance-based algorithm, this difference of magnitude can create a problem. So let’s first bring all the variables to the same magnitude.

![](https://github.com/sudheera96/badges/blob/main/k.PNG?raw=true)

from heat map we can observe carweight and enginsize are highly correlated with price because we are not using categorical variables in k means, because when we create dummies it won't create perfert clustering because of its distance based algorithm.

![](https://github.com/sudheera96/badges/blob/main/dimin.PNG?raw=true)

_Sum of pca explaine varience ratio is 70 %_

![](https://github.com/sudheera96/badges/blob/main/v.PNG?raw=true)

_Average Root Mean Square  0.1536220185004178_

![](https://github.com/sudheera96/badges/blob/main/Clust.PNG?raw=true)

I have applied dimensionality reduction since the data is more than 2 dimensional. I have taken number of clusters as 7 

### Link:

[Kmeans_with_pca.ipynb](https://github.com/44-599-MachineLearning-S21/project-machine-learning-s21-sudheera96/blob/main/Kmeans_with_pca.ipynb)

## 6. Linear Regression without anomalous data

Used detectors are :
- Isolation forest
- Elliptical envelope
- Local Outlier Factor
- One-Class SVM

| Learning Algorithm   with outliner detector  | Number of outliners | Mean absolute error |
| ----------- | ----------- | ------ |
| Linear Regresion with Isolation forest    | 14    |2498.619|
| Linear Regresion with Elliptical envelope   | 2   |2430.685|
| Linear Regresion with Local outliner Factor    | 13   |2159.432|
| Linear Regresion with one class SVM   | 0    |2609.678|

By comparing the MAE of linear regression with all outliners detection methods we got local outliner detector with low MAE with removal of 13 outliners. So we can say there are 13 outliners which are not useful.

### Link

[anomalous_data.ipynb](https://github.com/44-599-MachineLearning-S21/project-machine-learning-s21-sudheera96/blob/main/anomalous_data.ipynb)

## Challenges, limitations, Improvments
Finding outliners are tricky part  

### Things need to findout inthis project:

- Finding out what are those variables having the outliners.
- Finding to know whether the outliners univarient or multivarient.
- Able to understand what are the causes for the outliners like, is it artifical outliners or natural outliners.

By knowing above things we can do more things like
- Deleting observations
- Transforming and binning values
- Imputing
- Treat separately

We can improve our performace of dataset still by using neural networks.



























