java c
POPH90145 - 2024
Survival Analysis and Regression for Rates
Assignment 2 - Questions
Due: Friday 25th  October, 11:00 pm (Melbourne time)
The maximum mark for this assignment is 80. It forms 40% of the final grade for this subject. Your assignment should be submitted via Gradescope as a PDF document.
Please put your student ID number in the header of the document.
Unless you are asked to do so in the question, please do not include any Stata output directly in your assignment document. Instead, format any results you want to show in away that would be suitable for inclusion in a report or journal article.
This Assignment has 7 questions. You should attempt all questions.
For this assessment, you will need to download and use the data file POPH90145_Assignment2.dta from Canvas.
Perform. all Stata tasks via a do-file (you can use the do-files from the Stata practicals located on Canvas as a guide). You will need to include a copy of the Stata commands used to complete your assignment.
Trialling tolerability of a new medication for diabetes
In this study, researchers are investigating a new medication for Type 2 diabetes called “TrialMed” . You have been provided with health records of patients who have been started on this medication
and were followed up. An important concern for the researchers is the rate at which patients stopped taking TrialMed due to side effects.
Research aim: The hospital researchers would like to identify risk factors that are associated with time to stopping TrialMed, a new medication for Type 2 diabetes.
Table 1: Description of the variables in the dataset
Variable name
Description
id
Unique ID of patient
sex
Sex of patient (1 = Female; 2 = Male)
birthdate
Dateofbirth
startdate
Date when patient was started on TrialMed
bmicat
Body mass index (BMI) category
(0 = Normal; 1 = Underweight; 2 = Overweight; 3 = Obese)
hba1c
HbA1c (a measure of diabetes control) when TrialMed was started
(1 = <7%; 2 = 7 to < 8%; 3 = 8 to < 9%; 4 = ≥ 9%)
diabetes_treatment
Diabetes treatment regimen when TrialMed was started
(1 = Tablets only; 2 = Insulin only; 3 = Tablets and insulin)
diabetes_educator
Diabetes educator review - Was the patient seen by a diabetes educator before starting TrialMed? (0 = No; 1 = Yes)
stopdrug
Did the patient stop TrialMed? (0 = No; 1 = Yes)
exitdate
Date when patient stopped TrialMed or was censored


Question 1. Descriptive statistics and data manipulation [18 marks]
a)   The hospital researchers want to use survival analysis to identify risk factors that are associated with time to stopping TrialMed. This means that the key event of interest for analysis is the time to stopping TrialMed for each patient. What is a sensible choice for the time of analysis (i.e. the time axis) for this study? Please explain your answer. [1 mark]
b)  Calculate the follow-up time (in years) for participants in the study. Present a table of the distribution of follow-up time for patients by sex, BMI category, HbA1c and diabetes treatment, in a format that is suitable for publication. [5 marks]
c)   How many obese male participants were seen by a diabetes educator before starting TrialMed? List the 5 smallest IDs. [2 mark]
d)  Of all the overweight males that stopped TrialMed, how many were on insulin only at the time TrialMed was started? List the 5 smallest IDs. [2 marks]
e)   What proportion of females were on insulin only before starting TrialMed? [1 mark]
f)   Calculate the age of each patient (in years) at the time of starting TrialMed (age).
Provide a table summarising the characteristics for participants in this study in a format suitable for publication. These characteristics include age at the time of starting TrialMed, sex, BMI category, HbA1c, diabetes treatment regimen and whether the patient was seen by a diabetes educator before starting TrialMed. [7 marks]




Question 2. Kaplan-Meier estimate of the survivor function [14 marks]
a)    Use Stata to plot the Kaplan-Meier estimate of the overall survivor curve and include this plot in your assignment. Based on the plot only, estimate the median survival time to stopping TrialMed for patients in this study. [2 marks]
b)   Use Stata to plot the Kaplan-Meier survivor function estimates for each category of sex and include this plot in your assignment. Based on this plot only, briefly describe differences, if any, between the probability of stopping TrialMed in males and females in this study. [2 marks]
c)    Plot the Kaplan-Meier estimates of the survivor function for each category of BMI and include this plot in your assignment. Comment on the possible relationship between BMI and the probability of stopping TrialMed. Test whether there are any differences in survival between different BMI categories and explain your results. [4 marks]
d)   Use Stata to complete the two tables below. The two tables list estimates of the survivor function for each category of BMI for females and males, separately. [2 marks]
Females only
Survivor function
BMI
Normal
Underweight
Overweight
Obese



Time
1 year




2 years




3 years




4 years




5 years





Males only
Survivor function
BMI
Normal
Underweight
Overweight
Obese



Time
1 year




2 years




3 years




4 years




5 years








