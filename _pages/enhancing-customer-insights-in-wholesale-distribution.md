---
permalink: /projects/enhancing-customer-insights-in-wholesale-distribution
title: "Enhancing Customer Insights in Wholesale Distribution"
author_profile: true
---

**Supervisor:** Prof. Garg  
**Type:** Academic Project (Data Analysis, Machine Learning)

## Overview
This project, under the supervision of Prof. Garg, focused on analyzing the data of clients of a wholesale distributor. The goal was to describe the variation in the different types of customers by analyzing their annual spending across various product categories.

## Methodology
The methodology for the project included:
1. **Exploratory Data Analysis (EDA):** Conducting EDA and performing any necessary data cleaning.
2. **Feature Scaling:** Implementing and comparing MinMaxScaler and StandardScaler for data normalization, and selecting the most appropriate scaler.
3. **Optimal Feature Selection:** Using Recursive Feature Elimination with Cross-Validation (RFECV) to find the optimal number of features and plotting the relationship between the number of features selected and cross-validation score.
4. **KMeans Clustering:** Implementing KMeans Clustering for K values ranging from 2 to 15 and identifying the optimum number of clusters using the elbow method.
5. **Principal Component Analysis (PCA):** Conducting PCA with the original number of features to determine how much variance is explained by the first 2 and first 4 components, and visualizing the clusters.
6. **XGBoost Classifier Implementation:** Implementing an XGBoost Classifier with 5-Fold Cross-Validation and reporting the performance metrics.

## Evaluation
The project evaluation focused on:
- **Data Insights and Patterns:** Analyzing the patterns and insights derived from the EDA and feature scaling processes.
- **Clustering Analysis:** Assessing the effectiveness of the KMeans Clustering and PCA in grouping similar types of customers.
- **Model Performance:** Evaluating the performance of the XGBoost Classifier in terms of accuracy, precision, recall, and other relevant metrics.

## Key Findings
- Identified key spending patterns and customer segments from the wholesale distributor's client data.
- Determined the optimal number of customer clusters and visualized them effectively.
- Demonstrated the efficacy of the XGBoost Classifier in predicting customer categories based on their spending habits.

## Personal Contributions
- **Complete Project Implementation:** Led the entire project, including data analysis, feature scaling, clustering, PCA, and classifier implementation.
- **Data Cleaning and EDA:** Conducted thorough data cleaning and exploratory analysis to understand customer spending patterns.
- **Feature Scaling and Selection:** Implemented and compared different scaling techniques, and used RFECV for optimal feature selection.
- **Clustering and PCA:** Executed KMeans Clustering and PCA to uncover customer segments and visualized the results.
- **Classifier Development:** Developed and fine-tuned an XGBoost Classifier model, assessing its performance with cross-validation.

## Conclusion
The project successfully analyzed the wholesale distributor's customer data, providing valuable insights into customer behaviors and segmentation. The implementation of advanced data analysis techniques, such as clustering and machine learning classifiers, highlighted the potential of data-driven approaches in understanding customer dynamics in the wholesale industry.

## Project Jupyter Notebook
You can view the project's jupyter notebook via this [link](https://github.com/razaviah/Enhancing-Customer-Insights-in-Wholesale-Distribution/blob/main/Enhancing-Customer-Insights-in-Wholesale-Distribution.ipynb)

Or, you can view the text representation of it as follows:

# Enhancing Customer Insights in Wholesale Distribution

**Context**: The data set refers to clients of a wholesale distributor. It includes the annual spending in
monetary units on diverse product categories.

**Dataset Source**: "Wholesale customers data.csv"

**Task**: Goal of this project is to best describe the variation in the different types of customers that a
wholesale distributor interacts with.

**Implementation**:
- Perform EDA and any data cleaning if necessary.
- Implement Feature Scaling to Normalize the data(compare the histogram/KDE for MinMaxScaler
and StandardScaler). Choose one of the Scaler to proceed ahead and provide reasoning as to
why it was selected?
- Find optimal number of features using RFECV and show the plot between Number of features
selected vs Cross validation score (use channel as target variable)
- Implement KMeans Clustering for K=2 to K=15 and based on elbow method identify what is the
optimum number of clusters
- Implement PCA with number of original features to answer how much variance is explained by
first 2 components and by first 4 components and visualize the clusters in the data
- Implement XGBoost Classifier with 5 Fold CV and report the performance metrics

# Exploratory Data Analysis

## Reading the Data


