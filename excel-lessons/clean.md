# Data cleaning

Once data analysts import data, the next step is to make it useable for analysis. This requires data cleaning, which involves finding and then correcting or removing inaccuracies and inconsistencies in the data. That’s the topic of this lesson. (Common issues that require data cleaning include missing data, extra spaces, special characters, and inconsistent capitalization and naming conventions.)

## Learning objectives

*By the end of this lesson, you will be able to:*
* Communicate why it's important to clean the data
* List 5 techniques you can use to fix numbers, dates, and text 
* Apply Excel functions to remove extraneous characters
<br>

## Prework
* [Video: Data Analysis in Excel (9:58)](https://www.youtube.com/watch?v=YqS0x0yshlo&feature=youtu.be)
* [Video: Formula Auditing Tricks in Excel (4:51)](https://www.youtube.com/watch?v=dCK_LG3Nk6Q&list=PLnVcHd3TXd2qNpfJyfQkwHO70gaZZ79L8&index=3_)
* [Video: Cleaning up Data with TRIM, PROPER, and Text to Columns (13:49)](https://www.youtube.com/watch?v=x78JR7XHTro)
* [Video: Data Cleaning in Excel (12:04)](https://www.youtube.com/watch?v=WRk9t5yo5Zs)
* [Reading: Top Ten Ways to Clean Your Data](https://support.office.com/en-us/article/top-ten-ways-to-clean-your-data-2844b620-677c-47a7-ac3e-c2e157d1db19)

## In-class work
**Code along: remove extraneous characters - 15 min**
* Use the [data_cleaning_demo.xlsx](https://drive.google.com/file/d/10PFvbBtuSEVSmt0RmyfuzMbAERBkVY42/view?usp=sharing) spreadsheet for this code along
* Create a table in Excel to faciliate sorting
* Fill in the blank cells in a category column
  * ```Home > Find & Select > Go To Special```.   A Go To Special dialog box appears. Select the "Blanks" option
  * Enter a formula that copies the previous cell in the column. For example, "=B2" in cell B3
  * hit Ctrl-Enter to copy the formula to all the blank cells
* [SUBSTITUTE](https://support.office.com/en-us/article/substitute-function-6434944e-a904-4336-a9b0-1e58df3bc332)
* [TRIM](https://support.office.com/en-us/article/trim-function-410388fa-c5df-49c6-b16c-9e5630b479f9)
* [CLEAN](https://support.office.com/en-us/article/clean-function-26f3d7c5-475f-4a9c-90e5-4b8ba987ba41)
<br>

### !challenge

* type: paragraph
* id: 922a6ea0-cb66-4fb8-bd28-594dbe5b79d3
* title: remove unwanted characters

##### !question
**Exercise: remove extraneous characters - 15 min**
* Work in pairs
* Use the [EXAMPLE_DataToClean spreadsheet](https://drive.google.com/file/d/16SjBuqk5gPoqVM0oDKFreXxuhOTi21jv/view?usp=sharing)
* In the Area column, fill in the blank cells with the appropriate area name
* In the Street column:
  *  Remove leading and trailing blanks
  *  Replace the odd characters with blanks
* In the Street 2 column:
  * Use the [PROPER](https://support.office.com/en-us/article/proper-function-52a5a283-e8b2-49be-8506-b2887b889f94?ui=en-US&rs=en-US&ad=US) function to capitalize each word 
  * Sort by the column and do a few manual corrections
  * Submit a GitHub link to your spreadsheet

##### !end-question

##### !placeholder

Paste link here

##### !end-placeholder

### !end-challenge

**Exercise: correct data issues in several columns - 30 min**
* Work individually to discover a data cleaning function that you want to share with the class - 10 min
  * For ideas, refer to the post [Top ten ways to clean your data](https://support.office.com/en-us/article/top-ten-ways-to-clean-your-data-2844b620-677c-47a7-ac3e-c2e157d1db19)
  * From web searches, find the best description and examples for using that function
  * Share your link in the class Slack channel
* Share your findings with your classmates - 20 min
<br>

### Resources
