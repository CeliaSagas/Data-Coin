<!-- Add banner here -->
![Banner](https://github.com/CeliaSagas/Data-Coin/blob/e016fd55fecf69dd8a8a5694ae838f494b5f0517/img/datacoinheader.png)

# Data Coin

<!-- Add buttons here -->


![GitHub last commit](https://img.shields.io/github/last-commit/CeliaSagas/Data-Coin)
![GitHub issues](https://img.shields.io/github/issues/CeliaSagas/Data-Coin)
![GitHub pull requests](https://img.shields.io/github/issues-pr/CeliaSagas/Data-Coin)
![Project Code](https://img.shields.io/github/languages/top/CeliaSagas/Data-Coin)


<!-- Describe your project in brief -->

You've just finished up your statistics and coding training, and are ready to hit the job field as a budding new Data Scientist ready to bloom.

What kind of companies and job postings will best serve your growth as a creator of data pipelines and algorithms? How much monetary support will said job postings generate you?

Unfortunately, many of the job postings available today do not offer information on the available salary range per open position, which is why this regression model on Data Scientist salaries was created.

By scraping a little over 1300 salary postings in 36 cities across the continental United States on Glassdoor, I was able to create a regression model that can somewhat predict salaries for data scientists
according to some key factors identified by the model. Some of them are obvious, such as an Internship or Part Time position is associated with a decrease in Salary (about 40k), while taking a position
at a tech company on the West Coast is associated with an increase in Salary (about an 11k boost).

But some other findings are nuanced and require further modelling, such as the Cost of Living-- a higher cost of living was associated with a very modest !decrease in salary in the training set,(- $28), a
modest increase in the validation set (+ $368), and again a decrese in the test set of data (- $75). Perhaps the Cost of Living at the Headquarter city of the Company has a more direct relationship with
Salary than the Cost of Living at the city in which the Job is posted.

Further inquiry is required.

But for now, with the information thus gathered, we can gain a pretty moderate idea of the most important factors to keep in mind when applying for
Data Scientist positions (have you considered the West Coast? )

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
- [Installation](#installation)
- [Usage](#usage)
- [License](#license)
- [Footer](#footer)

# Installation
[(Back to top)](#table-of-contents)


To use this project, first clone the repo on your device using the command below:

```git init```

```git clone https://github.com/navendu-pottekkat/nsfw-filter.git```



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
