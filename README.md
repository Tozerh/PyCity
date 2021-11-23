# PyCity
Module 4 Work for Bootcamp 

## Project Overvew
PyCity Schools reached out for an analysis of their test scores. PyCity provided the raw data in csv form, and requested a series of slices of the data based on school size, school type, school name, etc. In order to complete this project, we had to deploy the pandas software library, which allows us to manipulate the raw data in Python and to generate the necessary tables. Ultimately, our goal with this project was to assist the school district in understanding how one school's (Thomas High School, "THS") academic dishonesty affected the entire district's reported metrics. 


## Resources
- Data Source: election_results.csv
- Software: Python 3.6.1 (with pandas library), Jupyter Notebooks

## Results

- How is the district summary affected?

Original District Summary:

![Original District Summary](https://github.com/Tozerh/PyCity/blob/main/Resources/DistrictSummaryOG.PNG)

Adjusted District Summary: 

![Adjusted District Summary](https://github.com/Tozerh/PyCity/blob/main/Resources/DistrictSummaryAdjusted.PNG)
      
      
      Average Math Score: Change from 79.0% to 78.9%.
      
      Average Reading Score: No change from 81.9%
      
      % Passing Math: Change from 75.0% to 74.8%
      
      % Passing Reading: Change from 85.8% to 85.7%
      
      % Overall Passing: Change from 65.2% to 64.1%
     
     Note: The above percentages use the adjusted student count for THS, excluding the 9th graders's scores and count from the student totals. 
- How is the school summary affected?

Original School Summary:

![Original School Summary](https://github.com/Tozerh/PyCity/blob/main/Resources/SchoolSummaryOG.PNG)
      
Adjusted School Summary:
 
![Adjusted School Summary](https://github.com/Tozerh/PyCity/blob/main/Resources/SchoolSummaryAdjusted.PNG)
      
  The school summary table was affected only in Thomas High School's row. The other schools didn't have data anomalies that needed to be removed, so their overall percentages     stayed the same. At THS specifically, we removed the presumably dishonest scores from their 9th grade testing, not counting these scores in our totals at all. The results were: 
      
      THS Average Math Score: Change from 83.41% to 83.35%
      
      THS Average Reading Score: 83.84% to 83.89%
      
      THS % Passing Math: Change from 93.27% to 93.19%
      
      THS % Passing Reading: Change from 97.31% to 97.02%
      
      THS % Overall Passing: Change from 90.95% to 90.63%

- How does replacing the ninth graders’ math and reading scores affect Thomas High School’s performance relative to the other schools?
  If we replace the ninth graders' scores with NaN and still include them in the total count of students at THS, then THS scores drop precipitously. Essentially the value of the NaN can be considerd to be zero, and the average scores at THS plummet. For the grade levels at THS not implicated in the academic dishonesty, these scores are not a fair esimate of performance. For example, without adjusting the total student count at THS while still scoring 9th grade results as all zeroes, the percent of THS students passing math is rougly 66.91. Adjusting the total student count at THS to include only grades ten, eleven, and twelve, however, brings the percnet passing math to 93.19, which is a much fairer representation of how THS performed overall. 
  
- How does replacing the ninth-grade scores affect the following:

**Math and reading scores by grade:** For THS's 9th grade scores, the adjusted tables contained the value `NaN` for reading and math. Because we replaced the fraudulent scores for each 9th grade student with `NaN`, we expect to see this reflected in the summary tables by grade. 
           
**Scores by school spending:** Similarly to the school summary and district dataframes, we see a slight changes in the spending range that includes THS. This range is the $630 - $644 range, and the value changes from the original dataframe to the adjusted are as follows: 
     
     - Avg. Math Score: 78.52% to 78.50%
     - Avg. Reading Score: 81.62% to 81.64%
     - % Passing Math: 73.48% to 73.46%
     - % Passing Reading: 84.39% to 84.32%
     - % Overall Passing: 62.86% to 62.79%

**Scores by school size:** Changes to scores by school size parallel the changes to scores by school spending, with a slight increase in the Average Reading Score, while all other categories see a slight decrease: 
     
Original School Size Summary Table: 
          
![OG School Size](https://github.com/Tozerh/PyCity/blob/main/Resources/SchoolSizeOG.PNG)
          
Adjusted School Size Summary Table: 
     
![Adjusted School Size](https://github.com/Tozerh/PyCity/blob/main/Resources/SchoolSizeAdjusted.PNG)
          
     **Scores by school type:** THS is a charter school, so we would expect to only see changes for this category of school, and indeed that's what the data bears out. The changes to charter school aggregate data are slight and in line with what we see in other summaries for this project (i.e., a slight uptick in average reading score and a slight decrease in all other categories:
     
        
Original School Type Summary Table: 
          
![OG School Type](https://github.com/Tozerh/PyCity/blob/main/Resources/TypeSummaryOG.PNG)
          
Adjusted School Type Summary Table: 
     
![Adjusted School Type](https://github.com/Tozerh/PyCity/blob/main/Resources/TypeSummaryAdjusted.PNG)
          

## Summary of Changes after Reading and Math Scores Were Replaced

*After reading and math scores were replaced, the overall statistics for the school disctrict changed in four ways:* 

1) Since the NaN values are treated like a zero when calculating averages, the % Passing Math and % Passing Reading for the District overall drop from 75.0% to 74.8% and from 85.8% to 85.7%, respectively. 

2) The Average Math Score for the District drops from 79.0% to 78.9%. 

3) The Average Reading Score for the Disrict remains largely unaffected, remaining at 81.9% even after the 9th grade THS scores were replaced. 

4) The % Overall Passing dropped from 65.2% before the score replacements to 64.1%. This significant drop can be attributed to the fact that the doctored scores for the 9th graders at THS included both doctored math and reading scores for each student. Since each 9th grade student at THS had higher scores than they should have in both categories, the % Overall Passing increased significantly.  

