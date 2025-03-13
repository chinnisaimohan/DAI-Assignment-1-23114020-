# DAI-Assignment-1-23114020-
Data Cleaning and EDA of titanic dataset 


# **Exploratory Data Analysis (EDA) Report: Titanic Dataset**

---

## **Introduction**
The Titanic dataset is one of the most popular datasets for data analysis and machine learning. It contains information about the passengers aboard the RMS Titanic, including their demographics, ticket class, fare, and whether they survived the disaster. This report provides a detailed analysis of the dataset, focusing on data cleaning, exploratory data analysis (EDA), and insights derived from the data.

---

## **Dataset Overview**
The Titanic dataset contains the following variables:
- **PassengerId**: Unique identifier for each passenger.
- **Survived**: Survival status (0 = No, 1 = Yes).
- **Pclass**: Ticket class (1 = 1st class, 2 = 2nd class, 3 = 3rd class).
- **Name**: Passenger's name.
- **Sex**: Gender of the passenger (male/female).
- **Age**: Age of the passenger.
- **SibSp**: Number of siblings/spouses aboard.
- **Parch**: Number of parents/children aboard.
- **Ticket**: Ticket number.
- **Fare**: Fare paid for the ticket.
- **Cabin**: Cabin number.
- **Embarked**: Port of embarkation (C = Cherbourg, Q = Queenstown, S = Southampton).

---

## **Data Cleaning**

### **1. Handling Missing Values**
- **Missing Values Identified**:
  - `Age`: 177 missing values.
  - `Cabin`: 687 missing values.
  - `Embarked`: 2 missing values.
- **Actions Taken**:
  - Imputed missing `Age` values with the median age.
  - Imputed missing `Embarked` values with the mode (most frequent port).
  - Dropped the `Cabin` column due to excessive missing values.

### **2. Removing Duplicate Records**
- No duplicate records were found in the dataset.

### **3. Treating Outliers**
- Outliers in the `Fare` column were detected using the Interquartile Range (IQR) method.
- Outliers were removed to ensure the analysis is not skewed.

### **4. Standardizing Categorical Values**
- Standardized categorical columns (`Sex` and `Embarked`) to ensure consistency (e.g., converting to lowercase or uppercase).

---

## **Exploratory Data Analysis (EDA)**

### **1. Univariate Analysis**
#### **Summary Statistics**
- **Numerical Variables**:
  - Mean age: ~29.7 years.
  - Median fare: £14.45.
  - Skewness in `Fare` indicates a right-skewed distribution.
- **Categorical Variables**:
  - Majority of passengers were male (65%).
  - Most passengers embarked from Southampton (72%).

#### **Frequency Distributions**
- **Survival Status**:
  - 62% of passengers did not survive.
  - 38% of passengers survived.
- **Passenger Class**:
  - 55% of passengers were in 3rd class.
  - 24% were in 1st class, and 21% were in 2nd class.

#### **Visualizations**
- **Histograms**:
  - Age distribution shows most passengers were between 20 and 40 years old.
- **Box Plots**:
  - Fare distribution highlights outliers, especially in higher fare ranges.

---

### **2. Bivariate Analysis**
#### **Correlation Matrix**
- Positive correlation between `Fare` and `Pclass` (higher fares for 1st class).
- Weak correlation between `Age` and `Survived`.

#### **Scatter Plots**
- **Age vs Fare**:
  - No strong linear relationship observed.
- **SibSp vs Parch**:
  - Passengers with more siblings/spouses tended to have more parents/children aboard.

#### **Grouped Visualizations**
- **Survival Rate by Gender**:
  - Females had a significantly higher survival rate (74%) compared to males (19%).
- **Survival Rate by Passenger Class**:
  - 1st class passengers had the highest survival rate (63%), followed by 2nd class (47%) and 3rd class (24%).

---

### **3. Multivariate Analysis**
#### **Pair Plots**
- Pair plots revealed relationships between numerical variables (`Age`, `Fare`, `SibSp`, `Parch`).
- KDE plots on the diagonal showed the distribution of each numerical variable.

#### **Heatmaps**
- Heatmap of survival rates by `Sex` and `Pclass`:
  - Females in 1st class had the highest survival rate (97%).
  - Males in 3rd class had the lowest survival rate (13%).

#### **Grouped Comparisons**
- **Age Distribution by Passenger Class and Survival**:
  - Younger passengers in 1st and 2nd classes had higher survival rates.
- **Fare Distribution by Passenger Class and Survival**:
  - Survivors in 1st class paid significantly higher fares.

---

## **Key Insights**
1. **Survival Rates**:
   - Females and 1st class passengers had the highest survival rates.
   - Males and 3rd class passengers had the lowest survival rates.

2. **Age and Survival**:
   - Children (age < 10) had higher survival rates, especially in 1st and 2nd classes.

3. **Fare and Survival**:
   - Higher fares were associated with higher survival rates, likely due to better accommodations and priority during evacuation.

4. **Family Size**:
   - Passengers with 1-2 siblings/spouses or parents/children had higher survival rates compared to those traveling alone or with large families.

---

## **Conclusion**
The analysis of the Titanic dataset revealed significant patterns in survival rates based on passenger demographics, ticket class, and fare. Key findings include:
- Females and 1st class passengers were more likely to survive.
- Younger passengers and those with moderate family sizes had higher survival rates.
- Higher fares were associated with better chances of survival.

These insights can be used to build predictive models or further explore the factors influencing survival on the Titanic.

---

## **Recommendations**
1. **Feature Engineering**:
   - Create new features such as family size (`SibSp + Parch`) and age groups (e.g., child, adult, senior).
2. **Machine Learning**:
   - Use the cleaned dataset to build classification models (e.g., logistic regression, random forest) to predict survival.
3. **Further Analysis**:
   - Investigate the impact of cabin location on survival (if cabin data is available).
   - Explore the relationship between embarkation port and survival.

---

## **References**
- Titanic Dataset: [Kaggle Titanic Dataset](https://www.kaggle.com/c/titanic/data)
- Seaborn Documentation: [Seaborn](https://seaborn.pydata.org/)
- Matplotlib Documentation: [Matplotlib](https://matplotlib.org/)

---
