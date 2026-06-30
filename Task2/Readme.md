# Titanic - Exploratory Data Analysis (EDA)

This is Task 2 of my AI and ML Internship. In this task I explored the Titanic 
dataset using statistics and visualizations to understand patterns in the data.

## What I Did

1. Loaded the dataset and checked summary statistics like mean, median and std.
2. Created histograms to see how numeric columns like Age and Fare are distributed.
3. Made boxplots to compare Age and Fare with Survived column.
4. Created a correlation heatmap to see relationship between numeric features.
5. Used pairplot to visualize multiple features together.
6. Checked survival rate based on Gender and Passenger Class.

## What I Found

- Female passengers had a higher survival rate than male passengers.
- 1st class passengers survived more compared to 3rd class.
- Fare column was right-skewed, meaning few passengers paid very high fare.
- Age and Survived did not show a strong direct correlation.

## Files

- eda_titanic.py — code for the analysis
- titanic_cleaned.csv — dataset used
- README.md — this file

## Tools Used

Pandas, Matplotlib, Seaborn
