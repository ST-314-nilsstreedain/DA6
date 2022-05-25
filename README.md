# Data Analysis 6 - T Procedures
## Part 1. (13.5 points)
The microbeersS22.csv dataset is a representative sample of 100 microbrews from around the United States. The variable abv represents the percent of alcohol by volume for each craft beer. According to the National Institute of Health, one standard serving of alcohol is 12 ounces of regular beer, which is usually about 5% alcohol by volume (abv).

Does the sample of microbrews provide evidence the average alcohol by volume of all craft beers is different from a standard serving of beer at 5% abv?

Use this dataset and the R script DA5_t_procedures.R to complete the following:

1. (1 point) What is the parameter of interest in this scenario? Provide the symbol and context.
```
μ: mean % abv for each beer
```
2. (1 point) State the null and alternative hypothesis to answer the question of interest.
```
H0: μ = 5
Ha: μ ≠ 5
```
3. (1 point) Make a histogram or boxplot to visualize the variable abv.  Is there visual evidence the average alcohol by volume is different than 5%?
```
This shows an average around 5.5%, rather than 5%.
```
4. (1 point) Calculate the sample mean and standard deviation using R. State the values.
```
Mean: 5.902
SD: 1.467698
```
5. (1 point) Check the conditions for inference. State them and whether they are met.
```
The sample must be reasonably large, aka n >= 30. 100 is greater than 30
```
6. (1 point) Calculate the test statistic by hand.  Show work.
```
t = (x - μ)/(sd/n1/2)
= (5.902 - 5)/(1.467698/1001/2) = .902/0.146798
= 6.1445
```
7. (1 point) State the p-value. Is it one or two sided?
```
The p-value is 1.676e-08. It is two sided because the null hypothesis is two
sided.
```
8. (1.5 points) Calculate the 95% Confidence Interval by hand. Show work.
```
95% = 5.902 +- 1.96(1.467698/1001/2) = 5.902 +- 1.96(1.467698/10)
= 5.902 +- 1.96(0.1467698)
= 5.902 +- .288
= [5.614331, 6.189668]
```
9. (1 point) Use the t.test() command in R to verify the results of the t test. For details on the t.test() function, please read the comments written in the DA6_t_procedures.R script. How do your answers compare?
```
The answers are extremely similar, slightly off likely due to rounding errors
with my calculator.
```
10. (4 points) From the R output, write a four-part conclusion describing the results. Use a = 0.05. Provide a statement in terms of the alternative hypothesis. State whether (or not) to reject the null. Give in context an interpretation of the point and interval estimate.  Include any other information you might feel to relevant.
```
H0:μ=5
Ha: μ ≠ 5
Test-sta5s5c: 6.1445
P-value: 1.676e-08

We reject the null hypothesis H0: μ = 5 because the p-value is less than the
significance level (0.05). Our sample data provides sufficient evidence that the
average alcohol by volume is significantly different from 5%.
```
## Part 2. (9.5 points)
A winery bottles 1000’s of bottles of wine per season. The winery has a machine that automatically dispenses the amount of wine per bottle. Each season the wine maker randomly samples **35 bottles** of wine to ensure the amount of wine per bottle is **750 ml**. If there is evidence that the amount is **different than** (less or more than) 750 ml the winery will need to evaluate the machine and perhaps rebottle or consider selling the wine at a discount. The **sample** yields a mean of -x = **746.4 ml** and standard deviation s = **7.7** ml. Use a significance level of 0.05.

**State: Is there sufficient evidence that the average fill of the wine bottles is different than 750 milliliters?**

### Plan:
1. (1 point) State the null and alternative hypotheses to answer the question of interest.
```
H0: μ = 750Ha: μ ≠ 750
```
2. (1 points) Check conditions for inference. List the conditions and state whether they are met.
```
The sample must be reasonably large, aka n >= 30. 35 is greater than 30
```

### Solve:
3. (1 point) Calculate the test statistic and degrees of freedom. Show work.
```
t = (x - μ)/(sd/n1/2)
= (746.4 - 750)/(7.7/351/2) = -3.6/1.30154
= -2.76596

DF = n -1 = 34
```
4. (1 point) What is the p-value for the test?
```
P-value = 0.00913
```
5. (1.5 points) Calculate a 95% confidence interval for µ. Show work.
```
95% = 746.4 +- 1.96(7.7/351/2) = 746.4 +- 1.96(7.7/5.91608) = 746.4 +- 1.96(1.30154)
= 746.4 +- 2.55101
= [743.84899, 748.95101]
```

### Conclude:
6. Write a four-part conclusion describing the results. 
   - (1 point) Provide a statement in terms of the alternative hypothesis. 
   - (1 point) State whether (or not) to reject the null.
   - (1 point) Give an interpretation of the point and interval estimate.  
   - (1 points) Include context.  
```
H0: μ = 750
Ha: μ ≠ 750
Test-statistic: -2.76596
P-value: 0.00913

We reject the null hypothesis H0: μ = 750 because the p-value is less than the
significance level (0.05). Our sample data provides sufficient evidence that the
amount of wine per boele is significantly different from 750ml.
```

## Gradescope Page Matching (2 points)
When you upload your PDF file to Gradescope, you will need to match each question on this assignment to the correct pages. Video instructions for doing this are available in the Start Here module on Canvas on the page “Submitting Assignments in Gradescope”. Failure to follow these instructions will result in a 2-point deduction on your assignment grade. Match this page to outline item “Gradescope Page Matching”.
