## Conclusion And Future work

In conclusion, this study explored various methods in
feature selection like Correlation Coefficient,LASSO Regularization and Linear regression with outliners detection methods, Descison tree, Random forest, SVM with different kernals aiming to predict price from a
[car price prediction dataset](https://www.kaggle.com/hellbuoy/car-price-prediction) from kaggle. 

It shows that:

<input type="checkbox" disabled checked />[Elastic net regression](https://github.com/44-599-MachineLearning-S21/project-machine-learning-s21-sudheera96/blob/main/linear_regression.ipynb) works very well and feature coefficient values also performed good way.

<input type="checkbox" disabled checked />[SVM linear kernal](https://github.com/44-599-MachineLearning-S21/project-machine-learning-s21-sudheera96/blob/main/classification.ipynb) gave best accuracy than any other kernel.

<input type="checkbox" disabled checked />[PCA](https://github.com/44-599-MachineLearning-S21/project-machine-learning-s21-sudheera96/blob/main/Kmeans_with_pca.ipynb) provided two vairables with sum of variance ratio as 70% with root mean square error.

<input type="checkbox" disabled checked /> [Local outliner detector](https://github.com/44-599-MachineLearning-S21/project-machine-learning-s21-sudheera96/blob/main/anomalous_data.ipynb) provided 13 outliners which are not useful by giving low MAE value through linear regression.


### _So from above models we can observe that pricing dynamics of the new market in the different cars for business growth_

<input type="checkbox" disabled checked />Price of the car mostly depends upon engine size.

<input type="checkbox" disabled checked /> Stroke,dohcv, ohcv & 1 engine type, cylinders with 12,5 and 6, car weight,length and height, horsepower, sedan carbody, wheel base variables also come in factor for car prices.

<input type="checkbox" disabled checked />Mostly car wieght and engine size matter a lot for car pricing.

 
 On other hand it shows that
 
 <input type="checkbox" disabled /> [Random forest](https://github.com/44-599-MachineLearning-S21/project-machine-learning-s21-sudheera96/blob/main/RandomForest.ipynb), [descision tree](https://github.com/44-599-MachineLearning-S21/project-machine-learning-s21-sudheera96/blob/main/classification.ipynb) are overfitting.

<input type="checkbox" disabled /> none of outliners tells belongs to which variables.

<input type="checkbox" disabled />what are the causes of the outliners whether they are artificial or natural.

### _Future work need to focus on_

1. We plan to utilize Artificial Neural Networks to improve our prediction performance while avoiding overfitting. In addition to this, we shall tune Decision-Tree parameters like the number of trees, depth, etc. and sub-sample data points.

2. Also we need to do deep study on outliners.





 

