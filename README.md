# Heart Disease Prediction: Exploratory Data Analysis (EDA)

## Introduction
This project involves the exploration of a heart disease dataset, aiming to predict the presence of heart disease in patients based on various attributes. The dataset includes demographic and medical information, and our goal is to build a model that can classify whether a patient has heart disease or not.

## Dataset
The dataset is stored in the file `heart.csv`. It contains 303 entries with 14 features, including both continuous and categorical data.

### Dataset Description
| **Variable Name** | **Description** |
|-------------------|-----------------|
| age               | Age of the patient in years |
| sex               | Gender of the patient (0 = male, 1 = female) |
| cp                | Chest pain type: 0 = Typical angina, 1 = Atypical angina, 2 = Non-anginal pain, 3 = Asymptomatic |
| trestbps          | Resting blood pressure in mm Hg |
| chol              | Serum cholesterol in mg/dl |
| fbs               | Fasting blood sugar > 120 mg/dl (1 = true, 0 = false) |
| restecg           | Resting electrocardiographic results: 0 = Normal, 1 = ST-T wave abnormality, 2 = Probable/definite left ventricular hypertrophy |
| thalach           | Maximum heart rate achieved during stress test |
| exang             | Exercise-induced angina (1 = yes, 0 = no) |
| oldpeak           | ST depression induced by exercise relative to rest |
| slope             | Slope of the peak exercise ST segment: 0 = Upsloping, 1 = Flat, 2 = Downsloping |
| ca                | Number of major vessels (0-4) colored by fluoroscopy |
| thal              | Thalium stress test result: 0 = Normal, 1 = Fixed defect, 2 = Reversible defect, 3 = Not described |
| target            | Heart disease status (0 = no disease, 1 = presence of disease) |

### Dataset Overview
- **Number of Entries:** 303 rows, from index 0 to 302.
- **Columns:** 14 columns, including both numerical and categorical data.
- **Data Types:**
  - Most columns are of `int64` type, except for the `oldpeak` column, which is `float64`.
- **Missing Values:** There are no missing values in the dataset.

## Exploratory Data Analysis (EDA)

### 1. Univariate Analysis
In this phase, we examine each feature individually to understand its distribution, range, and variability.

#### Numerical Variables Distribution
Histograms and KDE plots were created for continuous features to analyze their distribution. The features examined include:
- `age`
- `trestbps`
- `chol`
- `thalach`
- `oldpeak`

#### Categorical Variables Distribution
For categorical features, we analyzed the frequency percentages using bar plots.

### 2. Bivariate Analysis
This phase investigates the relationship between each feature and the target variable to evaluate its impact on predicting heart disease.

#### Numerical Features vs Target
For each continuous feature, we compared its distribution between heart disease (`target = 1`) and no heart disease (`target = 0`) using bar plots and KDE plots.

#### Categorical Features vs Target
We used stacked bar plots to show the proportions of each categorical feature with respect to the target variable.

### 3. Outlier Treatment
Outliers in continuous variables were handled using the Interquartile Range (IQR) method. Outliers outside the 1.5 * IQR were clipped to the respective boundary values.

#### Columns Affected:
- `age`
- `trestbps`
- `chol`
- etc.

#### Outliers Before and After Treatment:
The number of outliers before and after clipping was noted for each column.

### 4. Categorical Features Encoding

#### One-Hot Encoding Decision
- **Nominal Variables (One-Hot Encode):** `cp`, `restecg`, `thal`
- **Binary/Ordinal Variables (No Encoding):** `sex`, `fbs`, `exang`, `slope`, `ca`

Categorical variables with multiple levels (such as `cp`, `restecg`, `thal`) were one-hot encoded. Binary and ordinal features were left unchanged, as encoding is unnecessary.

## Conclusion
The exploratory data analysis provides insights into the dataset's structure, distribution of features, and their relationships with the target variable. Outliers were treated, and categorical features were properly encoded for further modeling.

## Next Steps
1. Split the dataset into training and testing sets.
2. Build machine learning models to predict heart disease using algorithms such as Logistic Regression, Random Forest, KNN, etc.
3. Perform model evaluation using appropriate metrics.
