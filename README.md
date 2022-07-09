# School_District_Analysis
## Analysis Overview
This analysis was conducted for fifteen schools. There was evidence that the reading and math scores for the ninth graders at Thomas High School were altered. As a result, we evaluated this analysis to remove those altered grades while the rest of the data remained intact, in order to uphold state-testing standards. We analyzed the school district by:
  * Average scores for reading, math, and overall.
  * Total budget for all schools, then by individual school.
  * The per student budget for each school.
  * The top five and bottom five schools in the district based on overall passing scores.
  * Math and reading scores by individual grade (from 9th to 12th).
  * Scores by school spending, size, and type (District and Charter)

## Resources
  * Data Source: schools_complete.csv, students_complete.csv
  * Software: Jupyter Notebook 6.4.8.

## Results
  * How is the district summary affected?
    * To evaluate how the district summary was affected, we will first present the district summary prior to the removal of the ninth graders' math and reading scores.
    ![Previous District Summary](https://user-images.githubusercontent.com/106129195/177899346-41cf54b1-0d78-49bd-b358-51284b249b9d.png)
    
    * As shown above, we have a summary of the district's budget, average reading and math scores, along with the percentages of passing. Let us compare this summary to after we had replaced the scores with NaNs.
    ![Current District Summary](https://user-images.githubusercontent.com/106129195/177899355-f1c60f39-2b32-43fe-84ee-8b1d63151513.png)
    
    * We can see that the average math score dropped by 0.1, whereas the average reading score remained the same. We can also note that the percentage of those passing math had dropped by 0.2%, and passing reading dropped by 0.1%. The overall passing percentage dropped by 0.3%.

  * How is the school summary affected?
    * To look into whether the school summary was affected, we can first review the summary prior to the changes being implemented, as shown below.
      ![Previous School Summary](https://user-images.githubusercontent.com/106129195/177900703-79fc2eb1-7cb3-4bba-b10c-155b9a731835.png)
    
    * Thomas High School had percentages of passing scores between 65.1% to 69.7%. Now let us take a look at the summary after we have removed the ninth graders math and reading scores.
  
      ![Current School Summary](https://user-images.githubusercontent.com/106129195/177900715-17374b12-8e63-4876-afb8-d99092cb87f1.png)
      
    * Looking to Thomas High School, we can see that the percentages passing math, reading, and overall, increased to a range of 90.6% to 97.0%.

  * How does replacing the ninth graders' math and reading scores affect Thomas High School's performance relative to the other schools?
    * When the grades for the ninth graders were replaced, Thomas High School's performance relative to other schools drastically increased, as shown below.
      ![Top Five Schools](https://user-images.githubusercontent.com/106129195/178079856-3377e184-6fd1-42e5-9dd8-6f9fdc77ca2f.png)

    * Due to Thomas High School's overall passing percentage having gone up, it became one of the top five performing schools out of the total of 15 schools.
  
  * How does replacing the ninth-grade scores affect the following:
    * Math and reading scores by grade
      * To review how the math and reading scores were affected, here is a summary of math and reading scores prior to removing the ninth graders' scores.
    
        ![Math Scores - Previous_resized](https://user-images.githubusercontent.com/106129195/178087021-dcfb9c00-f3fc-4da3-87d7-648fe6308e59.png)
        ![Reading Scores - Previous_resized](https://user-images.githubusercontent.com/106129195/178087053-e983cdf2-3b9a-4947-959e-7e651f491620.png)
        
        ##### Math and Reading scores, respectively.
        
      * Now that we've established what the grades were before, let us take a look at the summary of math and reading scores after removing the ninth graders' scores for Thomas High School.
    
        ![Math Scores - Current_resized](https://user-images.githubusercontent.com/106129195/178086984-035e46b3-1f70-422b-a2b4-d73938979a51.png)
        ![Reading Scores - Current_resized](https://user-images.githubusercontent.com/106129195/178087064-e18dca34-f95b-40cc-887a-c3f939b3b6c9.png)

        ##### Math and Reading scores, respectively.

      * As we can see, the ninth graders' scores were changed to 'nan' for math and reading. This did not affect any other grades for any of the other schools.

    * Scores by school spending
    
      * To investigate whether there was a correlation between the scores and school spending, we pulled the data from the Per Student Budget (as shown in the school summary above) and set the numbers into ranges. We analyzed the data to see how much money was spent on each student, and their average math and reading scores, along with the percentages of those passing math, reading, and overall.
    
        ![School Spending - Previous](https://user-images.githubusercontent.com/106129195/178082252-ce7806b5-5104-46fe-bc5b-bff38b1954f1.png)
      
      * Now, let us look at the same information, but with the ninth graders' scores removed.
    
        ![School Spending - Current](https://user-images.githubusercontent.com/106129195/178082260-1873b088-1a72-4871-befe-128094f2cdd0.png)
      
      * Thomas High School's Per Student Budget was $638.00, causing it to fall in the range of $631-645. We used the decimal points to see the scale of the effect removing the ninth graders' scores had on that range. It would appear that there was a slight decrease in those numbers, except for the Average Reading score. There was a slight increase.
      
    * Scores by school size
    
      * To look into the relationship between the scores and the school size, we sorted the school sizes by small (less than 1,000 students), medium (1,000 to 1,999 students), and large (2,000 to 5,000). We specifically looked at the average math and reading scores, and the passing percentages for math, reading, and overall, as shown below.
    
        ![Scores by School Size - Previous](https://user-images.githubusercontent.com/106129195/178085867-51f00f96-e630-4a0f-9619-4ee0cbe88505.png)

      * As we can see, small and medium-sized schools have a higher number of students passing math, reading, and overall, compared to large schools. Now, let us take a look at the data when we had removed the ninth graders' scores from Thomas High School, which was a medium-sized school.
    
        ![Scores by School Size - Current](https://user-images.githubusercontent.com/106129195/178085868-4da6dba5-6441-435f-8a25-702f83a8615f.png)
    
      * Upon comparison, there was a slight decrease in percentages for medium-sized schools, except for the Average Reading score, where we can see a slight increase.

    * Scores by school type

      * To evalute how the removal of the scores affect the school type information, we analyzed the data by school type: District and Charter. Prior to replacing the ninth graders' scores by 'NaN', here we can see how the scores fared with each school type:

        ![Scores by School Type - Previous](https://user-images.githubusercontent.com/106129195/178085924-3e5d35e5-9ea8-4de7-940d-8c8ff94fef22.png)
      
      * Now, here is the summary of scores by school type, when we had removed the ninth graders' grades from Thomas High School, a Charter school.

        ![Scores by School Type - Current](https://user-images.githubusercontent.com/106129195/178085926-208825d8-f092-4a9f-b4ca-6165ad635181.png)

      * As shown, we can see that in the Charter row, in the decimal point ranges, most of the scores had a slight decrease. In contrast, the average reading score had a slight increase.

## Summary

As the results have shown, the altered ninth graders' scores had an effect on the overall purview of the schools' performances. One change we noticed was in the district summary. After the change, the average math score dropped, as well as the percentages of students passing math, reading, and overall. It is also worth noting that the average reading score remained the same.

Another change we noticed was within the school summary. Less than 70% of Thomas High School students passed any of the three criteria (math, reading, and overall). However, upon removing the altered grades, the percentages had a dramatic increase, from ~60% to ~90%. The percentage of students who passed reading was 97%, whereas beforehand it was 69%. We can draw the conclusion that the percentages of students passing drastically increased when the altered grades were removed.

We also saw that Thomas High School moved into the top five schools out of the 15 schools. Based on the school summary, Thomas High School had an overall passing percentage of 65.1%. Upon replacing the ninth graders' math and reading scores with 'NaN', the percentage increased to 90.6%, earning the school a spot in the top five.

When we compared the Per Student budget with the scores, we also noticed a change. As Thomas High School spent $638.00 per student, falling in the summary's range of $631-645, removing the ninth graders' scores caused a decrease in: average math score, and percentage of students passing math, reading, and overall. Although we also note that the decrease was very slight, less than 1%. In contrast, the average reading score increased slightly. As the math and reading scores for the ninth graders at Thomas High School were replaced, this would affect any averages that would include those values.

In conclusion, the analysis shows that removing the ninth graders' math and reading scores had an affect, except for the scores in each grade for each school.
