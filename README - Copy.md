# pandas_challenge
Pandas DataFrame code

#Virtual environment is under PyCity Schools with the name 'virtual_env'
#DISTRICT SUMMARY
1. Left join using merge method (schools x students). Result is assigned to a new DataFrame (district_df)
2. Calculate all variables:
a. Total_schools - getting "school_name" unique values to get total number of schools. As result is a Series, we need to get length of it
b. Total_students - getting "Student ID" unique values to get total number of students. As result is a Series, we need to get length of it 
c. Total Budget - group by is needed to get budget for each school. We could use unique as in a & b, but there may be schools with same budge where some school budgets might be skipped.
d. Average Math score - average of "math_score" values. As total number of district_df corresponds to the total number of students.
e. Average Reading Score - idem for "reading_score" values
f. % Passing Math - Using loc for district_df where "math_score" >= 70. As it returns a DataFrame, shape attribute is used. Then, it's divided by total number of students.
g. % Passing Reading - idem
h. Overall Passing. test using loc if students have passed both math and reading
	district_df.loc[(district_df['math_score'] >= 70) & (district_df['reading_score'] >= 70) 

#SCHOOL SUMMARY
To get data for each school, 'group by' should be used, assigning the outcome to another DataFrame (school_sum) to get all the required information. 
Final results to display will be content in 'school_summary' Data Frame

Most values are calculated similarly to #DISTRICT SUMMARY by using the school_sum Data Frame, except for:
Budget for Student - calculated while filling 'school_summary' data frame 
%Passing Math - using nested for to create a dictionary{school_name:#students who passed Math}. Percentage is calculated using school_students while filling 'school_summary' data frame
%Passing Read - using nested for to create a dictionary{school_name:#students who passed Reading}. Percentage is calculated using school_students while filling 'school_summary' data frame
%Passing Read

