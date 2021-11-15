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
In this section, we reanalyzed the following metrics after exluding the 9th-graders test results:
* The District summary
* The school summary
* The top 5 and bottom 5 performing schools, based on the overall passing rate
* The average reading score for each grade level from each school
* The average math score for each grade level from each school
* The scores by school spending per student, by school size and by school type

---
### The District summary
Recalculated total student count by subtracting the number of ninth-grade students in Thomas High School from the total student count, then recalulated the passing math and passing reading percentages and overall passing percentage.
![new student total](https://user-images.githubusercontent.com/48603147/141705852-678ebf7e-d842-4f59-8aac-9a7679a22b83.png)

Using the new student total and recalculated math, reading  and overall passing percentage, I created a new data frame and formatted the values accordingly as seen below
![district_summary_df](https://user-images.githubusercontent.com/48603147/141705938-3b300af6-a89b-412a-900e-de17547c39a2.png)

### The school summary
Using the same methods from previous examples I created a data frame, including the data metrics: School Type, total studemts, total school budget, per student budget, average math score, average reading score, passing math percentage, passing reading percentage and overall passing percentage. I formatted the school budget and per student budget to include the dollar sign and set the values to show to the hundreds place. You can see the data in the following screenshot.
![School Summary table](https://user-images.githubusercontent.com/48603147/141706549-1af6d69f-acc7-40a8-8ce3-a27a1a37f7df.png)

### The top 5 and bottom 5 performing schools, based on the overall passing rate
To find the top 5 and bottom 5 perfoming schools, I recalucated the passing math percentage, passing reading percentage and overall passing percentage of Thomas High School and entered the new data into the school summary data frame. 

After calculating the total number of students in 10th, 11th and 12th grade I calculated the number of those students who passed math and reading. 
* Total number of students in 10th - 12th grade: 1174
* Passing reading: 1094
* Passing math: 1139
![total student](https://user-images.githubusercontent.com/48603147/141708068-ea46a1cb-70b2-48ae-a546-5e2bb749994b.png)

Next I calculated the percentage of 10th to 12th graders who passed readiing, math and the overall passing percentage by exluding the 9th grades data as seen below
![calculate percentage of passsing tests 10th - 12th](https://user-images.githubusercontent.com/48603147/141708206-a1b7ad46-4dbe-4e5a-992c-53db03ec58a3.png)

Next to calclate the top 5 and bottom 5 I replaced the new data from Thomas High School in the per_school_summary_df by using the loc function and used ascending=False.head(5) to find the top five schools and ascending=True.head(5) to find the bottom five schools.
![top 5 and bottom 5 school](https://user-images.githubusercontent.com/48603147/141708907-196c97c4-d2a3-4cbe-8ff7-b35686879c74.png)
