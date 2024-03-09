# EXNO2DS
# AIM:
      To perform Exploratory Data Analysis on the given data set.
      
# EXPLANATION:
  The primary aim with exploratory analysis is to examine the data for distribution, outliers and anomalies to direct specific testing of your hypothesis.
  
# ALGORITHM:
STEP 1: Import the required packages to perform Data Cleansing,Removing Outliers and Exploratory Data Analysis.

STEP 2: Replace the null value using any one of the method from mode,median and mean based on the dataset available.

STEP 3: Use boxplot method to analyze the outliers of the given dataset.

STEP 4: Remove the outliers using Inter Quantile Range method.

STEP 5: Use Countplot method to analyze in a graphical method for categorical data.

STEP 6: Use displot method to represent the univariate distribution of data.

STEP 7: Use cross tabulation method to quantitatively analyze the relationship between multiple variables.

STEP 8: Use heatmap method of representation to show relationships between two variables, one plotted on each axis.

## CODING AND OUTPUT
```
  import pandas as pd
import numpy as np
import matplotlib.pyplot as pit
import seaborn as sns
dt=pd.read_csv("/content/titanic_dataset.csv")
```
### ![image](https://github.com/23007232/EXNO2DS/assets/139115574/93bce808-8530-4b96-b991-37d9f6f75e4d)
```
dt.info()
```
### ![image](https://github.com/23007232/EXNO2DS/assets/139115574/123cd5f1-9a1d-4877-a100-c1d6d9354f42)
```
dt.shape
```
### ![image](https://github.com/23007232/EXNO2DS/assets/139115574/b8fdbb5b-0044-42ab-a75c-eb5a88c66dde)
```
import pandas as pd
dt=pd.read_csv("/content/titanic_dataset.csv")
dt.set_index("PassengerId",inplace=True)
print(dt.set_index)
```
### ![image](https://github.com/23007232/EXNO2DS/assets/139115574/9113f5ff-f784-4c0e-9366-48beed907d8d)
```
dt.nunique()
```
### ![image](https://github.com/23007232/EXNO2DS/assets/139115574/077bb7c4-e85d-40d3-95be-744ca78023df)

```
dt["Survived"].value_counts()
```
### ![image](https://github.com/23007232/EXNO2DS/assets/139115574/8baf4dd9-bad8-4eeb-946b-8706ce36bdf6)
```
per=(dt["Survived"].value_counts()/dt.shape[0]*100).round(2)
per
```
### ![image](https://github.com/23007232/EXNO2DS/assets/139115574/9dd48d02-3fd1-4d35-9608-d580690fd696)
```
sns.countplot(data=dt,x="Survived")
```
### ![image](https://github.com/23007232/EXNO2DS/assets/139115574/19acdd7f-6495-4459-aeb3-5e2b6b788643)
```
dt
```
### ![image](https://github.com/23007232/EXNO2DS/assets/139115574/4834f0f1-2759-4969-966a-3f2e2ce61ef9)
```
dt.Pclass.unique()
```
### ![image](https://github.com/23007232/EXNO2DS/assets/139115574/9974f555-3840-44c9-be8b-b9b589c2b385)
```
import pandas as pd
dt=pd.read_csv("/content/titanic_dataset.csv")
dt.rename(columns = {'Sex':'Gender'},inplace = True)
dt
```
### ![image](https://github.com/23007232/EXNO2DS/assets/139115574/92281592-cf12-4ed1-a2cb-860e2e56c01d)
```
import seaborn as sns
dt=pd.read_csv("/content/titanic_dataset.csv")
sns.catplot(x="Sex",col="Survived",kind="count",data=dt,height=5,aspect=.7)
```
### ![image](https://github.com/23007232/EXNO2DS/assets/139115574/becc304f-bb0e-4b6e-a868-18e36e621bfa)
```
sns.catplot(x='Survived',hue="Sex",data=dt,kind="count")
```
### ![image](https://github.com/23007232/EXNO2DS/assets/139115574/9cee2dd8-2851-43b2-8c9b-21efe9d918cb)
```
dt.boxplot(column="Age",by="Survived")
```
### ![image](https://github.com/23007232/EXNO2DS/assets/139115574/915645f5-0175-4f49-8e53-a068156b42cb)
```
sns.scatterplot(x=dt["Age"],y=dt["Fare"])
```
### ![image](https://github.com/23007232/EXNO2DS/assets/139115574/19e18da3-0dfd-4130-8e00-b3259145c712)
```
import matplotlib.pyplot as plt
fig, ax1=plt.subplots(figsize=(8,5))
pt=sns.boxplot(ax=ax1,x='Pclass',y='Age',hue='Sex',data=dt)
```
### ![image](https://github.com/23007232/EXNO2DS/assets/139115574/baa9e2af-8a19-4ab8-bd2b-cd214877ae36)

```
sns.catplot(data=dt,col="Survived",x="Sex",hue="Pclass",kind="count")
```
### ![image](https://github.com/23007232/EXNO2DS/assets/139115574/1f67e781-6a53-4153-8535-eabd4ba5ac86)
```
#co-relation
import seaborn as sns
corr=dt.corr()
sns.heatmap(corr,annot=True)
```
### ![image](https://github.com/23007232/EXNO2DS/assets/139115574/79393259-2b76-4793-aea1-8ce59be77f6f)
```
sns.pairplot(dt)
```
### ![image](https://github.com/23007232/EXNO2DS/assets/139115574/d2e4d74b-50c4-438c-aed0-38ec5bbc692e)
    
# RESULT
      The Code is executed Successfully
