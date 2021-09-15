![Header](https://github.com/CeliaSagas/Data-Coin/blob/e016fd55fecf69dd8a8a5694ae838f494b5f0517/img/datacoinheader.png)


# Abstract   :pushpin:


The goal of this project is to identify which key factors contribute to the expected salary range of a Data Scientist job posting. By scraping a little over 1300 salary postings in 36 cities across the continental United States, I was able to create a regression model that can somewhat predict salaries for data scientists according to some *key factors* identified by the model. Some of them are obvious, such as an Internship or Part Time position is associated with a decrease in Salary *(about 40k)*, while taking a position at a tech company on the West Coast is associated with an increase in Salary *(about an 11k boost)*.


# Design   :bar_chart:

Lasso and Ridge lambda tuning models were applied to standardized data, as well as Step Oridinary Least Squares modelling removing influential points and outliers. A Lasso model was chosen for final testing in order to avoid overfitting and data loss while achieving a maximal fit.


# Data   :floppy_disk:

1300+ data points were scraped from Glassdoor targeting 36 cities in the continental United States repsenting all four major geographical areas of the country (West, Midwest, South and North East). Variables of interest included the Base Salary, Salary Range, and Additional Pay per company per city, as well as industry, year founded, and revenue of said company. Additional Cost of Living Index by city was scraped from Numbeo.

# Algorithms   :printer:

**Data Preparation** :mag:

1.	Removed salaries below $25,000 as they represented monthly pay instead of annual pay.
2.	Removed stock information from "Company Type" column in order to compare relevant company types with salary. Simplified said category in order to represent relevant business categories.
3.  Reviewed Revenue information per company and simplified data into 5 bins.
3.	Reviewed size information per company and simplified data into 5 bins.
4.	Mapped city location by geographical location in the United States and created a "Geograpic Map" category for modelling.
5. Added Cost of Living Index per city to the dataframe from data scrapped from Numbeo.
6. Re-mapped hundreds of industries associated with Company information into 13 distinct categories, identified key industries to compare, and simplified categories into three distinct bins.
7. Corrected "year founded" data for erroneous postings (UC Berkeley, Chubb), transformed year founded to Age.
8. Performed boxcox transformation Additional Pay, then recoded additional pay into "Low" and "High" categories.
9. Transformed Number of Interviews reported on Glassdoor using the boxcox method.
10. Simpified the Internship/Part time/ Contractor column into a binary label, Internship/Part Time or No Internship.

**Data Analysis** :mag:
1. Standardized all continuous numerical data using the StandardScaler from SKLearn.
2. Added an interaction term for West Coast + Tech industry
3. Identified highly correlated features and removed those who had a pearson correlation coefficient > 0.7
4. Added constant to Features dataframe and removed features with a VIF > 5.00
5. Performed a Lasso Cross-Validation model with a Alpha Tuning on the training dataset with 28 features, 4 were dropped, Adjusted r2 = 0.433, MAE = 16138.46, RMSE = .451
6. Performed a Ridge Cross-Validated model with Alpha Tuning on the training dataset with 28 features, Adjusted r2 = .431, MAE = 16117.85, RMSE = 20851.42
7. Performed an OLS model with 28 features on the training dataset, 9 were significant, Adjusted r2 = .434, MAE = 16059.89, RMSE = 20812.746
8. Performed a Step OLS model with insgnificant features removed on the training dataset, totalling 9 predictors, Adjusted r2 = .425, MAE = 16524.80, RMSE = 21221.05
9. Identified influential points in the model and removed them, ran a subsequent Step OLS analysis with 9 features on the training set, Adjusted r2 = .445, MAE = 16156.337, RMSE = 20612.63
10. Identified outliers in the model using Cook's distance, ran a subsequent Step OLS model with 9 features, 728 observations on the training datset, Adjusted r2 = 0.530, MAE = 14129.89, RMSE = 17227.546.
11. Performed a Lasso Regression Analysis on the validation dataset with the optimal alpha value from the training dataset, Adjusted r2 = .468, MAE = 15577.056, RMSE = 20184.325
12. Performed a Lasso Regression Analysis on the test dataset with the optimal alpha value identified in training, Final Adjusted r2 = .401, MAE = 16669.88, RMSE = 22055.264

# Tools   :hammer_and_pick:

-	Pandas, Numpy, Scipy, Collections, Re, Matplotlib, and Seaborn used for data preparation.
-	SKLearn, Stasmodels, itertools, and Math used for Data Analysis
-	Matplotlib and Seaborn used for visualizations.

# Communication  :loud_sound:

Glassdoor analysis will be shared on Medium, Celiasagastume.com, and in class through PowerPoint presentation. Further visualizations on Glassdoor will be developed and shared on Reddit. 