e)    Create  a new categorical variable agecat which categ代 写POPH90145 – 2024 Survival Analysis and Regression for Rates Assignment 2 – QuestionsJava
代做程序编程语言orises age at the time of starting TrialMed as follows:


Age (years)                 agecat
<35 years                       0
35 to <50 years               1
50 to <65 years               2
65 or more years              3


Use Stata to plot the Kaplan-Meier survivor function estimates for each category of agecat and include this plot in your assignment. Based on this plot, comment on the possible relationship between the age categories and the survival probability of stopping TrialMed.
Test whether there are any differences in survival between the different age groups and explain your results. [4 marks]
Question 3. Univariable Cox regression [13 marks]
a)   Use univariable Cox regression to estimate the effect of age (as a continuous variable), sex, BMI category, HbA1c, diabetes treatment and diabetes educator review on the hazard of stopping TrialMed. Present these results in a table suitable for publication. [7 marks]
b)  Interpret your results for the univariable Cox regression model for BMI category and for age.  [6 marks]
Question 4. Checking the proportional hazards assumption [6 marks]
a)  Use an appropriate visual assessment to test whether the proportional hazards assumption is satisfied for the exposure diabetes_educator and include the plot in your assignment. Based on the plot only, comment on whether the proportional hazards assumption is satisfied. [2 marks]
b)  Use a statistical test to test the proportional hazards assumption for the variable diabetes_educator and for the variable bmicat. Interpret the results. [4 marks]


Question 5. Multivariable Cox regression [21 marks]
The main exposure of interest for the researchers was diabetes educator review before starting TrialMed (diabetes_educator). The researchers constructed the following causal diagram for the association between diabetes educator review and time to stopping TrialMed. 

a)   Based on the above causal diagram, fit a multivariable Cox regression model to assess the association  between  diabetes  educator  review  (diabetes_educator)  and  time  to  stopping TrialMed. Consider the scale of any continuous variable in your model. Present the results of this regression model in a table suitable for publication. Interpret the results of the association between diabetes educator review and time to stopping TrialMed from this model. [8 marks]
b)  Investigate if the association between diabetes educator review (diabetes_educator) and
time to stopping TrialMed is modified by age (age), adjusting for the potential confounders identified in Question 5a. [3 marks]
c)   Investigate if the association between diabetes educator review (diabetes_educator) and
time to stopping TrialMed is modified by sex (sex), adjusting for the potential confounders identified in Question 5a. [3 marks]
d)  The investigators are also interested in the association between diabetes educator review
(diabetes_educator) and time to stopping TrialMed, after adjusting for age, sex and HbA1c at the start of the study (hba1c). However, the investigators believe that there is evidence against the null hypothesis that the proportional hazards assumption is met for HbA1c.
Fit two models: 1) a standard Cox regression model of the association between diabetes educator review and time to stopping TrialMed, after adjusting for age, sex and HbA1c; and 2) a stratified Cox regression model of the association between diabetes educator review and  time to stopping TrialMed by the variable violating the proportional hazards assumption (hba1c), and also adjusting forage and sex. Present the results of the two models and comment on the differences in results, if any. [3 marks]
e)   The investigators believe that there is evidence against the proportional hazards assumption for the exposure variable diabetes educator review (diabetes_educator) in the multivariable Cox regression model fitted in Question 5a.
Why can we not handle the violation of the proportional hazards assumption for the exposure variable diabetes_educator using a stratified Cox regression model?
Fit a multivariable Cox regression model that allows for a different hazard ratio for the exposure diabetes_educator at time [0-1) year and 1+ years, adjusting for the same potential confounders as in Question 5a. Present and describe these results.  [4 marks]
Question 6. Stata Do file [3 marks]
a)  Please provide a copy of your  Stata do-file for performing the statistical analyses for this assignment. Do not upload a second file when submitting your assignment but instead copy and paste the Stata do-file to your Word document. [3 marks]
Question 7. Kaplan-Meier estimator of the survivor function [5 marks]
You do not needStata for this question.You have been given data from a cohort study of 15 individuals diagnosed with stomach cancer where the main event of interest is death after cancer diagnosis. The investigators of the study followed-up these 15 individuals for a maximum of 2 years after diagnosis of cancer and recorded the following data:
ID
Follow-up Time
(months)
Died?
(0 = No; 1 = Yes)
1
5
1
2
8
1
3
12
0
4
3
1
5
17
0
6
18
0
7
12
1
8
12
0
9
14
1
10
20
0
11
15
1
12
10
1
13
4
1
14
7
0
15
5
0Compute the Kaplan-Meier estimate of the population survivor function. Please show your working. Use the estimated survivor function to predict the probability of survival after cancer diagnosis at 18 months. [5 marks]





         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
