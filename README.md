![Header](https://github.com/CeliaSagas/Data-Coin/blob/c33d8e47151a67585af6103b46f8282cdcc8a8fd/img/coin-spin-4.gif)




# Data-Coin
Regression Analysis of Data Scientist Salaries on Glassdoor




# Question/Need: :question:

**1. What is the question behind your analysis? What is the purpose of the model/system you plan to build?**

  - Data Scientist salaries posted on Glassdoor may vary by geographical location, industry, size of company, and number of reviews left by current and former employees of each company. I plan to build a regression model that will identify what the most important factors for predicting salary are, so that newly trained data scientists entering the field know what to take into consideration when negotiating their salary.



**2. Who benefits from exploring this question or building this model/system?**

  - New data scientists entering then field and considering what salary to negotiate for, as well as current data scientists gauging their own salary against the industry norms in their area.



# Data Description: :card_index_dividers:

**1. What dataset(s) do you plan to use, and how will you obtain the data?**

  - I will scrape Glassdoor.com for 50 data science salary postings in the top 10 major metropolitan areas for tech in the United States:

            * Dallas, texas
            *  Miami, fl
            *  Atlanta, georgia
            *  Detroit, mi
            *  Cleveland, oh
            *  Denver, co
            *  Orlando, fl
            *  st.louis, mo
            *  Charlotte, nc
            *  Salt Lake City, ut
            *  Columbus, oh
            *  Las Vegas, nv
            *  Kansas City, mo
            *  Indianapolis, in
            *  Cincinnati, oh
            *  Raleigh, nc
            *  phoenix, az
            *  portland, or
            *  houston, tx
            *  seattle, wa
            *  san francisco, ca
            *  Austin, Tx
            *  san jose, ca
            *  boston, ma
            *  washington, dc
            *  philadelphia, pa
            *  fremont, CA
            *  New York, NY
            *  arlington, va
            *  los angeles, ca
            *  irvine, ca
            *  chicago, il
            *  Minneapolis, MN
            *  Baltimore, MD
            *  San Diego, CA
            *  Palo Alto, CA



**2. What is an individual sample/unit of analysis in this project?**

   - A single unit of analysis is one company with data on location, size, industry, data scientist base salary, lowest salary, highest salary, 1st quartile, 3rd quartile, cash bonus, stock bonus, number of reviews, number of salaries the Glassdoor.com estimate is based on, and data scientist total salary.


**3. What characteristics/features do you expect to work with?**

   - I expect to work with the total salary, location, size, and industry for each company.


**4. If modeling, what will you predict as your target?**

   - My predictive target is the total salary per company.



# Tools: :hammer_and_wrench:

**1. How do you intend to meet the tools requirement of the project?**

   - I plan to use pandas, seaborn, matplotlib, scipy, selenium, and chromedriver.


**2. Are you planning in advance to need or use additional tools beyond those required?**

   - If time allows, I would love to begin learning d3 and animate my visualizations for this project.



# MVP Goal: :bar_chart:

**1. What would a minimum viable product (MVP) look like for this project?**

  - My MVP will be a correlation chart and regression model using all variables collected for this project.

  ![footer](https://github.com/CeliaSagas/Data-Coin/blob/c33d8e47151a67585af6103b46f8282cdcc8a8fd/img/coin-spin-4.gif)
