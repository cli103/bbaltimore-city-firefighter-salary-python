# Regression Analyses for Baltimore City Fire Fighter Salaries
## Background

I used Microsoft Excel to conduct data analysis on the annual salary of fire fighters in Baltimore City. I used open data from the Baltimore City government on employee salaries from 2011 – 2020 to generate a regression model to predict the future annual salary of fire fighters. 

I also used Python on Google Colabatory to repeat this analysis.

## Business Question
Can we predict the annual salary of Baltimore City fire fighters based on data from previous years?

## Data Sources – Open Data
[Baltimore City Government Employee Salaries](https://data.baltimorecity.gov/datasets/baltimore-employee-salaries).
The relevant file can be found [here](https://github.com/cli103/baltimore-city-firefighter-salary/blob/main/Baltimore_City_Employee_Salaries.csv)

## Data Analysis
Find step-by-step instructions [here](https://github.com/cli103/baltimore-city-firefighter-salary/blob/main/excel-instructions)

I generated a simple linear regression model pictured below. 

![alt text](https://github.com/cli103/baltimore-city-firefighter-salary/blob/main/Simple%20Regression%20Annual%20Salary.png)

As labeled, the best fit line is y = 0.5718x + 18668 and the r squared value is 0.3127. This means that a one dollar difference in the previous year’s salary is associated with a 0.5718 dollar difference in the current year’s salary. As the r squared value is quite low, the model only represents around 31% of the variation in a fire fighter’s average annual salary is explained by their salary from the previous year. The standard error of the residual is 6679.82. The p-value is 0.12 which is greater than 0.05, meaning that the average annual salary of the previous year is not a significant predictor of the annual salary in the current year. As a result, the regression model does not seem to provide an accurate prediction of the annual salary of Baltimore City firefighters.

I recreated this data exploration using Python in Google Colaboratory and generated the following [model](https://github.com/cli103/bbaltimore-city-firefighter-salary-python/blob/main/plotly_scatter_salary.html).

The line best fit is y = 0.384046x + 23500.203537 and the r squared value is 0.501226. This means that a one dollar difference in the previous year’s salary is associated with a 0.384046 dollar difference in the current year’s salary. The r squared value is somewhat low as the model represents around 50% of the variation in a fire fighter’s average annual salary is explained by their salary from the previous year. The regression analysis generated using Python differs slighty to the regression analysis generated by Excel. This could be due to the difference in the years of data used. The excel analysis forms a regression analysis of data from 2011 - 2020 whereas the Python analysis forms a regression analysis of data from 2014-2020. I am unsure why this occured as I used the same filtering techniques on the Python data frame as I did in Excel. However, the Python analysis indicates that in later years, the prediction of annual salary based on the previous year's annual salay is a little more accurate and the increase in annual salary year over year has decreased from 2014 onwards.

This data may be important for the Baltimore City Fire department to consider when setting the annual salary for fire fighters. A sudden decrease in average salary such as from 2015 – 2016 may affect the retention of fire fighters as well as the longevity of the career path. In 2016, the amount of fire fighters in the Baltimore City Fire Department decreased from 45 to 5. This is due to the civil unrest in Baltimore that occurred in 2015, whereby a lot of fire trucks were damaged by rioters. However, following this incident, the average salary of fire fighters has not grown significantly year over year, this is evident in the Python analysis. If annual salary does not grow year over year, people may be discouraged from becoming a fire fighter. Other data that may improve this model include number of fire fighters, years worked and differences between part time and full time salaries. This may provide more information regarding why the average annual salary has declined significantly since 2015. 
