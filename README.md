# Stellar Classification
![Project Image](https://astrobiology.nasa.gov/uploads/filer_public_thumbnails/filer_public/cf/29/cf294394-800d-4fc4-954d-78dba367de36/large_web.jpg__1240x510_q85_subject_location-620%2C254_subsampling-2.jpg)

---

### Table of Contents

- [Description](#description)
- [Methods Used](#methods-used)
- [References](#reference)
- [Author Info](#author-info)

---

## Description
In astronomy, stellar classification is the classification of stars based on their spectral characteristics. The classification scheme of galaxies, quasars, and stars is one of the most fundamental in astronomy. The early cataloguing of stars and their distribution in the sky has led to the understanding that they make up our own galaxy and, following the distinction that Andromeda was a separate galaxy to our own, numerous galaxies began to be surveyed as more powerful telescopes were built. This datasat aims to classificate stars, galaxies, and quasars based on their spectral characteristics.


#### Methods Used
> All code written in Python
- **Python Libaries Used for EDA**
```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
```
- **Python Libraries for future Machine Learning**
```python
from sklearn.model_selection import train_test_split, GridSearchCV
from sklearn.preprocessing import StandardScaler, LabelEncoder
from sklearn.pipeline import make_pipeline
from sklearn.decomposition import PCA
from sklearn.linear_model import LogisticRegression
from sklearn.neighbors import KNeighborsClassifier
from sklearn.metrics import classification_report, confusion_matrix, ConfusionMatrixDisplay
```

- **Pandas for data manipulation**: Thankfully this dataset came clean and polished for analysis and machine learning. There are no duplicate rows, missing values, inconsistent categories, or incorrect datatypes. 
```python
df.info()
```
![df info()](https://user-images.githubusercontent.com/97704503/165173934-c60e3a26-97be-46a2-8309-403766194355.jpg)


- **Exploratory visualizations**: Since every feature in this dataset except the class feature consists of numeric data, I relied heavily on seaborn violin plot visualizations to analyze the data more in depth. Violin plots are very useful for analyzing numeric data. I analyzed the target column with a histogram to check for imbalance in the dataset.

> Target column

![download](https://user-images.githubusercontent.com/97704503/165180724-a0b0f702-fa1a-4bd4-95e8-cd1d3190c41d.png)

> Alpha: Right Ascension Angle. Astronimical equivalent of longitude

> Delta: Declination Angle. Astronimical equivalent of latitude


![Alpha   Delta Violin plots](https://user-images.githubusercontent.com/97704503/165169798-d66f0302-c1b0-4e5d-9054-dda79833d545.png)

- **Machine Learning**: I applied 2 machine learning models to this dataset. A K Neighbors Classifier model, and a Logistic Regression model. I used PCA and GridSearchCV to enhance both models to perform faster and better. In the end I found K Nearest Neighbors to be a slightly better model to apply to this dataset.

> PCA: Principal Component Analysis. The scree plot shows a strong elbow at 3 & 5, so I went with a value of 5 n_components for PCA 
```python
# Instantiating Standard Scaler
scaler = StandardScaler()
# Fitting and transforming data
scaled_df = scaler.fit_transform(X)
# Instantiating & fitting PCA
pca = PCA()
pcs = pca.fit_transform(scaled_df)
```
```python
# Plotting the explained variance ratios of the first 9 principal components
plt.plot(range(1, 10), pca.explained_variance_ratio_, marker = '.')
plt.xticks(ticks = range(1, 10), fontsize=8)
plt.xlabel('Principal Component')
plt.ylabel('Proportion of Explained Variance')
```

![Scree Plot](https://user-images.githubusercontent.com/97704503/166168817-c2bf15c7-d018-49f4-8798-1a8d9f2ba382.png)

> K Neighbors Classifier w/ PCA & Gridsearch CV performance

```
KNN Classification Report for Training Set
              precision    recall  f1-score   support

           0       0.97      0.98      0.97     44584
           1       0.96      0.99      0.97     16195
           2       0.97      0.92      0.94     14221
    accuracy                           0.97     75000
   macro avg       0.97      0.96      0.96     75000
weighted avg       0.97      0.97      0.97     75000
```
```
KNN classification Report for Testing Set
              precision    recall  f1-score   support

           0       0.96      0.96      0.96     14861
           1       0.94      0.97      0.95      5399
           2       0.96      0.89      0.92      4740

    accuracy                           0.95     25000
   macro avg       0.95      0.94      0.95     25000
weighted avg       0.95      0.95      0.95     25000
```

> Logistic Regression w/ PCA & GridSearchCV performance

```
Log Reg classification Report for Training Set
              precision    recall  f1-score   support

           0       0.95      0.97      0.96     44584
           1       0.96      1.00      0.98     16195
           2       0.94      0.86      0.89     14221

    accuracy                           0.95     75000
   macro avg       0.95      0.94      0.95     75000
weighted avg       0.95      0.95      0.95     75000

```
```
Log Reg classification Report for Testing Set
              precision    recall  f1-score   support

           0       0.96      0.97      0.96     14861
           1       0.97      1.00      0.98      5399
           2       0.94      0.87      0.90      4740

    accuracy                           0.96     25000
   macro avg       0.95      0.94      0.95     25000
weighted avg       0.96      0.96      0.96     25000

```

---

## Reference
>Data: [Stellar Classification](https://www.kaggle.com/datasets/fedesoriano/stellar-classification-dataset-sdss17)
---

## Author Info

- Email - jimenezmarco3254@gmail.com
- LinkedIn - [Marco Jimenez](https://www.linkedin.com/in/marco-jimenez-50637922b/)

[Back To The Top](#Food-Sales-Predictions)
