# workshop-Multivariate-analysis
# AIM:
To Perform Multivariate Analysis

# ALGORITHM:
1.Read the given data

2.Get information from the data

3.Perform the Multivariate Analysis

4.Save the clean data to file

# PROGRAM:
```
Name:S.ESWARI

Regno:212221220012

import pandas as pd

import numpy as np

import seaborn as sns

import matplotlib.pyplot as plt

import io

from google.colab import files

uploaded = files.upload()

dd = pd.read_csv(io.BytesIO(uploaded['FlightInformation.csv.csv']))

print(dd)
```

# Types of bivariate:

# 1. Numerical & Numerical
```

sns.scatterplot (dd['Date_of_Journey'],dd['Dep_Time'])
```

![image](https://user-images.githubusercontent.com/127847210/229982679-a71c5805-dffd-4c47-a873-f0cafd090a26.png)

# 2. Numerical & Categorical
```

sns.barplot (x=dd['Duration'],y=dd['Price'])
```

![image](https://user-images.githubusercontent.com/127847210/229982817-a8e34691-e87a-4aa4-be17-31d89ac1ef64.png)

```
sns.barplot(x=dd["Arrival_Time"],y=dd["Price"],data=dd)
```

![image](https://user-images.githubusercontent.com/127847210/229982863-edb78985-3074-4563-a514-0df2cf1bce75.png)

```
states=dd.loc[:,["Duration","Price"]]

states=states.groupby(by=["Duration"]).sum().sort_values(by="Price")

sns.barplot(x=states.index,y="Price",data=states)

plt.xticks(rotation = 90)

plt.xlabel=("Duration")

plt.ylabel=("Price")

plt.show()
```

![image](https://user-images.githubusercontent.com/127847210/229984003-4ec3e98a-d2d2-4bfa-aa8b-62072fd84e66.png)

# Multivariate Analysis

```
dd.corr()

data = np.random.randint(low = 1, high = 100, size = (10, 10))

print("The data to be plotted:\n")

print(data)

hm = sns.heatmap(data = data)

plt.show()
```

![image](https://user-images.githubusercontent.com/127847210/229983165-a2d8c26d-dc97-4b49-b7d2-fb7a72b16af0.png)


# RESULT:

Thus, Bivariate/Multivariate Analysis is performed successfully.

