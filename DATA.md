## Initial Exploration



Dataset consists of 26 columns with 205 entries. Fortunately there are no null values. Other than integer and float datatypes there are also object datatypes.

![c](https://raw.githubusercontent.com/sudheera96/badges/main/C.PNG)

- Maximum count of cars are 6. There are different companies in dataset.
- we did carnames in to groups and observed, these groups having different fuel tyes, prices etc, by comparing with all variables.Also there are different models

## Single Variant Analysis

- There are more cars with fuel type as gas

![](https://github.com/sudheera96/badges/blob/main/gas.PNG?raw=true)

- Most of cars havings 4 doors.

![](https://github.com/sudheera96/badges/blob/main/door.PNG?raw=true)

- Most of the car body is of sedan

![sedan](https://github.com/sudheera96/badges/blob/main/sedan.PNG?raw=true)

## Bivariant Analysis

- Prices are high in gas fuel type

![](https://github.com/sudheera96/badges/blob/main/fuel.PNG?raw=true)

- Prices are high in hardtop

![](https://github.com/sudheera96/badges/blob/main/hardtop.PNG?raw=true)

- Prices are high in rearwheel and front engine

![](https://github.com/sudheera96/badges/blob/main/engine.PNG?raw=true)

- Prices are high in ohcv engine type

![](https://github.com/sudheera96/badges/blob/main/havoc.PNG?raw=true)

## Categorical Data analysis

- Only car weight, car width, car height, car length are normally distributed

![](https://github.com/sudheera96/badges/blob/main/cat.PNG?raw=true)

## Intresting relationships
There is huge correlation between price and engine size and next price and car weight, car lenght, car weight, wheel base and boreratio.

But price and engine size are weekly correlated with highwaympg

![](https://github.com/sudheera96/badges/blob/main/Corr.PNG?raw=true)

## Features to predict
From heatmap we can observe that citympg, highwaympg, peakrmp, symboling and car Id are negatively correlated to price. So we can consider other features to predict.

## Creating dummies

There are non numercial variables, so we have to convert them to the numerical by creating dummies

After observing the correlation between the dummy variables and target variable(price) there few negative correlation variables and we have dropped them.

Those are: 

```python
columns=["cylindernumber_four","drivewheel_fwd","fuelsystem_2bbl","enginetype_ohc",
                                        "enginelocation_front","carbody_hatchback","aspiration_std","fuelsystem_1bbl",
                                        "fueltype_gas","cylindernumber_three","fuelsystem_spdi","drivewheel_4wd",
                                        "carbody_wagon","doornumber_two","fuelsystem_spfi","fuelsystem_4bbl",
                                        "enginetype_rotor","cylindernumber_two","fuelsystem_mfi"]
```


# Links:

## [initial_exploration.ipynb](https://github.com/44-599-MachineLearning-S21/project-machine-learning-s21-sudheera96/blob/main/initial_exploration.ipynb)

Initial exploration notebook have the information of dataset like its

- Dataypes
- Number of rows and columns
- Independent and dependent variabaes
- Relationship between independent and - dependent features
- Correlations
- Features to predict
- Traning and testing data set

## Dimensional Analysis

After applying PCA, we got 10 Principal Components. It’s interesting to see how much variance each principal component captures.

![](https://github.com/sudheera96/badges/blob/main/pca.PNG?raw=true)

The first 5 Principal Components are capturing around 80% of the variance so we can replace the 10 original features with the new 5 features having 80% of the information. So, we have reduced the 10 dimensions to only 5 dimensions while retaining most of the information.

![](https://github.com/sudheera96/badges/blob/main/var.PNG?raw=true)

So there 6 dimensions with varianace more than 95%, which is useful to bserve the clusters.

### Link

[Dimensional_analysis.ipynb](https://github.com/44-599-MachineLearning-S21/project-machine-learning-s21-sudheera96/blob/main/dimensional_analysis.ipynb)


