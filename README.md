# **Crime Classification using KDD Methodology**

## **Project Overview**
This project aims to demonstrate the use of the Knowledge Discovery in Databases (KDD) methodology to build a crime classification model using a publicly available crime dataset. The goal is to classify crime types based on various attributes such as location, time, and victim demographics. Using machine learning techniques, we can predict whether a crime falls under a Part 1 (serious crime) or Part 2 (less severe crime) category. This project applies the KDD process to ensure a systematic flow from data preparation to model evaluation.

The KDD methodology consists of five stages: Selection, Preprocessing, Transformation, Data Mining, and Interpretation. Each stage is implemented in this project to build an effective classification model.

## **KDD Methodology**
The KDD (Knowledge Discovery in Databases) methodology provides a structured approach to extracting useful knowledge from large datasets. It consists of the following five phases:

### **1. Selection**
- Selected the "Crime Data from 2020 to Present" dataset from the Los Angeles Police Department's open data portal.
- The dataset contains over 200,000 rows and 28 columns, detailing various aspects of reported crime incidents.
- Relevant attributes such as `Vict Age`, `Vict Sex`, `Vict Descent`, `Premis Cd`, and `Weapon Used Cd` were selected as feature variables, while the target variable was `Part 1-2` (indicating whether the crime is a serious Part 1 offense or a less severe Part 2 offense).

### **2. Preprocessing**
- Checked for missing values and handled any inconsistencies in the data.
- Cleaned column names by removing leading/trailing spaces and standardized formats.
- Applied one-hot encoding to categorical variables such as `Vict Sex` and `Vict Descent` to prepare the data for modeling.

### **3. Transformation**
- Converted categorical features into numerical representations using one-hot encoding.
- Engineered additional features such as `FamilySize` and other relevant indicators to capture information on the context of the crime.
- Scaled the continuous features using `StandardScaler` to ensure all features contribute equally during modeling.

### **4. Data Mining**
- Implemented a Random Forest Classifier to classify crimes as either Part 1 or Part 2 offenses.
- Split the dataset into training (80%) and testing (20%) sets using stratified sampling to maintain class distribution.
- Hyperparameter tuning was performed using Grid Search to optimize the model for accuracy and recall.

### **5. Interpretation**
- Evaluated the model using classification metrics such as Precision, Recall, F1-Score, and ROC-AUC.
- Visualized the performance using a confusion matrix and ROC curve to demonstrate the model’s predictive capabilities.
- Analyzed the most important features influencing the classification results.

## **Dataset Information**
The dataset used for this project is sourced from the [Los Angeles Police Department's Open Data Portal](https://data.lacity.org/). It includes crime reports from 2020 to the present and contains 28 features such as:

- **DR_NO**: Report Number (Unique Identifier)
- **Date Rptd**: Date the crime was reported
- **Vict Age**: Age of the victim
- **Vict Sex**: Gender of the victim (M/F)
- **Vict Descent**: Ethnic descent of the victim
- **Premis Cd**: Code representing the type of premises where the crime occurred
- **Weapon Used Cd**: Type of weapon used
- **Crm Cd Desc**: Description of the crime
- **Class**: Target variable (1 = Part 1 crime, 2 = Part 2 crime)

## **Medium Article**
https://medium.com/@syedanidakhader/unveiling-crime-patterns-a-journey-through-kdd-in-crime-analysis-8a8d02474e85
