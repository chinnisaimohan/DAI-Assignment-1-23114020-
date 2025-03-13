# **Titanic Dataset Analysis**

This repository contains the code and analysis for the **Titanic Dataset**, focusing on data cleaning, exploratory data analysis (EDA), and visualization of key insights. The goal of this project is to understand the factors that influenced survival on the Titanic.

---

## **Repository Structure**

```
Titanic-Dataset-Analysis/
├── data/
│   └── titanic.csv                # Raw Titanic dataset
├── notebooks/
│   └── Titanic_Analysis.ipynb     # Jupyter Notebook for analysis
├── images/                        # Folder for saved visualizations
│   ├── survival_rate_gender_pclass.png
│   ├── age_distribution_survival.png
│   └── fare_distribution_pclass.png
├── README.md                      # This file
└── requirements.txt               # Python dependencies
```

---

## **Project Overview**

### **Objective**
The objective of this project is to:
1. Perform **data cleaning** to handle missing values, duplicates, and outliers.
2. Conduct **exploratory data analysis (EDA)** to uncover patterns and relationships in the data.
3. Visualize key insights using **bar plots**, **violin plots**, **box plots**, and **heatmaps**.

### **Dataset**
The dataset used is the **Titanic Dataset**, which contains information about passengers aboard the RMS Titanic, including:
- **Survived**: Survival status (0 = No, 1 = Yes).
- **Pclass**: Ticket class (1 = 1st class, 2 = 2nd class, 3 = 3rd class).
- **Sex**: Gender of the passenger.
- **Age**: Age of the passenger.
- **Fare**: Fare paid for the ticket.
- **Embarked**: Port of embarkation.

---

## **Steps Performed**

### **1. Data Cleaning**
- Handled missing values in `Age`, `Embarked`, and `Cabin`.
- Removed duplicate records.
- Detected and treated outliers in the `Fare` column.
- Standardized categorical values (e.g., `Sex` and `Embarked`).

### **2. Exploratory Data Analysis (EDA)**
- **Univariate Analysis**:
  - Summary statistics for numerical variables.
  - Frequency distributions for categorical variables.
  - Histograms and box plots for numerical variables.
- **Bivariate Analysis**:
  - Correlation matrix for numerical variables.
  - Scatter plots for relationships between numerical variables.
  - Grouped bar plots and box plots for categorical vs. numerical variables.
- **Multivariate Analysis**:
  - Pair plots for multiple numerical variables.
  - Heatmaps for survival rates by `Sex` and `Pclass`.

### **3. Visualizations**
- **Survival Rate by Gender and Passenger Class**:
  - Bar plot showing survival rates for males and females across passenger classes.
- **Age Distribution by Survival Status**:
  - Violin plot showing age distributions for survivors and non-survivors.
- **Fare Distribution by Passenger Class**:
  - Box plot showing fare distributions across passenger classes.

---

## **Key Insights**
1. **Survival Rates**:
   - Females and 1st class passengers had the highest survival rates.
   - Males and 3rd class passengers had the lowest survival rates.
2. **Age and Survival**:
   - Children (age < 10) had higher survival rates, especially in 1st and 2nd classes.
3. **Fare and Survival**:
   - Higher fares were associated with higher survival rates.

---

## **How to Use This Repository**

### **1. Clone the Repository**
```bash
git clone https://github.com/your-username/Titanic-Dataset-Analysis.git
cd Titanic-Dataset-Analysis
```

### **2. Install Dependencies**
Ensure you have the required Python libraries installed:
```bash
pip install -r requirements.txt
```

### **3. Run the Jupyter Notebook**
Open the Jupyter Notebook to explore the analysis:
```bash
jupyter notebook notebooks/Titanic_Analysis.ipynb
```

### **4. View Visualizations**
The visualizations are saved in the `images/` folder. You can view them directly or access them in the Jupyter Notebook.

---

## **Dependencies**
- Python 3.x
- Libraries:
  - pandas
  - numpy
  - matplotlib
  - seaborn
  - jupyter

---

## **Files**
- **`data/titanic.csv`**: The raw Titanic dataset.
- **`notebooks/Titanic_Analysis.ipynb`**: Jupyter Notebook containing the analysis.
- **`images/`**: Folder containing saved visualizations.
- **`requirements.txt`**: List of Python dependencies.

---

## **Contributing**
If you'd like to contribute to this project, please follow these steps:
1. Fork the repository.
2. Create a new branch for your feature or bugfix.
3. Commit your changes.
4. Submit a pull request.

---

## **License**
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## **Contact**
For questions or feedback, please contact:
- **Your Name**
- **Email**: your.email@example.com
- **GitHub**: [your-username](https://github.com/your-username)

---

This `README.md` file provides a clear and structured overview of your project, making it easy for others to understand and use your repository. Let me know if you need further assistance!