```python
import matplotlib.pyplot as plt
import joblib
import pandas as pd
import numpy as np
import seaborn as sns
import warnings
warnings.filterwarnings("ignore", category=UserWarning)
warnings.filterwarnings("ignore", category=FutureWarning)
warnings.filterwarnings('ignore', category=DeprecationWarning)
from sklearn.model_selection import train_test_split, cross_val_score, GridSearchCV, learning_curve, cross_validate
from sklearn.ensemble import RandomForestClassifier, GradientBoostingClassifier
from sklearn.metrics import accuracy_score, precision_score, recall_score, make_scorer
from sklearn.linear_model import LogisticRegression, LinearRegression
from sklearn.neural_network import MLPClassifier
from sklearn.svm import SVC
from time import time

from sklearn.neighbors import KNeighborsClassifier
from sklearn.feature_selection import RFECV
from sklearn.cluster import KMeans
from sklearn.preprocessing import StandardScaler, MinMaxScaler
from sklearn.decomposition import PCA
from sklearn.model_selection import KFold
import sys

%matplotlib inline

customers = pd.read_csv('wholesale customers data.csv')
customers.head(5)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Channel</th>
      <th>Region</th>
      <th>Fresh</th>
      <th>Milk</th>
      <th>Grocery</th>
      <th>Frozen</th>
      <th>Detergents_Paper</th>
      <th>Delicassen</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>2</td>
      <td>3</td>
      <td>12669</td>
      <td>9656</td>
      <td>7561</td>
      <td>214</td>
      <td>2674</td>
      <td>1338</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>3</td>
      <td>7057</td>
      <td>9810</td>
      <td>9568</td>
      <td>1762</td>
      <td>3293</td>
      <td>1776</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2</td>
      <td>3</td>
      <td>6353</td>
      <td>8808</td>
      <td>7684</td>
      <td>2405</td>
      <td>3516</td>
      <td>7844</td>
    </tr>
    <tr>
      <th>3</th>
      <td>1</td>
      <td>3</td>
      <td>13265</td>
      <td>1196</td>
      <td>4221</td>
      <td>6404</td>
      <td>507</td>
      <td>1788</td>
    </tr>
    <tr>
      <th>4</th>
      <td>2</td>
      <td>3</td>
      <td>22615</td>
      <td>5410</td>
      <td>7198</td>
      <td>3915</td>
      <td>1777</td>
      <td>5185</td>
    </tr>
  </tbody>
</table>
</div>



## Exploring the Data

Description of features is as folllows:

-    FRESH : annual spending (m.u.) on fresh products (Continuous);
-    MILK : annual spending (m.u.) on milk products (Continuous);
-    GROCERY : annual spending (m.u.)on grocery products (Continuous);
-    FROZEN : annual spending (m.u.)on frozen products (Continuous);
-    DETERGENTS_PAPER : annual spending (m.u.) on detergents and paper products (Continuous);
-    DELICATESSEN : annual spending (m.u.)on and delicatessen products (Continuous);
-    CHANNEL : customers Channel - Hotel (Hotel/Restaurant/Cafe) or Retail channel (Categorical);
-    REGION : customers Region Lisnon, Oporto or Other (Categorical);

As we can see from the two tables below and the information provided in [this link](https://archive.ics.uci.edu/ml/datasets/wholesale+customers) about the dataset, there are two nominal variables and the rest of the variables are continuous. The two nominal features are `Channel` which is our target variable in this case, and `Region`. 


```python
customers.describe()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Channel</th>
      <th>Region</th>
      <th>Fresh</th>
      <th>Milk</th>
      <th>Grocery</th>
      <th>Frozen</th>
      <th>Detergents_Paper</th>
      <th>Delicassen</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>count</th>
      <td>440.000000</td>
      <td>440.000000</td>
      <td>440.000000</td>
      <td>440.000000</td>
      <td>440.000000</td>
      <td>440.000000</td>
      <td>440.000000</td>
      <td>440.000000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>1.322727</td>
      <td>2.543182</td>
      <td>12000.297727</td>
      <td>5796.265909</td>
      <td>7951.277273</td>
      <td>3071.931818</td>
      <td>2881.493182</td>
      <td>1524.870455</td>
    </tr>
    <tr>
      <th>std</th>
      <td>0.468052</td>
      <td>0.774272</td>
      <td>12647.328865</td>
      <td>7380.377175</td>
      <td>9503.162829</td>
      <td>4854.673333</td>
      <td>4767.854448</td>
      <td>2820.105937</td>
    </tr>
    <tr>
      <th>min</th>
      <td>1.000000</td>
      <td>1.000000</td>
      <td>3.000000</td>
      <td>55.000000</td>
      <td>3.000000</td>
      <td>25.000000</td>
      <td>3.000000</td>
      <td>3.000000</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>1.000000</td>
      <td>2.000000</td>
      <td>3127.750000</td>
      <td>1533.000000</td>
      <td>2153.000000</td>
      <td>742.250000</td>
      <td>256.750000</td>
      <td>408.250000</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>1.000000</td>
      <td>3.000000</td>
      <td>8504.000000</td>
      <td>3627.000000</td>
      <td>4755.500000</td>
      <td>1526.000000</td>
      <td>816.500000</td>
      <td>965.500000</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>2.000000</td>
      <td>3.000000</td>
      <td>16933.750000</td>
      <td>7190.250000</td>
      <td>10655.750000</td>
      <td>3554.250000</td>
      <td>3922.000000</td>
      <td>1820.250000</td>
    </tr>
    <tr>
      <th>max</th>
      <td>2.000000</td>
      <td>3.000000</td>
      <td>112151.000000</td>
      <td>73498.000000</td>
      <td>92780.000000</td>
      <td>60869.000000</td>
      <td>40827.000000</td>
      <td>47943.000000</td>
    </tr>
  </tbody>
</table>
</div>



Our dataset looks like complete as there are total of 440 rows and all the features have 440 values in them, therefore, does not need handling of missing variables. Also, all the features are represented in type of `int64`, so there is no need for converting our categorical features into numerical values as it is already done.


```python
customers.info()
```

    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 440 entries, 0 to 439
    Data columns (total 8 columns):
     #   Column            Non-Null Count  Dtype
    ---  ------            --------------  -----
     0   Channel           440 non-null    int64
     1   Region            440 non-null    int64
     2   Fresh             440 non-null    int64
     3   Milk              440 non-null    int64
     4   Grocery           440 non-null    int64
     5   Frozen            440 non-null    int64
     6   Detergents_Paper  440 non-null    int64
     7   Delicassen        440 non-null    int64
    dtypes: int64(8)
    memory usage: 27.6 KB


