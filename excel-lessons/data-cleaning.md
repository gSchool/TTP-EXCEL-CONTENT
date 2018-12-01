# Data cleaning

Once data analysts import data, the next step is to make it useable for analysis. This requires data cleaning, which involves finding and then correcting or removing inaccuracies and inconsistencies in the data. That’s the topic of this lesson. (Common issues that require data cleaning include missing data, extra spaces, special characters, and inconsistent capitalization and naming conventions.)

## Learning objectives
*By the end of this lesson, you will be able to:*
* Communicate why data cleaning is important
* List 5 techniques that you can use to fix numbers, dates, and text 
* Apply Excel functions to remove extraneous characters

## Prework
* [Video: Data Cleaning in Excel (12:04)](https://www.youtube.com/watch?v=WRk9t5yo5Zs)
* [Text: Top Ten Ways to Clean Your Data](https://support.office.com/en-us/article/top-ten-ways-to-clean-your-data-2844b620-677c-47a7-ac3e-c2e157d1db19) (This is long; it's okay to skim it.)

## In-class work

### Discuss: data cleaning (5 min)

* Data cleaning is important; if data has flaws it might be unusable or unable to load, and analysis will be invalid.
* Often, the data in a database has already been cleaned enough to work with immediately, but that's not the case with data from other sources.
* Obtaining and cleaning data for analysis can often take 50-80% of an analyst's time; be sure to allocate enough time for this data cleaning.

### Code along: remove extraneous characters (15 min)

**Notes:**

Use the [data_cleaning_demo.xlsx](https://drive.google.com/uc?export=download&id=10PFvbBtuSEVSmt0RmyfuzMbAERBkVY42) spreadsheet.

**Instructions:**

1. Using the data_cleaning_demo.xlsx spreadsheet, duplicate the Starting data tab.
2. Select the column headers and data in the tab and turn those into an Excel table using `Data > Filter`.
3. In the month column, fill in the blank cells with the month value using `Home > Find & Select > Go To Special`. When a dialog box appears, select the "Blanks" option.
4. Enter a formula that copies the previous cell in the column. For example, "=B2" in cell B3.
5. Hit *Ctrl-Enter* to copy the formula to all the blank cells.
6. Create a new column with a formula that [TRIM](https://support.office.com/en-us/article/trim-function-410388fa-c5df-49c6-b16c-9e5630b479f9)s the values in the previous column.
7. Create a new column with a formula that [CLEAN](https://support.office.com/en-us/article/clean-function-26f3d7c5-475f-4a9c-90e5-4b8ba987ba41)s the values in the previous column.
8. Create a new column with a formula that [LOWER](https://support.office.com/en-us/article/lower-function-3f21df02-a80c-44b2-afaf-81358f9fdeb4)s (lowercases) the values in the previous column.
9. Create a new column with a formula that uses [SUBSTITUTE](https://support.office.com/en-us/article/substitute-function-6434944e-a904-4336-a9b0-1e58df3bc332) to change the previous column's values that have blanks to "widget."
10. Change the data type of all of the values in the purchases column from their current data types to integer.

### !challenge

* type: paragraph
* id: 922a6ea0-cb66-4fb8-bd28-594dbe5b79d3
* title: remove unwanted characters

##### !question
**Exercise: remove extraneous characters (15 min)**

**Notes:**

* Use the [EXAMPLE_DataToClean](https://drive.google.com/uc?export=download&id=12TsaeEyFddHlRJyPtDcwzwBdcD3wejT0) spreadsheet.
* Work in pairs.

**Instructions:**

1. In the Area column, fill in the blank cells with the appropriate area name.
2. In a new column create a formula that...
    *  Removes leading and trailing blanks in the Street column (column C),
    *  Replaces the odd characters with blanks.
3. In a new column, create a formula using [PROPER](https://support.office.com/en-us/article/proper-function-52a5a283-e8b2-49be-8506-b2887b889f94?ui=en-US&rs=en-US&ad=US) to capitalize each word of the Street 2 column.
4. In a new column, create a formula that combines the logic from the previous two steps into one formula.
5. Submit a GitHub link to the spreadsheet in the box below.

##### !end-question

##### !placeholder

Paste your GitHub link here:

##### !end-placeholder

### !end-challenge

### Exercise: discover other techniques to clean tour data (25 min)

**Notes:**

Work individually.

**Instructions:**

1. Search the web for a different data cleaning function. (Feel free to refer to the post [top ten ways to clean your data](https://support.office.com/en-us/article/top-ten-ways-to-clean-your-data-2844b620-677c-47a7-ac3e-c2e157d1db19).) (10 mins) 
    * Find the best description and examples of using that function.
    * Paste a link of your findings in the class Slack channel.
2. Present your findings with your classmates. (15 min)

## Solutions
Example solutions to the exercises in this lesson above are available in [this](https://drive.google.com/uc?export=download&id=12TsaeEyFddHlRJyPtDcwzwBdcD3wejT0) spreadsheet. These are intended for use after the exercises are completed.

## Resources
* [Video: Data Analysis in Excel (9:58)](https://www.youtube.com/watch?v=YqS0x0yshlo&feature=youtu.be)
* [Video: Formula Auditing Tricks in Excel (4:51)](https://www.youtube.com/watch?v=dCK_LG3Nk6Q&list=PLnVcHd3TXd2qNpfJyfQkwHO70gaZZ79L8&index=3_)
* [Video: Cleaning up Data with TRIM, PROPER, and Text to Columns (13:49)](https://www.youtube.com/watch?v=x78JR7XHTro)
