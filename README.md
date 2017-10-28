## Statistical Inference: Capital Bikeshare Ride Time Prediction
The Capital Bikeshare Ride Time Prediction project looks to predict the ride time between two stations depending on different factors like weather conditions, day of the week, season, or holidays. The purpose of the analysis is to determine if the differences in ride times found in the visual exploratory data analysis are truly found in the data or if they just happened by chance.

## Central Limit Theorem
The Central Limit Theorem (CLT) is the main piece needed to conduct the statistical analysis in the report. The CLT states that the distribution of xbar (the sample mean), or a point estimate (like a proportion or correlation coefficient, is approximately normal under certain conditions, listed below:
Independence
Sampled Observations must be independent of each other
The sample should be randomly sampled
If sampling without replacement, the sample size should be less than 10% of the population
Sample Size/Skew
If the distribution is skewed, then the sample size needs to be increased in order for the distribution of the point estimate to be normal
<br>
<br>
For the tests done in this analysis, a random sample of 100,000 rows from the 1.1 million rows of bike rides were analyzed. Each row is independent of the other rows as one ride does not depend on the previous or future rides. The data were sampled without replacement and are less than 10% of the total number of bike rides. The distribution of the ride time is skewed to the right but this is overcome because of the large sample size. Because the CLT conditions are met, we can apply the CLT for the hypotheses tests and confidence intervals using the normal distribution.

## Statistical Tests Used
In this analysis, the normal distribution is used for the tests. However, instead of using the z-distribution, the t-distribution is used because the standard deviation of ride time for the entire population is not known. The tests used in this analysis include t-tests for differences in means, 95% confidence intervals for differences in means, and Analysis of Variance (ANOVA) to test differences in means for more than two means.
<br>
<br>
In most cases, the significance level (alpha) was 0.05 but for t-tests used after an ANOVA test, the alpha is lowered using the formula k(k - 1) / 2, where k is the number of groups.

## Conclusions from Tests
After some visual exploratory analysis, the difference in ride times differed greatly between registered and casual riders (13.71 minutes differences). A t-test was used to determine if this was by chance or if there actually is a difference in the mean ride times between the two sets of riders. Based on the test results, the mean ride times between the groups were different and . This result is a key finding and was used throughout the analysis.
<br>
<br>
An ANOVA test with additional t-tests were conducted to determine if the mean ride times for the different seasons (spring, summer, fall, and winter) were different. The analysis found that there were differences between all of the months and when factoring in rider type, the differences in ride times within the same season were also all different. The second part of the analysis (factoring in rider type) is consistent with the initial test where casual riders had longer rides than registered riders.
<br>
<br>
The data contains a weather category variable (sunny, cloudy/misty, and rainy/snowy/stormy) and additional tests (ANOVA and t-tests) were conducted to determine if the ride times were different when looking at the different categories and rider types. The tests provided proof that there were differences between all of the ride times and were even larger when factoring in rider type within a single category.
<br>
<br>
The same tests were done to determine if holidays/non-holidays and workdays/non-workdays also had an impact on the ride times. As with the weather category and the seasons, the tests provided evidence that the mean ride times were different for holidays and non-holidays and for workdays and non-workdays. And like the other tests, the differences were even more evident when rider type was factored within single categories (ex. Casual riders on holidays vs. registered riders on holidays). 
<br>
<br>
The data does contain contain three quantitative variables: normalized temperature, humidity, wind speed, and miles between two stations. Tests were conducted to determine if there was a correlation between each variable with the ride time and in each case there was a correlation. However, the correlation values for humidity, wind speed, and temperature were close to 0, meaning there is not a strong correlation between these variables. The correlation between the ride time and miles had a correlation of 0.4 so the correlation is much stronger than the other two variables.

## Impacts to Ride Time Prediction
This analysis provided key insights as to which factors lead to increased or decreased ride times. The rider type seems to play a large role in the ride times. Season, weather, holidays, and workdays also play a role in how long a ride might take. When the rider type is factored into those four variables, the differences in ride times is very similar to the actual differences in ride times only between the rider type. These variables will more than likely be included the models that will be used to determine ride times. The miles between two stations could also be a determining factor in the length of a ride.
<br>
<br>
While the temperature, humidity, and wind speed are not strongly correlated with the ride time, they will not be excluded from further analysis. This is because each variable was tested with the ride time variable but combinations of humidity, temperature, and wind speed were not looked at. Additional analysis will need to be done to determine if these variables affect the ride time. 