The data frames below show that, there are 3 possible values `(1, 2, 3)` for `Region` and 2 possible values `(1, 2)` for `Channel` in the dataset. This is mentioned to have a better understanding of what our dataset presents.

\
REGION Frequency and their representing nominal values:

> Lisbon 77 ---> 1\
> Oporto 47 ---> 2\
> Other Region 316 ---> 3\
> Total 440

\
CHANNEL Frequency and their representing nominal values:


> Horeca 298 ---> 1\
> Retail 142 ---> 2\
> Total 440 


```python
customers['Region'].value_counts()
```




    3    316
    1     77
    2     47
    Name: Region, dtype: int64




```python
customers['Channel'].value_counts()
```




    1    298
    2    142
    Name: Channel, dtype: int64



For the analysis on the data we convert the values we have in `Channel` to 0 and 1 as stated below:

> Horeca 298 ---> 1\
> Retail 142 ---> 0\
> Total 440


```python
channel_map = {2: 0, 1: 1}

customers['Channel'] = customers['Channel'].map(channel_map)
```

## Plotting data

As we can see below there are clearly some outliers in our dataset which we need to handle as the outliers do not represent our actual dataset. Also there is no clear pattern between the features and the `Channel` feature which is our target variable.


```python
customers.plot(figsize=(18,9), style='.');
```


    
![png](./../images/enhancing-customer-insights-in-wholesale-distribution/output_18_0.png)
   



```python
fig = plt.figure(figsize = (15,8))
customers_cont = customers.drop(['Channel', 'Region'], axis=1)
customers_cont.boxplot(grid=False)
```




    <AxesSubplot:>




    
![png](./../images/enhancing-customer-insights-in-wholesale-distribution/output_19_1.png)
    


**boxplot** considers **Q3 + 1.5 IQR** as its `upper bound` and **Q1 - 1.5 IQR**  as its `lower bound`. Anything greater than `upper bound` and smaller than `lower bound` would be considered as outlier and we delete them as the outliers might cause the models not to perform at their best.


```python
df = customers.copy()

Q1 = df.quantile(0.25)
Q3 = df.quantile(0.75)
IQR = Q3 - Q1

# This part of the code is taken from StackOverflow
df = df[~((df < (Q1 - 1.5 * IQR)) |(df > (Q3 + 1.5 * IQR))).any(axis=1)]

print("Number of outliers detected %d" % (len(customers) - len(df)))
print("Proportion of outliers to the whole dataset is %f" % ((len(customers) - len(df))/len(customers)))
    

```

    Number of outliers detected 108
    Proportion of outliers to the whole dataset is 0.245455


As the number of outliers detected in total are more than 20% of our dataset, then not dropping them would be more reasonable and we will try feature engineering to reduce the effects of the outliers.


```python
sns.heatmap(customers.corr())
```




    <AxesSubplot:>




    
![png](./../images/enhancing-customer-insights-in-wholesale-distribution/output_23_1.png)
    


As we can see from our correlation table the some of the independent features represent a hight correlation that needs to be resolved as high correlations between the independent variables result in multicollinearity and it may cause overfitting.

The other features that have high correlation between them are:
1. `Grocery` and `Detergents_Paper` have correlation of **0.924641**
2. `Grocery` and `Milk` have correlation of **0.728335**
3. `Milk` and `Detergents_Paper` have correlation of **0.661816**



```python
(customers.corr()).style.background_gradient(cmap='coolwarm')
```




