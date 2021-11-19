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

- How is the school summary affected?
 Original School Summary:
      ![Original School Summary](https://github.com/Tozerh/PyCity/blob/main/Resources/SchoolSummaryOG.PNG)
      
 Adjusted School Summary: 
      ![Adjusted School Summary](https://github.com/Tozerh/PyCity/blob/main/Resources/SchoolSummaryAdjusted.PNG)
      
  The school summary table was affected only in Thomas High School's row. The other schools didn't have data anmoalies that needed to be removed, so their overall percentages     stayed the same. At THS specifically, we removed the presumably dishonest scores from their 9th grade testing, not counting these scores in our totals at all. The results       were: 
      
      Average Math Score: Change from 83.41% to 83.35%
      
      Average Reading Score: 83.84% to 83.89%
      
      % Passing Math: Change from 93.27% to 93.19%
      
      % Passing Reading: Change from 97.31% to 97.02%
      
      % Overall Passing: Change from 90.95% to 90.63%

- How does replacing the ninth graders’ math and reading scores affect Thomas High School’s performance relative to the other schools?
  If we replace the ninth graders' scores with NaN and still include them in the total count of students at THS
- How does replacing the ninth-grade scores affect the following:

- Math and reading scores by grade

- Scores by school spending

- Scores by school size

- Scores by school type

## Suggestions to Modify Code for Other Elections


