# Case Study 2 - Doing Data Science


__Objective__

We have been hired by the __DDSAnalytics__ that specializes in talent management solutions for Fortune 100 companies, with the objective of predicting employee turnover using the existing employee data. These objectives include:
1. identify top 3 factors that lead to attrition
2. job role specific treands _(e.g., highest job satisfaction)_
3. build a model to predict attrition


__Executive Summary__
Please refer to this youtube clip for recorded presentation (<5mins) 

[![CaseStudy 2 DDS](http://img.youtube.com/vi/_qAkuMxDMnU/0.jpg)](http://www.youtube.com/watch?v=_qAkuMxDMnU "2019 Employee Report")

In summary to the objective, we found:

* Employee attrition– whre employees that were most likely to turnover are those that (1) most importantly workovertime and (2) have lower salaries. Also, we saw decreased in job involvement and increased time_till_promotion. 
* In terms of monthly income – Job Role and Job Level were key to predicting salary
* Age and Gender – Good news!  Yall are on the right track with employee management as both Age and Gender were not significant factors or indicators used in the models. We would indicate that there is a slight tendacy for those younger  in age to be more likely to leave. This was appartent in the Employee attrition model werhe maritial status = single, but Age itself was not a key factor. Contrary to other industries, the dataset provided indicated no significant indication gender was a key factor in turnover or a wage gap.


#### Repo Setup
* CaseStudy - powerpoint, rmd and html
* ~\data\ - original data and submisison files

#### Data Dictionary

```
'data.frame':	870 obs. of  36 variables:
 $ ID                      : int  1 2 3 4 5 6 7 8 9 10 ...
 $ Age                     : int  32 40 35 32 24 27 41 37 34 34 ...
 $ Attrition               : Factor w/ 2 levels "No","Yes": 1 1 1 1 1 1 1 1 1 1 ...
 $ BusinessTravel          : Factor w/ 3 levels "Non-Travel","Travel_Frequently",..: 3 3 2 3 2 2 3 3 3 2 ...
 $ DailyRate               : int  117 1308 200 801 567 294 1283 309 1333 653 ...
 $ Department              : Factor w/ 3 levels "Human Resources",..: 3 2 2 3 2 2 2 3 3 2 ...
 $ DistanceFromHome        : int  13 14 18 1 2 10 5 10 10 10 ...
 $ Education               : int  4 3 2 4 1 2 5 4 4 4 ...
 $ EducationField          : Factor w/ 6 levels "Human Resources",..: 2 4 2 3 6 2 4 2 2 6 ...
 $ EmployeeCount           : int  1 1 1 1 1 1 1 1 1 1 ...
 $ EmployeeNumber          : int  859 1128 1412 2016 1646 733 1448 1105 1055 1597 ...
 $ EnvironmentSatisfaction : int  2 3 3 3 1 4 2 4 3 4 ...
 $ Gender                  : Factor w/ 2 levels "Female","Male": 2 2 2 1 1 2 2 1 1 2 ...
 $ HourlyRate              : int  73 44 60 48 32 32 90 88 87 92 ...
 $ JobInvolvement          : int  3 2 3 3 3 3 4 2 3 2 ...
 $ JobLevel                : int  2 5 3 3 1 3 1 2 1 2 ...
 $ JobRole                 : Factor w/ 9 levels "Healthcare Representative",..: 8 6 5 8 7 5 7 8 9 1 ...
 $ JobSatisfaction         : int  4 3 4 4 4 1 3 4 3 3 ...
 $ MaritalStatus           : Factor w/ 3 levels "Divorced","Married",..: 1 3 3 2 3 1 2 1 2 2 ...
 $ MonthlyIncome           : int  4403 19626 9362 10422 3760 8793 2127 6694 2220 5063 ...
 $ MonthlyRate             : int  9250 17544 19944 24032 17218 4809 5561 24223 18410 15332 ...
 $ NumCompaniesWorked      : int  2 1 2 1 1 1 2 2 1 1 ...
 $ Over18                  : Factor w/ 1 level "Y": 1 1 1 1 1 1 1 1 1 1 ...
 $ OverTime                : Factor w/ 2 levels "No","Yes": 1 1 1 1 2 1 2 2 2 1 ...
 $ PercentSalaryHike       : int  11 14 11 19 13 21 12 14 19 14 ...
 $ PerformanceRating       : int  3 3 3 3 3 4 3 3 3 3 ...
 $ RelationshipSatisfaction: int  3 1 3 3 3 3 1 3 4 2 ...
 $ StandardHours           : int  80 80 80 80 80 80 80 80 80 80 ...
 $ StockOptionLevel        : int  1 0 0 2 0 2 0 3 1 1 ...
 $ TotalWorkingYears       : int  8 21 10 14 6 9 7 8 1 8 ...
 $ TrainingTimesLastYear   : int  3 2 2 3 2 4 5 5 2 3 ...
 $ WorkLifeBalance         : int  2 4 3 3 3 2 2 3 3 2 ...
 $ YearsAtCompany          : int  5 20 2 14 6 9 4 1 1 8 ...
 $ YearsInCurrentRole      : int  2 7 2 10 3 7 2 0 1 2 ...
 $ YearsSinceLastPromotion : int  0 4 2 5 1 1 0 0 0 7 ...
 $ YearsWithCurrManager    : int  3 9 2 7 3 7 3 0 0 7 ...
```