<style type="text/css">
#T_8d7ec_row0_col0, #T_8d7ec_row1_col1, #T_8d7ec_row2_col2, #T_8d7ec_row3_col3, #T_8d7ec_row4_col4, #T_8d7ec_row5_col5, #T_8d7ec_row6_col6, #T_8d7ec_row7_col7 {
  background-color: #b40426;
  color: #f1f1f1;
}
#T_8d7ec_row0_col1, #T_8d7ec_row0_col3, #T_8d7ec_row0_col4, #T_8d7ec_row0_col6, #T_8d7ec_row0_col7, #T_8d7ec_row6_col0, #T_8d7ec_row6_col2, #T_8d7ec_row6_col5 {
  background-color: #3b4cc0;
  color: #f1f1f1;
}
#T_8d7ec_row0_col2 {
  background-color: #8badfd;
  color: #000000;
}
#T_8d7ec_row0_col5 {
  background-color: #9dbdff;
  color: #000000;
}
#T_8d7ec_row1_col0 {
  background-color: #afcafc;
  color: #000000;
}
#T_8d7ec_row1_col2 {
  background-color: #6788ee;
  color: #f1f1f1;
}
#T_8d7ec_row1_col3 {
  background-color: #abc8fd;
  color: #000000;
}
#T_8d7ec_row1_col4, #T_8d7ec_row2_col3 {
  background-color: #bbd1f8;
  color: #000000;
}
#T_8d7ec_row1_col5, #T_8d7ec_row1_col7 {
  background-color: #5875e1;
  color: #f1f1f1;
}
#T_8d7ec_row1_col6 {
  background-color: #bcd2f7;
  color: #000000;
}
#T_8d7ec_row2_col0 {
  background-color: #dadce0;
  color: #000000;
}
#T_8d7ec_row2_col1 {
  background-color: #5d7ce6;
  color: #f1f1f1;
}
#T_8d7ec_row2_col4 {
  background-color: #b6cefa;
  color: #000000;
}
#T_8d7ec_row2_col5, #T_8d7ec_row5_col7 {
  background-color: #c7d7f0;
  color: #000000;
}
#T_8d7ec_row2_col6 {
  background-color: #a7c5fe;
  color: #000000;
}
#T_8d7ec_row2_col7 {
  background-color: #98b9ff;
  color: #000000;
}
#T_8d7ec_row3_col0 {
  background-color: #5b7ae5;
  color: #f1f1f1;
}
#T_8d7ec_row3_col1 {
  background-color: #5572df;
  color: #f1f1f1;
}
#T_8d7ec_row3_col2 {
  background-color: #7699f6;
  color: #f1f1f1;
}
#T_8d7ec_row3_col4 {
  background-color: #e8765c;
  color: #f1f1f1;
}
#T_8d7ec_row3_col5 {
  background-color: #84a7fc;
  color: #f1f1f1;
}
#T_8d7ec_row3_col6 {
  background-color: #ee8669;
  color: #f1f1f1;
}
#T_8d7ec_row3_col7 {
  background-color: #ccd9ed;
  color: #000000;
}
#T_8d7ec_row4_col0 {
  background-color: #3f53c6;
  color: #f1f1f1;
}
#T_8d7ec_row4_col1 {
  background-color: #4e68d8;
  color: #f1f1f1;
}
#T_8d7ec_row4_col2, #T_8d7ec_row4_col5 {
  background-color: #536edd;
  color: #f1f1f1;
}
#T_8d7ec_row4_col3 {
  background-color: #eb7d62;
  color: #f1f1f1;
}
#T_8d7ec_row4_col6, #T_8d7ec_row6_col4 {
  background-color: #c43032;
  color: #f1f1f1;
}
#T_8d7ec_row4_col7 {
  background-color: #8caffe;
  color: #000000;
}
#T_8d7ec_row5_col0 {
  background-color: #e0dbd8;
  color: #000000;
}
#T_8d7ec_row5_col1 {
  background-color: #455cce;
  color: #f1f1f1;
}
#T_8d7ec_row5_col2 {
  background-color: #c3d5f4;
  color: #000000;
}
#T_8d7ec_row5_col3 {
  background-color: #c0d4f5;
  color: #000000;
}
#T_8d7ec_row5_col4, #T_8d7ec_row7_col0 {
  background-color: #b1cbfc;
  color: #000000;
}
#T_8d7ec_row5_col6 {
  background-color: #a1c0ff;
  color: #000000;
}
#T_8d7ec_row6_col1 {
  background-color: #4b64d5;
  color: #f1f1f1;
}
#T_8d7ec_row6_col3 {
  background-color: #f29274;
  color: #f1f1f1;
}
#T_8d7ec_row6_col7 {
  background-color: #5f7fe8;
  color: #f1f1f1;
}
#T_8d7ec_row7_col1 {
  background-color: #5977e3;
  color: #f1f1f1;
}
#T_8d7ec_row7_col2 {
  background-color: #a3c2fe;
  color: #000000;
}
#T_8d7ec_row7_col3 {
  background-color: #f1cdba;
  color: #000000;
}
#T_8d7ec_row7_col4 {
  background-color: #dedcdb;
  color: #000000;
}
#T_8d7ec_row7_col5 {
  background-color: #d3dbe7;
  color: #000000;
}
#T_8d7ec_row7_col6 {
  background-color: #cad8ef;
  color: #000000;
}
</style>
<table id="T_8d7ec_">
  <thead>
    <tr>
      <th class="blank level0" >&nbsp;</th>
      <th class="col_heading level0 col0" >Channel</th>
      <th class="col_heading level0 col1" >Region</th>
      <th class="col_heading level0 col2" >Fresh</th>
      <th class="col_heading level0 col3" >Milk</th>
      <th class="col_heading level0 col4" >Grocery</th>
      <th class="col_heading level0 col5" >Frozen</th>
      <th class="col_heading level0 col6" >Detergents_Paper</th>
      <th class="col_heading level0 col7" >Delicassen</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th id="T_8d7ec_level0_row0" class="row_heading level0 row0" >Channel</th>
      <td id="T_8d7ec_row0_col0" class="data row0 col0" >1.000000</td>
      <td id="T_8d7ec_row0_col1" class="data row0 col1" >-0.062028</td>
      <td id="T_8d7ec_row0_col2" class="data row0 col2" >0.169172</td>
      <td id="T_8d7ec_row0_col3" class="data row0 col3" >-0.460720</td>
      <td id="T_8d7ec_row0_col4" class="data row0 col4" >-0.608792</td>
      <td id="T_8d7ec_row0_col5" class="data row0 col5" >0.202046</td>
      <td id="T_8d7ec_row0_col6" class="data row0 col6" >-0.636026</td>
      <td id="T_8d7ec_row0_col7" class="data row0 col7" >-0.056011</td>
    </tr>
    <tr>
      <th id="T_8d7ec_level0_row1" class="row_heading level0 row1" >Region</th>
      <td id="T_8d7ec_row1_col0" class="data row1 col0" >-0.062028</td>
      <td id="T_8d7ec_row1_col1" class="data row1 col1" >1.000000</td>
      <td id="T_8d7ec_row1_col2" class="data row1 col2" >0.055287</td>
      <td id="T_8d7ec_row1_col3" class="data row1 col3" >0.032288</td>
      <td id="T_8d7ec_row1_col4" class="data row1 col4" >0.007696</td>
      <td id="T_8d7ec_row1_col5" class="data row1 col5" >-0.021044</td>
      <td id="T_8d7ec_row1_col6" class="data row1 col6" >-0.001483</td>
      <td id="T_8d7ec_row1_col7" class="data row1 col7" >0.045212</td>
    </tr>
    <tr>
      <th id="T_8d7ec_level0_row2" class="row_heading level0 row2" >Fresh</th>
      <td id="T_8d7ec_row2_col0" class="data row2 col0" >0.169172</td>
      <td id="T_8d7ec_row2_col1" class="data row2 col1" >0.055287</td>
      <td id="T_8d7ec_row2_col2" class="data row2 col2" >1.000000</td>
      <td id="T_8d7ec_row2_col3" class="data row2 col3" >0.100510</td>
      <td id="T_8d7ec_row2_col4" class="data row2 col4" >-0.011854</td>
      <td id="T_8d7ec_row2_col5" class="data row2 col5" >0.345881</td>
      <td id="T_8d7ec_row2_col6" class="data row2 col6" >-0.101953</td>
      <td id="T_8d7ec_row2_col7" class="data row2 col7" >0.244690</td>
    </tr>
    <tr>
      <th id="T_8d7ec_level0_row3" class="row_heading level0 row3" >Milk</th>
      <td id="T_8d7ec_row3_col0" class="data row3 col0" >-0.460720</td>
      <td id="T_8d7ec_row3_col1" class="data row3 col1" >0.032288</td>
      <td id="T_8d7ec_row3_col2" class="data row3 col2" >0.100510</td>
      <td id="T_8d7ec_row3_col3" class="data row3 col3" >1.000000</td>
      <td id="T_8d7ec_row3_col4" class="data row3 col4" >0.728335</td>
      <td id="T_8d7ec_row3_col5" class="data row3 col5" >0.123994</td>
      <td id="T_8d7ec_row3_col6" class="data row3 col6" >0.661816</td>
      <td id="T_8d7ec_row3_col7" class="data row3 col7" >0.406368</td>
    </tr>
    <tr>
      <th id="T_8d7ec_level0_row4" class="row_heading level0 row4" >Grocery</th>
      <td id="T_8d7ec_row4_col0" class="data row4 col0" >-0.608792</td>
      <td id="T_8d7ec_row4_col1" class="data row4 col1" >0.007696</td>
      <td id="T_8d7ec_row4_col2" class="data row4 col2" >-0.011854</td>
      <td id="T_8d7ec_row4_col3" class="data row4 col3" >0.728335</td>
      <td id="T_8d7ec_row4_col4" class="data row4 col4" >1.000000</td>
      <td id="T_8d7ec_row4_col5" class="data row4 col5" >-0.040193</td>
      <td id="T_8d7ec_row4_col6" class="data row4 col6" >0.924641</td>
      <td id="T_8d7ec_row4_col7" class="data row4 col7" >0.205497</td>
    </tr>
    <tr>
      <th id="T_8d7ec_level0_row5" class="row_heading level0 row5" >Frozen</th>
      <td id="T_8d7ec_row5_col0" class="data row5 col0" >0.202046</td>
      <td id="T_8d7ec_row5_col1" class="data row5 col1" >-0.021044</td>
      <td id="T_8d7ec_row5_col2" class="data row5 col2" >0.345881</td>
      <td id="T_8d7ec_row5_col3" class="data row5 col3" >0.123994</td>
      <td id="T_8d7ec_row5_col4" class="data row5 col4" >-0.040193</td>
      <td id="T_8d7ec_row5_col5" class="data row5 col5" >1.000000</td>
      <td id="T_8d7ec_row5_col6" class="data row5 col6" >-0.131525</td>
      <td id="T_8d7ec_row5_col7" class="data row5 col7" >0.390947</td>
    </tr>
    <tr>
      <th id="T_8d7ec_level0_row6" class="row_heading level0 row6" >Detergents_Paper</th>
      <td id="T_8d7ec_row6_col0" class="data row6 col0" >-0.636026</td>
      <td id="T_8d7ec_row6_col1" class="data row6 col1" >-0.001483</td>
      <td id="T_8d7ec_row6_col2" class="data row6 col2" >-0.101953</td>
      <td id="T_8d7ec_row6_col3" class="data row6 col3" >0.661816</td>
      <td id="T_8d7ec_row6_col4" class="data row6 col4" >0.924641</td>
      <td id="T_8d7ec_row6_col5" class="data row6 col5" >-0.131525</td>
      <td id="T_8d7ec_row6_col6" class="data row6 col6" >1.000000</td>
      <td id="T_8d7ec_row6_col7" class="data row6 col7" >0.069291</td>
    </tr>
    <tr>
      <th id="T_8d7ec_level0_row7" class="row_heading level0 row7" >Delicassen</th>
      <td id="T_8d7ec_row7_col0" class="data row7 col0" >-0.056011</td>
      <td id="T_8d7ec_row7_col1" class="data row7 col1" >0.045212</td>
      <td id="T_8d7ec_row7_col2" class="data row7 col2" >0.244690</td>
      <td id="T_8d7ec_row7_col3" class="data row7 col3" >0.406368</td>
      <td id="T_8d7ec_row7_col4" class="data row7 col4" >0.205497</td>
      <td id="T_8d7ec_row7_col5" class="data row7 col5" >0.390947</td>
      <td id="T_8d7ec_row7_col6" class="data row7 col6" >0.069291</td>
      <td id="T_8d7ec_row7_col7" class="data row7 col7" >1.000000</td>
    </tr>
  </tbody>
