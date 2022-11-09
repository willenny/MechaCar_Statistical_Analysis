# MechaCar_Statistical_Analysis

## Linear Regression to Predict MPG
![summary script](https://user-images.githubusercontent.com/109091887/200946616-6e765e74-53e9-42c6-ac27-f3c2b9b1f454.PNG)

- Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?
In the summary output, each Pr(>|t|) value represents the probability that each coefficient contributes a random amount of variance to the linear model. According to our results, vehicle length and ground clearance (as well as intercept) are statistically unlikely to provide random amounts of variance to the linear model due to their p-values being less than 0.05%. In other words the vehicle length and ground clearance have a significant impact on miles per gallon. (Source: 15.7.3)

![lm script](https://user-images.githubusercontent.com/109091887/200947790-16ebcb9a-a877-445a-afb6-efe12caebcb0.PNG)

- Is the slope of the linear model considered to be zero? Why or why not?
The output of multiple linear regression using the lm() function produces the coefficients for each variable in the linear equation. Therefore, the linear regression model for our dataset would be .Because multiple linear regression models use multiple variables and dimensions, they are almost impossible to plot and visualize. 

- Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?
