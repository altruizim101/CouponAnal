# Project 1: Data Analysis & Visualization
## Task: Answer the question - “Will customer accept coupon?” 

## (Goal & Objective)
The goal of this project is to use recently developoed skills about data visualizations and probability distributions to distinguish between customers who accepted a driving coupon versus those who did not.
The survey data describes different driving scenarios, including the destination, current time, weather, and passenger, and then asks people whether they will accept the coupon if they are the driver. 

## (Project Plan)
## There are three possible answers people can choose from:
- “Right away”
- “Later, before the coupon expires”
- “No, I do not want the coupon”

## Deliverables
The final submission should include the Practical Application 1 Jupyter Notebook and other relevant files, such as the dataset provided and uploaded to a GitHub repository as a first portfolio project. To explore the data, utilize knowledge of pandas and Python to create statistical summaries demonstrating differences in those who accepted and rejected the coupon. Utilize the Matplotlib and Seaborn libraries to create a visualization using Python. Ensure that the findings are clearly stated in a separate section alongside actionable items and recommendations.

## Links to Project Deliverables
- READMe file with a summary of findings here >> https://github.com/altruizim101/CouponAnal/edit/main/README.md
- Link to Jupyter notebook here >> http://localhost:8888/notebooks/Downloads/assignment5_1_starter/Project1_July23.ipynb?
- Data Visualization >> https://github.com/altruizim101/CouponAnal

## (Data Understanding)
I reveiwed features and attributes of the data, using Pandas tool and its functions. I loaded the data using:
data.head(), data.sample(), ...


## (Data Preparation)
Checked for Null (NaN) values in "Y" column and coupon type used for analysis ("Bar" coupon type). From "data.info()" summary,
1) The "Y" column has no missing values (12684 non Null values).
2) the "Bar" column has 107 missing vaues (1264 - 12577).
Action: remove missing (NaN) data in "Bar" column


## (Modeling & Evaluation)
  After data cleaning, I evaluated response rate by considering different attributes in the data, including coupon type, driver income, education, marital status. The evaluation includes
  data analysis with Pandas and plots of the distributions by attributes to reveal trends or correlation.

### Data Analysis with Pandas & Findings
  Data analysis revealed the following - 
  The proportion of drivers that accepted coupon overall is:
  - "Y" = 1, response = 56.9%
  - "Y" = 0, response = 43.1%

  From Histogram plot in Fig.2, data shows more 80degree days, followed by 55degrees, and then 30degrees.
  
  For "Bar" coupon, the proportion of drivers that accepted coupon is:
  - "Y" = 1, response = 58.9%
  - "Y" = 0, response = 41.1%

  Acceptance rate of "Bar" coupon for drivers that go 3 or less times is:
  - "Y" = 1, response = 64.7%
  - "Y" = 0, response = 35.3%

  Acceptance rate of "Bar" coupon for drivers that go 4 or more times is:
  - "Y" = 1, response = 64.9%
  - "Y" = 0, response = 35.1%

  The acceptance rate for the "above 25yrs olds" group is:
  - "Y" = 1, response = 61.5%
  - "Y" = 0, response = 38.5%
    and is higher when compared to acceptance rate for "all others"
  - "Y" = 1, response = 56.7%
  - "Y" = 0, response = 43.3%

  The Acceptance rate for "drivers who go to bars more than once a month and had passengers that were not a kid and had occupations other than "farming, fishing, or forestry"
  is less than "above 25yrs olds" scenario above, and is equal to "all others" scenario as shown above.
  - "Y" = 1, response = 56.7%
  - "Y" = 0, response = 43.3% 

The proportions are as follows when comparing the acceptance rates between those drivers who:

a) go to bars more than once/ month, passengers are non-kid, & not widowed:
"Y" = 1, response = 56.5 and "Y" = 0, response = 43.5%
  
b) go to bars more than once a month and are under the age of 30:
"Y" = 1, response = 50.4% and "Y" = 0, response = 49.6%

c) go to cheap restaurants more than 4 times/ month and income less than 50K:
"Y" = 1, response = 65.3% and "Y" = 0, response = 34.7%

Overall Observations above for "Bar" coupon reveals that drivers who accepted the coupons are generally 25+ yrs old, opt more often for low budget restaurant (< $20 range) including carry out& Takeouts, are low-income earners (< $50K) tend to do "carry out& Takeouts" more often than others, and tend to accept coupons more often on 80degree days.

### Data Visualization - Plots & Findings
- Fig 1: The barplot shows highest response rate for "Restaurant(<20)" and "carry out& Takeout" coupons, followed by "coffee house". The "Bar" category coupons ranked the lowest.
- Figure2: The histogram shows most frequent 80-degree days, followed by 55degrees, and then 30degrees.
- Figure3: In addition to type of coupon, other "attributes" of data considered for further insight. I looked at "marital status", "education", and "income" on acceptance rate.
  In marital status case, the "singles" showed highet acceptance rate and "widowed" with lowest acceptance rate.
  In education case, "some high school" shows highest coupon acceptance rate while graduate degree shows lowest.
  In "income" scenario, we see low accpetance rate for earners above $75K
- Figure4: The heatmap does not reveal much in terms of correlation in parameters.
- Figure5: shows sample distribution based on education - highest with some college and bachelors degree.
- Figure6: shows sample distribution based on marital status - "married partner" & "single" categories with largest.
- Figure7: shows sample distribution based on income, with $25K - $37.5K having the highest. Interesting to note, above $75K earners also included in coupon data.
- Figure8: The mostly sunny days for coupon clearly makes sense, as drivers will be more inlcined compared to rainy or snowy days.


## Independent Investigation
Using the bar coupon example as motivation, explore one of the other coupon groups and try to determine the characteristics of passengers who accept the coupons.

## Carryout & take Away" coupons
We exploring acceptance Rate for "Carryout & take Away" coupons. For this scenario, we discovered the following:

proportion of drivers accepted "Carryout & take Away" coupon
- "Y" = 1, response = 56.7%
- "Y" = 0, response = 43.3%

Acceptance rate between those who went to "Carry away & take out" 3 or fewer times a month
- "Y" = 1, response = 62.4%
- "Y" = 0, response = 37.6%

Acceptance rate of "Carry away & take out" coupon 4 or more times
- "Y" = 1, response = 55.5%
- "Y" = 0, response = 44.5%