</table>




Below is a complete plot of, plots of different features of the dataset. As it can be seen from below, the attributes overlap most of the time but, for example, `Fresh` vs `Detergents_Paper` plot, they are some what distinctable. Based on the plots below we can say, our model will have a good chance of predicting the `Channel` of the wholesale customers correctly by taking into account different features at the same time.


```python
sns.pairplot(customers,hue="Channel")
plt.show()
```


    
![png](./../images/enhancing-customer-insights-in-wholesale-distribution/output_27_0.png)
    


The plots below give us additional insights around the dataset we have. The 6 plots below are the overlaid histograms for `Fresh`, `Milk`, `Grocery`, `Frozen`, `Detergents_Paper`, `Delicassen`. The histograms show the distribution for the two `Channel` based on their `Grocery` value, for example. As we can see from the below plots, most of the purchases in both `Channel`s have low values and there are only some with high values. The Overlaid histograms show that the `Retail (Channel 0)` has mostly bigger values compared to `Horeca (Channel 1)` but they also overlap most of them time.


```python
for i in ['Fresh', 'Milk', 'Grocery', 'Frozen', 'Detergents_Paper', 'Delicassen']:
    channel1 = list(customers[customers['Channel'] == 1][i])
    channel0 = list(customers[customers['Channel'] == 0][i])
    xmin = min(min(channel1), min(channel0))
    xmax = max(max(channel1), max(channel0))
    width = (xmax - xmin) / 40
    sns.distplot(channel1, color='g', kde=False, bins=np.arange(xmin, xmax, width))
    sns.distplot(channel0, color='b', kde=False, bins=np.arange(xmin, xmax, width))
    plt.legend(['Horeca (Channel 1)', 'Retail (Channel 0)'])
    plt.title('Overlaid histogram for {}'.format(i))
    plt.show()
```


    
![png](./../images/enhancing-customer-insights-in-wholesale-distribution/output_29_0.png)
    



    
![png](./../images/enhancing-customer-insights-in-wholesale-distribution/output_29_1.png)
    



    
![png](./../images/enhancing-customer-insights-in-wholesale-distribution/output_29_2.png)
    



    
![png](./../images/enhancing-customer-insights-in-wholesale-distribution/output_29_3.png)
    



    
![png](./../images/enhancing-customer-insights-in-wholesale-distribution/output_29_4.png)
    



    
![png](./../images/enhancing-customer-insights-in-wholesale-distribution/output_29_5.png)
    


