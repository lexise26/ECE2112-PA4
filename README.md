# ECE2112-PA4
## EXPERIMENT 4: DATA WRANGLING AND DATA VISUALIZATION

### Custodio, Louise Angela G.
## 2ECE-D

**I. Intended Learning Outcomes**:
1. To identify the codes and functions needed in cleaning and visualizing data
2. To be able to apply and use the different codes and functions in creating a Python program that will be used in data wrangling and data visualization

**II. Instructions:**
Download the ECE Board Exam 2 dataset and write a Python script/code in the Jupyter Notebook to do the given problems.

## Problems
ECE BOARD EXAM PROBLEM: Using data wrangling and data visualization technique with storytelling, analyze the data and present different (i) data frames; and (ii) visuals using the dataset given

## How I did my code:

Step 1: Load and Display the DataFrame - Load the data from an Excel file into a DataFrame named board and display the contents.

Step 2: Extract Data for Instrumentation - Select rows where the 'Electronics' score is 71 or higher, 'Track' is 'Instrumentation', and 'Hometown' is 'Luzon'. Remove unnecessary columns and reset the index.

Step 3: Calculate and Add the Average Score Column - Compute the average score across 'Math', 'Electronics', 'GEAS', and 'Communication' columns and add it as a new column named 'Average' in the DataFrame.

Step 4: Extract Data for Mindanao - Select rows where the 'Average' score is 55 or higher, 'Hometown' is 'Mindanao', and 'Gender' is 'Female'. 

Step 5: Plot the Average Scores - Create a horizontal bar plot to visualize the effect of 'Track', 'Gender', and 'Hometown' on the 'Average' score.


## Conclusion

This experiment highlighted the importance of data wrangling and visualization techniques in analyzing the ECE Board Exam dataset. By extracting targeted subsets of data and computing an average score, the analysis provided a clearer understanding of student performance. The addition of the 'Average' score column allowed for a comprehensive view of academic achievement, while the horizontal bar plot effectively visualized the impact of 'Track', 'Gender', and 'Hometown' on these scores. This approach demonstrated how combining data manipulation with visualization can transform complex information into insightful and actionable conclusions, showcasing the practical value of these techniques in data analysis.
