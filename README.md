# MechaCar_Statistical_Analysis

## Linear Regression to Predict MPG
![summary script](https://user-images.githubusercontent.com/109091887/200946616-6e765e74-53e9-42c6-ac27-f3c2b9b1f454.PNG)

- Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?

In the summary output, each Pr(>|t|) value represents the probability that each coefficient contributes a random amount of variance to the linear model. According to our results, vehicle length and ground clearance (as well as intercept) are statistically unlikely to provide random amounts of variance to the linear model due to their p-values being less than 0.05%. In other words the vehicle length and ground clearance have a significant impact on miles per gallon. 

![lm script](https://user-images.githubusercontent.com/109091887/200947790-16ebcb9a-a877-445a-afb6-efe12caebcb0.PNG)

- Is the slope of the linear model considered to be zero? Why or why not?

Because multiple linear regression models use multiple variables and dimensions, they are almost impossible to plot and visualize. The output of multiple linear regression using the lm() function does produce the coefficients for each variable in the linear equation though. Therefore, the linear regression model for our dataset would be: 

mpg = 6.267* vehicle_weight + 0.001245* vehicle_weight + 0.06877* spoiler_angle + 3.546* ground_clearance + -3.411* AWD + -1.04.

That being said, due to the complexity of the slope in a multiple linear regression model, we cannot determine one singular slope value. We could view the Estimate values for each independent variable to understand their individual slope with respect to the dependent variable, mpg. For instance, the Estimate for vehicle length is 6.267, meaning for each one unit increase in vehicle length (presumably in feet), the miles per gallon will increase by 6.267. When observing each Estimate value, it would be acceptable to say that vehicle length, ground clearnce, and AWD have nonzero slopes, whereas vehicle weight and spoiler angle have zero slopes. 

- Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?

In order to determine the effectiveness in predicting outputs we will use our p-value and our r-squared value. From our summary, the r-squared value is 0.7149, which means that roughly 71% of the variablilty of our dependent variable (miles per gallon prediction) is explained using this multiple linear model. In addition, the p-value of our linear regression analysis is 5.35 x 10-11, which is much smaller than our assumed significance level of 0.05%. Therefore, we can state that there is a significant relationship between the independent variables and miles per gallon, which would suggest this linear model predicts miles per gallon effectively. 

(Source: 15.7.3)