# Feature Scaling

Feature Scaling converts our original data to a scalable version of it in a way that features do not lose their values and each one of the features have same importance as the rest of the features. Some of the data in our dataset have larger values than others so by using feature scaling we try to eliminate any effects that would cause from the magnitude of values.

We implement both `Standard Scalar Method` and `MinMax Scalar Method` to see which one performs better on our dataset and apply it.


```python
customers.drop(['Channel', 'Region'], axis=1).plot(kind='kde')
```




    <AxesSubplot:ylabel='Density'>




    
![png](./../images/enhancing-customer-insights-in-wholesale-distribution/output_32_1.png)
    



```python
customers.drop(['Channel', 'Region'], axis=1).plot(kind='hist', bins=300)
```




    <AxesSubplot:ylabel='Frequency'>




    
![png](./../images/enhancing-customer-insights-in-wholesale-distribution/output_33_1.png)
    


## Standard Scalar Method

Standard Scalar Method basically changes the values of data in our dataset to have mean value of 0 and standard deviation of 1. The formula used to achieve this goal is `y = (x-mean)/std`


```python
# First we make a copy of our dataset so we would not accidentally change our original dataset
# Also we only scale the features which are continuous
df1 = customers.drop(['Channel', 'Region'], axis=1)

standardScale = StandardScaler().fit_transform(df1)

standardScale_df = pd.DataFrame(standardScale, columns=df1.columns)

standardScale_df.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Fresh</th>
      <th>Milk</th>
      <th>Grocery</th>
      <th>Frozen</th>
      <th>Detergents_Paper</th>
      <th>Delicassen</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0.052933</td>
      <td>0.523568</td>
      <td>-0.041115</td>
      <td>-0.589367</td>
      <td>-0.043569</td>
      <td>-0.066339</td>
    </tr>
    <tr>
      <th>1</th>
      <td>-0.391302</td>
      <td>0.544458</td>
      <td>0.170318</td>
      <td>-0.270136</td>
      <td>0.086407</td>
      <td>0.089151</td>
    </tr>
    <tr>
      <th>2</th>
      <td>-0.447029</td>
      <td>0.408538</td>
      <td>-0.028157</td>
      <td>-0.137536</td>
      <td>0.133232</td>
      <td>2.243293</td>
    </tr>
    <tr>
      <th>3</th>
      <td>0.100111</td>
      <td>-0.624020</td>
      <td>-0.392977</td>
      <td>0.687144</td>
      <td>-0.498588</td>
      <td>0.093411</td>
    </tr>
    <tr>
      <th>4</th>
      <td>0.840239</td>
      <td>-0.052396</td>
      <td>-0.079356</td>
      <td>0.173859</td>
      <td>-0.231918</td>
      <td>1.299347</td>
    </tr>
  </tbody>
</table>
</div>




```python
standardScale_df.plot(kind='kde')
```




    <AxesSubplot:ylabel='Density'>




    
![png](./../images/enhancing-customer-insights-in-wholesale-distribution/output_37_1.png)
    



```python
standardScale_df.plot(kind='hist', bins=300)
```




    <AxesSubplot:ylabel='Frequency'>




    
![png](./../images/enhancing-customer-insights-in-wholesale-distribution/output_38_1.png)
    


The Standard Scalar Method did a pretty good job with feature scaling as can be seen clearly from the `kde` plot. It has converted the data we originally had to a dataset where all the data have almost the same range as other features and this would make the prediction easier for the models.

## MinMax Scalar Method

MinMax Scalar Method changes the data in our dataset to be in range of [0,1] by using the normalization formula: `y = (x-min)/(max-min)`


```python
# First we make a copy of our dataset so we would not accidentally change our original dataset
# Also we only scale the features which are continuous
df2 = customers.drop(['Channel', 'Region'], axis=1)

