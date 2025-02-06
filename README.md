# Heart Disease Analysis Project

## Project Overview

This project aims to analyze a heart disease dataset to identify patterns and relationships between different features and the presence of heart disease. The project involves exploratory data analysis (EDA), data preprocessing, and visualization using various machine learning techniques.

---

## Table of Contents

1. [Importing Libraries](#importing-libraries)
2. [Dataset Description](#dataset-description)
3. [Exploratory Data Analysis](#exploratory-data-analysis)
4. [Data Preprocessing](#data-preprocessing)
5. [Visualization](#visualization)
6. [Results](#results)

---

## Importing Libraries

The following libraries were used:

```python
import warnings
warnings.filterwarnings('ignore')
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
from sklearn.model_selection import train_test_split
from sklearn.pipeline import Pipeline
from sklearn.preprocessing import StandardScaler
from sklearn.neighbors import KNeighborsClassifier
from sklearn.linear_model import LogisticRegression
from sklearn.svm import SVC
from sklearn.model_selection import GridSearchCV, StratifiedKFold
from sklearn.metrics import classification_report, accuracy_score
from sklearn.tree import DecisionTreeClassifier
from sklearn.ensemble import RandomForestClassifier
```

---

## Dataset Description

The heart disease dataset contains 303 entries and 14 columns representing various patient attributes and test results:

- `age`: Age of the patient in years
- `sex`: Gender of the patient (0 = male, 1 = female)
- `cp`: Chest pain type (0: Typical angina, 1: Atypical angina, etc.)
- `trestbps`: Resting blood pressure in mm Hg
- `chol`: Serum cholesterol in mg/dl
- `fbs`: Fasting blood sugar > 120 mg/dl (1 = true, 0 = false)
- `restecg`: Resting electrocardiographic results
- `thalach`: Maximum heart rate achieved
- `exang`: Exercise-induced angina (1 = yes, 0 = no)
- `oldpeak`: ST depression induced by exercise
- `slope`: Slope of the peak exercise ST segment
- `ca`: Number of major vessels colored by fluoroscopy
- `thal`: Thalium stress test result
- `target`: Heart disease status (0 = no disease, 1 = presence of disease)

---

## Exploratory Data Analysis

### Numerical Variables

Continuous features analyzed included:

- `age`, `trestbps`, `chol`, `thalach`, and `oldpeak`

**Visualization Example:**

- Histograms were used to analyze the distributions.
- Mean and standard deviations were annotated.

### Categorical Variables

**Analysis:**

- Frequency distribution for `sex`, `cp`, and other categorical features was visualized.
- Bar plots showcased percentage distributions.

---

## Data Preprocessing

- Continuous features were isolated and analyzed separately.
- Features inherently categorical were converted to the appropriate data type.
- Missing values: There were no missing values.

---

## Visualization

### Continuous Variables vs Target

Bar plots and KDE plots revealed patterns between heart disease presence and variables like age and cholesterol levels.

### Categorical Variables vs Target

Cross-tabulations demonstrated the relationship between categorical variables and target outcomes.

---

## Results

- Clear insights were obtained into features that significantly impact the presence of heart disease.
- Categorical and continuous features were visualized effectively to identify trends.

---

## Conclusion

This project provided valuable insights into factors affecting heart disease status. Further work could involve hyperparameter tuning and model evaluation using advanced machine learning techniques.

---

