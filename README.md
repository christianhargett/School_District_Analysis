# School District Analysis

## Overview of the Project

### In this project we have been given a dataset of student test scores for a particular school district by our manager, Maria, who has asked us to clean and manipulate the dataset in order to produce an analysis that she will later present to the school board. This analysis includes: a high-level snapshot of the district's key metrics, top 5 and bottom 5 performing schools based on the overall passing rate, the average math and reading scores by grade level, & school performance based on budget per student, school size, and type of school. After performing our analysis, Maria has informed us that the school board believes our raw data shows evidence of academic dishonesty, specifically from the reported math and reading scores of the 9th graders at Thomas High School. Maria has asked that we replace the reading and math scores from the 9th graders at Thomas High School and re-run the analysis, then compare the new metrics to our initial metrics.

## Results

### After replacing the math and reading scores of the 9th graders at Thomas High School with NaNs, our key metrics that we initially provided to Maria have changed:

- The district summary dataframe is a high-level overview of the key metrics for the entire district. These metrics include the total school and student count, total budget count, average math and reading scores, and % passing rates for math and reading as well as the overall passing rate. Before replacing the 9th grade Thomas High School scores our dataframe looked like the below:

![](https://github.com/christianhargett/School_District_Analysis/blob/master/Resources/District_Summary_Before.png)

- After replacing the values, our updated dataframe has a few changes:

![](https://github.com/christianhargett/School_District_Analysis/blob/master/Resources/District_Summary_After.png)

- The replacement of scores has a relatively small impact on the district snapshot, as the average math score has only dropped .1% while each "% Passing" category has only dropped 1%.

- Our school summary dataframe, however, is not so relatively unaffected. This dataframe contains similar metrics as the district summary except it is broken out by school. In our initial reporting, the % passing metrics for Thomas High School were as follows:
  - % Passing Math: 93.3%, % Passing Reading: 97.3%, % Overall Passing: 90.9%

- After replacing the 9th grade values, the new metrics are as follows:

  - % Passing Math: 66.9%, % Passing Reading: 69.7%, % Overall Passing: 65.1%

- We can see there is a drastic difference in the passing rates once we replace the 9th grade math and reading scores. This is quite a difference in average scores relative to other schools. Before we replaced the values, Thomas High School ranked 2nd among all schools in the % Overall Passing category:

![](https://github.com/christianhargett/School_District_Analysis/blob/master/Resources/Top_Schools_Before.png)

- Thomas High School is no longer in the top 5 schools once we replace their 9th grade score values:

![](https://github.com/christianhargett/School_District_Analysis/blob/master/Resources/Top_Schools_After.png)

- When looking at the dataframe that shows metrics by grade level, the only difference in our before vs. after snapshot is that the values for 9th grade at Thomas High School display as "Nan". This is expected, since we essentially voided all of the 9th grade scores from Thomas High School.

- Another dataframe we created was the spending per school summary. We put schools into 1 of 4 categories based off of their average spending per student. Our initial dataframe is as follows:

![](https://github.com/christianhargett/School_District_Analysis/blob/master/Resources/Per_School_Spending_Before.png)

- After replacing our values we have the following dataframe:

![](https://github.com/christianhargett/School_District_Analysis/blob/master/Resources/Per_School_Spending_After.png)

- We can see that the "630-644" bin passing rates have dropped. This is because Thomas High School is included in this bin, and when we replaced their 9th grade scores their passing rates also dropped.