minMaxScale = MinMaxScaler().fit_transform(df2)

minMaxScale_df = pd.DataFrame(minMaxScale,columns=df2.columns)

minMaxScale_df.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Fresh</th>
      <th>Milk</th>
      <th>Grocery</th>
      <th>Frozen</th>
      <th>Detergents_Paper</th>
      <th>Delicassen</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0.112940</td>
      <td>0.130727</td>
      <td>0.081464</td>
      <td>0.003106</td>
      <td>0.065427</td>
      <td>0.027847</td>
    </tr>
    <tr>
      <th>1</th>
      <td>0.062899</td>
      <td>0.132824</td>
      <td>0.103097</td>
      <td>0.028548</td>
      <td>0.080590</td>
      <td>0.036984</td>
    </tr>
    <tr>
      <th>2</th>
      <td>0.056622</td>
      <td>0.119181</td>
      <td>0.082790</td>
      <td>0.039116</td>
      <td>0.086052</td>
      <td>0.163559</td>
    </tr>
    <tr>
      <th>3</th>
      <td>0.118254</td>
      <td>0.015536</td>
      <td>0.045464</td>
      <td>0.104842</td>
      <td>0.012346</td>
      <td>0.037234</td>
    </tr>
    <tr>
      <th>4</th>
      <td>0.201626</td>
      <td>0.072914</td>
      <td>0.077552</td>
      <td>0.063934</td>
      <td>0.043455</td>
      <td>0.108093</td>
    </tr>
  </tbody>
</table>
</div>




```python
minMaxScale_df.plot(kind='kde')
```




    <AxesSubplot:ylabel='Density'>




    
![png](./../images/enhancing-customer-insights-in-wholesale-distribution/output_43_1.png)
    



```python
minMaxScale_df.plot(kind='hist', bins=300)
```




    <AxesSubplot:ylabel='Frequency'>




    
![png](./../images/enhancing-customer-insights-in-wholesale-distribution/output_44_1.png)
    


The MinMax Scalar Method also did pretty well with feature scaling as can be seen clearly from the plots above. It has converted the data we originally had to a dataset where all the data have the range of [0,1] as other features and this would make the prediction easier for the models.

## Comparison Between the Standard and MinMax Scalar Methods

As it can be seen from the graphs, both of the Standard and MinMax Scalar methods did well with scaling the data but Standard Scalar Method did better. By looking at the `kde` graphs, we can see that the density of different features in the scaled version using MinMax Scalar Method differs more than the densities in scaled version using Standard Scalar Method which could cause the model to have biased prediction. For this reason we choose Standard Scalar Method to as our Feature Scaling method.


```python
scaledDf = standardScale_df
```

# RFECV

We use the scaled features which we obtained by feature engineering for the RFECV. To use it, the `Region` has to be added to our X values and consider `Channel` as our target variable.


```python
scaledDf['Region'] = customers['Region']
X = scaledDf
y = customers['Channel']



X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=7)
```


```python
rfecv = RFECV(estimator=RandomForestClassifier())
rfecv.fit(X, y)

# Plot number of features VS. cross-validation scores
plt.xlabel("Number of Features Selected")
plt.ylabel("Cross-Validation Score")
plt.plot(range(1, len(rfecv.grid_scores_) + 1), rfecv.grid_scores_)
plt.title("Optimal number of features : %d" % rfecv.n_features_)
plt.show()

print("The features are as follows: ", scaledDf.columns[rfecv.support_].tolist())
```


    
![png](./../images/enhancing-customer-insights-in-wholesale-distribution/output_52_0.png)
    


    The features are as follows:  ['Fresh', 'Milk', 'Grocery', 'Frozen', 'Detergents_Paper', 'Delicassen']


As we can see in the above cell, the optimal number of features is 6 and the features are `Fresh`, `Milk`, `Grocery`, `Frozen`, `Detergents_Paper`, and `Delicassen`.

# KMeans Clustering

For this part we first implement the KMeans Clustering for K=2 to K=15 and then by using the elbow method we identify the optimum number of clusters.


```python
inertias = []
for i in range(2, 16):
    kmeans = KMeans(n_clusters = i, random_state = 7)
    kmeans.fit(scaledDf)
    inertias.append(kmeans.inertia_)
    cluster_labels = kmeans.labels_
plt.plot(range(2, 16), inertias)
plt.title('The Elbow Method')
plt.xlabel('Number of clusters')
plt.ylabel('Inertia')
plt.show()
```


    
![png](./../images/enhancing-customer-insights-in-wholesale-distribution/output_56_0.png)
    


By using Elbow Method, the optimum number of clusters would be 7.


