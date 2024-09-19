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

        board = pd.read_excel('board2.xlsx')    
        board                               

Step 2: Extract Data for Instrumentation - Select rows where the 'Electronics' score is 71 or higher, 'Track' is 'Instrumentation', and 'Hometown' is 'Luzon'. Remove unnecessary columns and reset the index. 
                                           
       Instru = board[(board['Electronics'] >= 71) & (board['Track'] == 'Instrumentation') & (board['Hometown'] == 'Luzon')]
       Instru.drop(columns=['Gender', 'Track', 'Hometown', 'Math', 'Communication']).reset_index(drop=True)

Step 3: Calculate and Add the Average Score Column - Compute the average score across 'Math', 'Electronics', 'GEAS', and 'Communication' columns and add it as a new column named 'Average' in the DataFrame.

      board['Average'] = (board['Math'] + board['Electronics'] + board['GEAS'] + board['Communication'])/4
      board

Step 4: Extract Data for Mindanao - Select rows where the 'Average' score is 55 or higher, 'Hometown' is 'Mindanao', and 'Gender' is 'Female'. 

     Mindy = board[(board['Average'] >= 55) & (board['Hometown']=='Mindanao') & (board['Gender']=='Female')]
     Mindy.drop(columns=['Gender', 'Hometown', 'Math', 'GEAS', 'Communication']).reset_index(drop=True)

Step 5: Plot the Average Scores - Create a horizontal bar plot to visualize the effect of 'Track', 'Gender', and 'Hometown' on the 'Average' score.

Step 6: Prepare the Data and Plot Setup - Assign the 'Average' column to a variable x, set the figure size (20x10), and apply the 'fivethirtyeight' plot style.

Step 7: Create the Plot - Generate three horizontal bar graphs comparing 'Track', 'Gender', and 'Hometown' with average scores, and label the axes and title appropriately.

Step 8: Add Legend and Display - Include a legend to distinguish between the categories and display the final plot using plt.show().

    x = board['Average']

    plt.figure(figsize=(20,10))
    plt.style.use('fivethirtyeight')

    plt.title('The Effect of Track, Gender, and Hometown to Average Score', fontsize=30, fontweight = 'bold')
    plt.barh(board['Track'], x, label="Track")
    plt.barh(board['Gender'], x, label="Gender")
    plt.barh(board['Hometown'], x, label="Hometown")
    plt.ylabel('Features', fontsize=20)
    plt.xlabel('Average', fontsize=20)

    plt.legend(fontsize=20)
    plt.show()

## Conclusion

This experiment highlighted the importance of data wrangling and visualization techniques in analyzing the ECE Board Exam dataset. By extracting targeted subsets of data and computing an average score, the analysis provided a clearer understanding of student performance. The addition of the 'Average' score column allowed for a comprehensive view of academic achievement, while the horizontal bar plot effectively visualized the impact of 'Track', 'Gender', and 'Hometown' on these scores. This approach demonstrated how combining data manipulation with visualization can transform complex information into insightful and actionable conclusions, showcasing the practical value of these techniques in data analysis.

## Author
  Custodio, Louise Angela G.

