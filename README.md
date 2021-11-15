# PyCitySchools_Challenge
Week 4 for Coloumbia's DS bootcamp
## Overview of PyCityShcools Challenge
The goal of this challenge was to analyize the standardized testing results from a large number of schools state-wide. The test results covered both Math and Reading from 9th to 12th grade and the purpose of this analysis was to see how removing test results from Thomas High School's 9th grade class affect the overall results we obtained from the assignment in Module 4. In Module 4 we found the overall passing percentage of the students and determine whether there is any correlation with the budget per student using numpy-python.


## Deliverable 1: Replace Thomas High School's 9th-grade reading and math scores with Nan
---
We used the loc method to select all the reading and math scores from the ninth grade at Thomas High School. Inside the the loc method a comparison operator was used to retreive all the rows with Thomas High School, logical and comparison operators were used to retrieve all the rows with the "reading_score" and "math_score" column. The reading and math score for the ninth graders in THomas High School are replaced with Nans. The code and table can be seen below. 

![Replace 9th grade math and reading scores.png](https://user-images.githubusercontent.com/48603147/141702225-12f367e8-b347-435e-877d-cb0b6db13264.png)
---

 ## Deliverable 2: Repeat the School District Analysis
In this section, we reanalyzed the following metrics:
* The District summary
* The school summary
* The top 5 and bottom 5 performing schools, based on the overall passing rate
* The average reading score for each grade level from each school
* The average math score for each grade level from each school
* The scores by school spending per student, by school size and by school type

---
### The District summary
Recalculated total student count by subtracting the number of ninth-grade students in Thomas High School from the total student count, then recalulated the passing math and passing reading percentages and overall passing percentage.

