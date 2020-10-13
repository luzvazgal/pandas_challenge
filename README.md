# pandas_challenge
Pandas DataFrame code

The intention of this code is practicing Pandas concepts such as DataFRames, Series, and their related methods.

The file PyCitiSchools_LCVG.ipynb is structured as follows:

1. Preparation and DataFrame definition
Import pandas library and creating DataFrames from reading CSV files, and doing merge
Two main DataFrames are used all over the file:
* district_df -> result from two DataFrames coming from CSV files (schools and students)
* school_sum -> Grouping By "school_name" the 'district_df' data frame

2.Functions Definition
* get_total_students(DataFrame)
	Returns the total number of students in a given DataFrame object

* get_total_Budget(Boolean)
	Returns the total Budget using DataFrame.GroupBy "school_name_gb". 
	Receives a boolean to determine if all values in Series should be summarize

* get_average_score(DataFrame, FieldToAverage)
	Returns Average Score given a DataFrame and field name (str)

* has_Passed_Subject(DataFrame, field_name, grade)
	Tests whether student has the required grade to pass a given assignature using DataFrame object, returning DataFrame if true
	Returns Percentage of students passing subject

* has_overall_passed(DataFrame, subject1, subject2, grade)
	Tests if and only if the student has passed two Subjects, given a DataFrame and a passing grade

* get_score_by(DataFrame, new_Field, cut_field, bins, group_labels)
	Returns DataFrame containing students' scores in Math, Reading and both given a bin to group by.
	If 'new_field' = '', cut method inside function is not used

#Virtual environment is under PyCity Schools with the name 'virtual_env'

#Setting global functions to "re-use" the same functionality across all sections
#DISTRICT SUMMARY
Create a high level snapshot (in table form) of the district's key metrics, including:

-Total Schools
-Total Students
-Total Budget
-Average Math Score
-Average Reading Score
-% Passing Math (The percentage of students that passed math.)
-% Passing Reading (The percentage of students that passed reading.)
-% Overall Passing (The percentage of students that passed math and reading.)

* Using 'district_df' to get results

#SCHOOL SUMMARY
Create an overview table that summarizes key metrics about each school, including:
-School Name
-School Type
-Total Students
-Total School Budget
-Per Student Budget
-Average Math Score
-Average Reading Score
-% Passing Math
-% Passing Reading
-% Overall Passing (The percentage of students that passed math and reading.)
-Create a dataframe to hold the above results

* 'school_sum' is used as based DataFrame

#Top Performing Schools (By % Overall Passing)
-Sort and display the top five performing schools by % overall passing.

* 'school_summary', which is the result from exercise #2 is used as based DataFrame

#Bottom Performing Schools (By % Overall Passing)
-Sort and display the five worst-performing schools by % overall passing.

* 'school_summary', which is the result from exercise #2 is used as based DataFrame


#Math & Reading Scores by Grade
-Create a table that lists the average Math Score for students of each grade level (9th, 10th, 11th, 12th) at each school.
-Create a pandas series for each grade. Hint: use a conditional statement.
-Group each series by school
-Combine the series into a dataframe
-Optional: give the displayed data cleaner formatting
Note: Reading score is calculated in the same way as Math score

#Scores by School Spending
Create a table that breaks down school performances based on average Spending Ranges (Per Student). Use 4 reasonable bins to group school spending. Include in the table each of the following:
-Average Math Score
-Average Reading Score
-% Passing Math
-% Passing Reading
-Overall Passing Rate (Average of the above two)

#Scores by School Size and #Scores by School Type, are calculated the same way as #Scores by School Spending
