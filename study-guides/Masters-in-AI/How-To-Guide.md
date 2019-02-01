# How To Guide

## Exploratory Data analysis (EDA) Phase

* Understand data
* Select feature(s)
* Run sample tests with various options, parameters and models types
* Execute large scale model training

## Definitions

* [Validations Assumptions and Identify Patterns](https://www.svds.com/value-exploratory-data-analysis/)

## Load dataset

* [Technical Notes and Common Operations](https://chrisalbon.com/)

```
# Import libraries
import numpy as np
from pandas import read_csv
import matplotlib.pyplot as plt

# Read data from file
dataframe = read_csv("dataset.csv")  # Option: header=None if the first row is containing data

# Show the first 5 rows
dataframe.head(5)

# Display number or rows and columns in set
dataframe.shape

# Display type of columns
dataframe.dtypes

# Display statistics of dataframe
#   Option: include='<types>' if needing to display statistics for only some data types
dataframe.describe(include='all')
```

```
# Extract comuns with only numerical data
numerical_columns = dataframe.describe().columns
print(numerical_columns)
```

```
# Extract comuns with only categorical data
categorical_columns = dataframe.select_dtypes(include=['category', object]).columns
print(categorical_columns)
```


## Create Plots

* [What plots?](https://towardsdatascience.com/what-plot-why-this-plot-and-why-not-9508a0cb35ea)
* [Visualisation using Pandas](https://machinelearningmastery.com/visualize-machine-learning-data-python-pandas/)
