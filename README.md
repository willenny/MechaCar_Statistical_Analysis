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

## Summary Statistics on Suspension Coils

- The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not?

![total summary](https://user-images.githubusercontent.com/109091887/200959481-3fd82af4-0cfa-4399-81d3-96d041f87bcd.PNG)

In total, the variance of the suspension coils is about 62.3 psi. Therefore, the current manufacturing data meets this design specification for all manufacturing lots.

![lot summary](https://user-images.githubusercontent.com/109091887/200959803-be7fcc28-f966-4e78-9d84-442d1613a8a6.PNG)

Individually, the variance in the suspension coils for Lot 1, Lot 2, and Lot 3 are 0.98 psi, 7.47 psi, and 170.29 psi, respectively. Therefore, Lot 1 and Lot 2 meet this design specification, but Lot 3 has a variance greater than 100 psi so it does not meet this design specification. 

## T-Tests on Suspension Coils

![psi t test all lots](https://user-images.githubusercontent.com/109091887/200989685-8018f0f2-fa0a-4b5c-a262-df42fbfaabfe.PNG)

Assuming our significance level was the common 0.05 percent, our p-value of 0.06% is above our significance level. Therefore, we do not have sufficient evidence to reject the null hypothesis, and we would state that the PSI across all manufacturing lots is not statistically different from the population mean of 1,500 pounds per square inch.

![t test lot 1](https://user-images.githubusercontent.com/109091887/200990090-c4e5e184-5e8e-4a28-922e-ec1641d82c6b.PNG)

When completing a t test between lot 1 and the population, our p-value of 1 is above our significance level. This is due to manufacturing lot having a mean psi of 1,500, which is the same as the population. Therefore, we do not have sufficient evidence to reject the null hypothesis, and we would state that the mean PSI in manufacturing lot 1 is not statistically different from the population mean of 1,500 pounds per square inch.

![t test lot 2](https://user-images.githubusercontent.com/109091887/200990445-7e52ce0d-39aa-4004-97d3-e895fb9dd8fa.PNG)

When completing a t test between lot 2 and the population, our p-value of 0.61 is above our significance level. Therefore, we do not have sufficient evidence to reject the null hypothesis, and we would state that the mean PSI in manufacturing lot 2 is not statistically different from the population mean of 1,500 pounds per square inch.

![t test lot 3](https://user-images.githubusercontent.com/109091887/200990803-4efd9cad-49b2-4759-9e90-7918879c479f.PNG)

When completing a t test between lot 3 and the population, our p-value of 0.04 is below our significance level. Therefore, we do have sufficient evidence to reject the null hypothesis, and we would state that the mean PSI in manufacturing lot 3 is statistically different from the population mean of 1,500 pounds per square inch.

## Study Design: MechaCar vs Competition

- What metric or metrics are you going to test?

In order to determine how MechaCars perform against their competition several metrics of interest would be: cost, engine type, safety rating, reliability, fuel economony, and odometer reading.

- What is the null hypothesis or alternative hypothesis?

The null hypothesis is that the mean difference in the safety rating between MechaCar and it's competitor is zero. The alternative hypothesis is that the mean difference in safety rating between MechaCar and it's competitor is not zero. 

- What statistical test would you use to test the hypothesis? And why?

In order to test the hypothesis, a two-sample t-tests can be used to compare MechaCar's safety rating with it's competitor's safety rating, each coming from a their population of cars. More specifically, a pair t-test can be completed because we want to pair observations in one dataset with observations in another. 

- What data is needed to run the statistical test?

Firstly, each sample size needs to be reasonably large. Generally speaking, this means that the sample data distribution should be similar to its population data distribution. Increasing the sample size until it's distribution resembles the population distribution would ensure an appropriate amount of data. In each sample, the safety rating data would need to be collected fo each car.