```python
kmeans = KMeans(n_clusters = 7,random_state = 7).fit(scaledDf)
print("Inertia: ", kmeans.inertia_)
print("The centroids coordinates are as follows: ")
for i in range(0,7):
    print("\tCentroid number %d: " % (i+1), end='\n\t')
    print(kmeans.cluster_centers_[i], end='\n\n')
```

    Inertia:  1014.3680859892069
    The centroids coordinates are as follows: 
    	Centroid number 1: 
    	[-0.22769812 -0.34582446 -0.41720485 -0.1187089  -0.38413343 -0.1790934
      3.        ]
    
    	Centroid number 2: 
    	[ 3.13830315e-01  3.92190593e+00  4.27561037e+00 -3.57419457e-03
      4.61816580e+00  5.03365339e-01  2.50000000e+00]
    
    	Centroid number 3: 
    	[-0.52725414  0.67712364  0.97454794 -0.34250796  0.98535368  0.0439009
      2.58139535]
    
    	Centroid number 4: 
    	[ 2.04769049  0.03613408 -0.12935913  0.61566275 -0.34062888  0.54486783
      2.75      ]
    
    	Centroid number 5: 
    	[ 1.96681731  5.17550306  1.28721685  6.90059988 -0.55486198 16.47844745
      3.        ]
    
    	Centroid number 6: 
    	[-0.14815235 -0.39254844 -0.41025632 -0.01403913 -0.39017655 -0.18845515
      1.34831461]
    
    	Centroid number 7: 
    	[ 0.79278421  0.56168505 -0.01130144  9.25255676 -0.46404706  0.93316414
      2.5       ]
    


# PCA

In this section we calculate the variance explained by the first 2 components and by the first 4 components in PCA and visualize the clusters in the data using PCA. 

First two components in PCA:


```python
pca2 = PCA(n_components=2).fit(scaledDf)
pca2df = pca2.transform(scaledDf)

print("Explained variance by the first 2 components:", pca2.explained_variance_)
print("Explained variance ratio by the first 2 components:", pca2.explained_variance_ratio_)
print(pca2df.shape)
```

    Explained variance by the first 2 components: [2.65133312 1.70737774]
    Explained variance ratio by the first 2 components: [0.40091742 0.2581786 ]
    (440, 2)


As we can see above, the explained variance ratio for first component is 40.09% and for the second component is 25.82%.

First four components in PCA:


```python
pca4 = PCA(n_components=4).fit(scaledDf)
pca4df = pca4.transform(scaledDf)

print("Explained variance by the first 4 components:", pca4.explained_variance_)
print("Explained variance ratio by the first 4 components:", pca4.explained_variance_ratio_)
```

    Explained variance by the first 4 components: [2.65133312 1.70737774 0.74423478 0.62656443]
    Explained variance ratio by the first 4 components: [0.40091742 0.2581786  0.11253836 0.09474501]


As we can see above, the explained variance ratio for first component is 40.09%, second component is 25.82%, third component is 11.25%, and fourth component is 9.47%.

The visualization of clusters using first two components of PCA would be as follow (we cannot show the plot of clusters using first four components of PCA as it would need four dimensions which is not possible to visualize):


```python
plt.figure(figsize = (10,10))
sns.scatterplot(pca4df[:,0], pca4df[:,1], 
                hue=kmeans.labels_, 
                palette="tab10")
plt.title("KMeans Clusters using first four components in PCA")
plt.legend()
plt.xlabel('Component 1')
plt.ylabel('Component 2')
plt.show()
```


    
![png](./../images/enhancing-customer-insights-in-wholesale-distribution/output_66_0.png)
    


As we can see from the above table the only clusters that are obvious that they are seperated are `cluster 1` which is represented by `orange` color, and `cluster 4` which is represented by `purple` color. The rest of the clusters shown are also seperated but cannot be visually seen in graph. 

# XGBoost Classifier

There are generally two ways to test the performance of a Gradient Boosting model. One is to explicitly indicate the train and test sets so that the model can be trained on the train model and be tested on the test set which will give us the scores of its performance. The other one is to use K-Fold CV which splits the data into `K` parts and then the system trains the model on `K-1` of those folds and finally would test the model on one fold. The system does this for `K` times and gives its average performance scores. For this section we will use `K-Fold CV` to test the performance of our model. Finally, when we have the results of our model we calculate the precision, recall, and accuracy scores to see how well the model performed.

In order to use XGBoost Classifier, first the package has to be installed which can be done by the following command. In this section we used [this link](https://machinelearningmastery.com/evaluate-gradient-boosting-models-xgboost-python/) as a reference. 


```python
# !pip install xgboost
```


```python
from xgboost import XGBClassifier
```


```python
XNonscaled = customers.drop(['Channel'], axis=1)
yNonscaled = customers['Channel']

scoring = {'accuracy' : make_scorer(accuracy_score), 
           'precision' : make_scorer(precision_score),
           'recall' : make_scorer(recall_score)}

model = XGBClassifier(eval_metric='mlogloss')
kfold = KFold(n_splits=5)
results = cross_validate(model, XNonscaled, yNonscaled, cv=kfold, scoring=scoring)

accuracy = results['test_accuracy'].mean()*100
precision = results['test_precision'].mean()*100
recall = results['test_recall'].mean()*100

print("Performance Scores: \n\tAccuracy: %f\tPrecision: %f\tRecall: %f" % (accuracy, precision, recall))
```

    Performance Scores: 
    	Accuracy: 91.136364	Precision: 93.260274	Recall: 92.966809
