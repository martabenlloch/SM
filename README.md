# SM
Question A
Consider the dataset regarding health insurance as provided in the file ”healthinsurancedata.txt”.
Y This is the response variable. It indicates whether (Y = 1) or not (Y = 0) the client has claimed
more than 5000 euro in the past 3 years.
x1 age the client’s current age in years
x2 sex 1 for female and 0 for male
x3 bmi body mass index (weight in kg/(height in m)2
)
x4 bloodpressure systolic bloodpressure in mm Hg.
x5 diabetic 1 for yes, 0 for no
x6 children the number of children the client has
x7 smoker 1 for yes, 0 for no
x8 region factor variable, indicating four regions in the country, roughly corresponding to northeast,
northwest, southeast and southwest.
You only work with a subset of 700 observations, depending on your student number.
You only work with your subset mydataA
Data.A =read.table("healthinsurancedata.txt",header=T)
studentnumber=0123456 # fill in your student number here, this is an example!
set.seed(studentnumber)
rownumbers = sample(1:nrow(Data.A),size=700)
mydataA = Data.A[rownumbers,]
A.1 Perform a model search using AIC to relate the outcome Y and the covariates in the dataset.
(a) Report in general terms (without listing them all) which models were part of the search and
which search method has been used.
(b) Report in correct mathematical notation the best 3 models of the search.
(c) Give a brief interpretation of the best model.
A.2 Start from the best model in A.1(b). If that model contains the variable x4 (bloodpressure), use
this model. If not, add variable x4 to the model. In this model, perform an order selection test
to test the null hypothesis that the effect of bloodpressure appears in a linear way in the model’s
linear predictor (in the terminology of the course notes). You do not test the other variables in
the model, but they stay in the model.
(a) Write both the null and the alternative hypothesis in correct mathematical notation.
(b) Explain which choices you made to perform the order selection test.
(c) Perform the test, report both the value of the test statistic and the p-value and state the
conclusion.
A.3 Representative R code for Question A.
