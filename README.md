<!-- Add banner here -->
![Banner](https://github.com/CeliaSagas/Data-Coin/blob/e016fd55fecf69dd8a8a5694ae838f494b5f0517/img/datacoinheader.png)

# Data Coin

<!-- Add buttons here -->


![GitHub last commit](https://img.shields.io/github/last-commit/CeliaSagas/Data-Coin)
![GitHub issues](https://img.shields.io/github/issues/CeliaSagas/Data-Coin)
![GitHub pull requests](https://img.shields.io/github/issues-pr/CeliaSagas/Data-Coin)
![Project Code](https://img.shields.io/github/languages/top/CeliaSagas/Data-Coin)


<!-- Describe your project in brief -->

You've just finished up your statistics and coding training, and are ready to hit the job field as a *budding* new Data Scientist ready to bloom.

What kind of companies and job postings will best serve your growth as a creator of data pipelines and algorithms? **How much monetary support will said job postings generate you?**

*Unfortunately*, many of the job postings available today *do not offer* information on the available salary range per open position, which is why I decided to collect and model said information from Glassdoor.

By scraping a little over 1300 salary postings in 36 cities across the continental United States, I was able to create a regression model that can somewhat predict salaries for data scientists according to some *key factors* identified by the model. Some of them are obvious, such as an Internship or Part Time position is associated with a decrease in Salary *(about 40k)*, while taking a position
at a tech company on the West Coast is associated with an increase in Salary *(about an 11k boost)*.


# Demo-Preview
<!-- Add a demo for your project -->

This project uses Python packages: pandas, numpy, request, os, selenium, statsmodels, sklearn and matplotlib to model and visualize salary data scraped from Glassdoor.

![Histogram Salary](https://github.com/CeliaSagas/Data-Coin/blob/12b8f09a65710ad579b19c905886df361f192a97/img/salary_hist.png)

The histogram of salaries as reported on Glassdoor show a mean salary of $109,038.29 across the continental United States, with a standard deviation of $28,715.00.


![Bar Plot Revenue](https://github.com/CeliaSagas/Data-Coin/blob/12b8f09a65710ad579b19c905886df361f192a97/img/revenue_bar.png)

Salary range per company revenue show that working for a $10 Billion+ company definitely does pay a bit higher compared to companies making less than $10 Billion, while Unknown/ Non-Applicable revenue refers to Non-Profit, Education, and Government salary ranges.

![Bar Plot Location](https://github.com/CeliaSagas/Data-Coin/blob/12b8f09a65710ad579b19c905886df361f192a97/img/location_bar.png)

Geographical location was mapped onto the City in which the Salary was posted, with a higher representation in the West Coast due to the amount of cities associated with the Tech Industry in California, which also contributes to the increase in Salary range for that area.


[Click Here](https://github.com/CeliaSagas/Data-Coin) to see the full project

# Table of contents


- [Project Title](#project-title)
- [Demo-Preview](#demo-preview)
- [Table of contents](#table-of-contents)
- [Data](#Data)
- [Installation](#installation)
- [Usage](#usage)
- [License](#license)
- [Footer](#footer)

# Data

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
4. Performed an XGboosted Regression model tuning Alpha, Learning Rate, Sub Sample, and Alpha. Adjusted r2 = 0.51, RMSE = 18931.85
5. Performed a Lasso Cross-Validation model with a Alpha Tuning on the training dataset with 19 features, 6 were dropped, Adjusted r2 = 0.370, RMSE = 21769.71
6. Performed a Ridge Cross-Validated model with Alpha Tuning on the training dataset with 19 features, Adjusted r2 = .41, RMSE = 21676.12
7. Chose XGBoosted Regression for final model, final Adjusted r2 = 0.67, RMSE = 15831.538


![Adjusted R2 Values](https://github.com/CeliaSagas/Data-Coin/blob/b8cfc8485e96d6e3b982803e606aabcc992c78f4/img/Bar_Plot_ADJ_R2.png)


![RMSE Values](https://github.com/CeliaSagas/Data-Coin/blob/b8cfc8485e96d6e3b982803e606aabcc992c78f4/img/Bar_Plot_RMSE.png)



# Installation
[(Back to top)](#table-of-contents)


To use this project, first clone the repo on your device using the command below:

```git init```

```git clone https://github.com/CeliaSagas/Data-Coin.git```



# Usage
[(Back to top)](#table-of-contents)

Glassdoor Salaries are accessed through the search page:

[Glassdoor Salary Search](https://www.glassdoor.com/Salaries/index.htm)

Glassdoor Company Overview is accessed through Data Scientist Salary posting per Company:

[Facebook Overview](https://www.glassdoor.com/facebook)

And Cost of Living Index was accessed through Numbeo:

[Cost of Living](https://www.numbeo.com/cost-of-living/rankings.jsp)

The Full List of Cities used for this project is:

        Dallas, texas
        Miami, Fl
        Atlanta, Ga
        Detroit, Mi
        Cleveland, Oh
        Denver, co
        Orlando, Fl
        st.louis, Mo
        Charlotte, Nc
        Salt Lake City, Ut
        Columbus, Oh
        Las Vegas, Nv
        Kansas City, Mo
        Indianapolis, In
        Cincinnati, Oh
        Raleigh, Nc
        Phoenix, Az
        Portland, Or
        Houston, Tx
        Seattle, Wa
        San francisco, Ca
        Austin, Tx
        San Jose, Ca
        Boston, Ma
        Washington, Dc
        philadelphia, Pa
        Fremont, CA
        New York, NY
        Arlington, va
        Los Angeles, ca
        Irvine, ca
        Chicago, Il
        Minneapolis, MN
        Baltimore, MD
        San Diego, CA
        Palo Alto, CA


# License
[(Back to top)](#table-of-contents)

This project is designed for free and open use.

[GNU General Public License version 3](https://opensource.org/licenses/GPL-3.0)

# Footer
[(Back to top)](#table-of-contents)

I hope this information brings you all the fulfillment and Salary options in your job search!

<!-- Add the footer here -->

![Footer](https://github.com/CeliaSagas/Data-Coin/blob/12b8f09a65710ad579b19c905886df361f192a97/img/datacoinfooter.png)
