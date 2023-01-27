## Healthcare Analysis using Excel

**Project description:** 
We’ve all had our experiences with healthcare. To improve experiences that occur in the hospital, we need to look back at the data. This particular dataset focuses on types of incoming patients, medications, procedures, length of stay and demographic features. It is a collection of 10 years (1999-2008) of clinical care that occurred between 130 hospitals within the United States. 

In this project, I am working to uncover following objectives:

1 - Which department likely needs more lab facilities?

2 - Which departments likely need more rooms to serve admitted patients?

3-  Which age groups need more number of medications?

4-  Do lab procedures mean longer stays in the hospital?

### 1. Which department likely needs more lab facilities?

Here I wanted to understand which departments perform the most number of lab procedures. Comparing it against the number of patients they get, we can 
decide whether the patients reporting to the department can benefit from establishing more lab facilities.

I used a pivot table and sorted the departments by the number of patients they handeled. Looking at the average number of lab procedures performed, most lab procedures are performed by internal medicine department which also handles the most number of patients. So, the internal medicine department may benefit from setting up more lab 
facilities.

<img src="images/Screenshot 2023-01-27 110122.png"/>

### 2. Which departments likely need more rooms to serve admitted patients?

Based on data the patients spend anywhere from 1 to 14 days in the hospital. Looking at the distribution of patients across the days, I noticed that around 60% patients admissions are concentrated between 4 to 9 days of hospitalization. So I filtered the number of patients being hospitalized between 4 to 9 days across all departments. After sorting, I found top 5 departments requiring most number of admitted patients between 4 to 9 days. So, these departments likely need more rooms to serve admitted patients.
Even in these 5 departments, Internal medicine department has the highest number of admitted patients staying for 9 days, so it is best to focus on the internal medicine department first in terms of evaluating room facilities.

<img src="images/Screenshot 2023-01-27 155732.png"/>

### 3. Which age groups need more number of medications?

The pivot table below clearly indicates that ag groups from 50 years to 70 years need most number of medications

<img src="images/Screenshot 2023-01-27 154334.png"/>

### 4. Do lab procedures mean longer stays in the hospital?

Using two attributes of number of lab procedures and time in hospital we can clearly see that more lab procedures mean more time in hospital. Further this trend is consistent across all age groups.

<img src="images/Screenshot 2023-01-27 155843.png"/>

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).
