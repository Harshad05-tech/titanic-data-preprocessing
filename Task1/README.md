# Titanic Data Cleaning & Preprocessing

This is my first task from the AI & ML Internship. In this task I worked on the 
Titanic dataset and cleaned it properly so that it can be used for machine learning models.

---

## What is this project about?

When we get real world data it is never clean. It has missing values, wrong data types,
text columns, and outliers. Before feeding any data into a ML model we have to clean it 
and prepare it. That is exactly what I did in this project using the Titanic dataset.

---

## Dataset

- Name: Titanic Dataset
- File used: train.csv
- Source: Kaggle
- Total Rows: 891
- Total Columns: 12

The Titanic dataset contains information about the passengers who were on the Titanic ship.
It includes details like their age, gender, ticket class, fare they paid, where they boarded 
from, and whether they survived or not.

---

## What I Did — Step by Step

### Step 1 — Loaded the Dataset
First I imported the dataset using pandas and explored it by checking the first few rows,
data types of each column, and basic statistics like mean, min, max values.

### Step 2 — Checked Missing Values
I used isnull().sum() to find out which columns had missing data.

Results:
- Age column had 177 missing values
- Cabin column had 687 missing values  
- Embarked column had 2 missing values

### Step 3 — Handled Missing Values
- Age: I filled the missing values with the mean age of all passengers because 
  age is a numerical column and mean is a good estimate.
- Embarked: I filled the 2 missing values with the mode (most frequent value) 
  which was 'S' (Southampton).
- Cabin: This column had too many missing values (almost 77%) so I dropped 
  the entire column because it was not useful anymore.

### Step 4 — Removed Unnecessary Columns
Columns like Name, Ticket, and PassengerId are just identifiers. They do not help 
the model learn anything useful so I removed them.

### Step 5 — Encoded Categorical Columns
Machine learning models only understand numbers. So I converted text columns into numbers.

- Sex column: I used Label Encoding. male became 1 and female became 0.
- Embarked column: I used One-Hot Encoding. The three categories S, C, Q became 
  separate columns with 0 and 1 values.

### Step 6 — Detected Outliers using Boxplot
I plotted boxplots for Age and Fare columns to visually see the outliers.
Outliers are data points that are very far from the rest of the data.
For example some passengers paid extremely high fares which were outliers.

### Step 7 — Removed Outliers using IQR Method
I used the IQR (Interquartile Range) method to remove outliers.

IQR = Q3 - Q1
Any value below Q1 - 1.5*IQR or above Q3 + 1.5*IQR was removed.

I did this for both Age and Fare columns. After removing outliers I plotted 
the boxplots again to confirm they were gone.

### Step 8 — Feature Scaling
Age and Fare columns had very different ranges. Age was between 0-80 and 
Fare was between 0-500. This big difference can confuse ML models.

So I used StandardScaler to bring both columns to the same scale where 
mean becomes 0 and standard deviation becomes 1.

### Step 9 — Saved the Cleaned Dataset
Finally I saved the cleaned and processed dataset as titanic_cleaned.csv 
so it is ready to be used in any machine learning model.

---

## Files in this Repository

- train.csv — original raw dataset downloaded from Kaggle
- Data_preprocessing.py — main Python script with all the cleaning steps
- titanic_cleaned.csv — final cleaned dataset after all preprocessing
- README.md — this file explaining the whole project

---

## Libraries Used

- pandas — for loading and manipulating the dataset
- numpy — for numerical operations
- matplotlib — for plotting graphs
- seaborn — for better looking boxplots
- scikit-learn — for Label Encoding and Standard Scaling

---

## What I Learned

- How to explore a dataset and understand its structure
- How to handle missing values using mean, mode, and dropping columns
- How to convert text data into numbers using encoding techniques
- How to detect and remove outliers using boxplots and IQR method
- How to scale numerical features so they are on the same range
- Why data preprocessing is so important before building any ML model

---

## Tools Used

- Python 3
- VS Code
- GitHub (for submission)
