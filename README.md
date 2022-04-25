# Stellar Classification
![Project Image](https://astrobiology.nasa.gov/uploads/filer_public_thumbnails/filer_public/cf/29/cf294394-800d-4fc4-954d-78dba367de36/large_web.jpg__1240x510_q85_subject_location-620%2C254_subsampling-2.jpg)

---

### Table of Contents

- [Description](#description)
- [Methods Used](#methods-used)
- [References](#references)
- [Author Info](#author-info)

---

## Description
In astronomy, stellar classification is the classification of stars based on their spectral characteristics. The classification scheme of galaxies, quasars, and stars is one of the most fundamental in astronomy. The early cataloguing of stars and their distribution in the sky has led to the understanding that they make up our own galaxy and, following the distinction that Andromeda was a separate galaxy to our own, numerous galaxies began to be surveyed as more powerful telescopes were built. This datasat aims to classificate stars, galaxies, and quasars based on their spectral characteristics.


#### Methods Used
> **Python Libaries Used for EDA**
```
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
```
> **Python Libraries for future Machine Learning**
from sklearn.model_selection import train_test_split, GridSearchCV
from sklearn.preprocessing import StandardScaler, OneHotEncoder
from sklearn.compose import make_column_transformer, make_column_selector
from sklearn.impute import SimpleImputer
from sklearn.pipeline import make_pipeline
from sklearn.ensemble import RandomForestClassifier
from sklearn.metrics import classification_report, confusion_matrix, ConfusionMatrixDisplay
```
- **Pandas for data manipulation**: Thankfully this dataset came clean and polished for analysis and machine learning. There are no duplicate rows, missing values, inconsistent categories, or incorrect datatypes. 
```python
df.info()
```
![df info()](https://user-images.githubusercontent.com/97704503/165173934-c60e3a26-97be-46a2-8309-403766194355.jpg)


- **Exploratory visualizations**: Since every feature in this dataset except the class feature consists of numeric data, I relied heavily on seaborn violin plot visualizations to analyze the data more in depth.
![Alpha   Delta Violin plots](https://user-images.githubusercontent.com/97704503/165169798-d66f0302-c1b0-4e5d-9054-dda79833d545.png)


---

## Reference
>Data: [Stellar Classification](https://www.kaggle.com/datasets/fedesoriano/stellar-classification-dataset-sdss17)
---

## Author Info

- Email - jimenezmarco3254@gmail.com
- LinkedIn - [Marco Jimenez](https://www.linkedin.com/in/marco-jimenez-50637922b/)

[Back To The Top](#Food-Sales-Predictions)
