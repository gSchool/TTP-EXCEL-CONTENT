# Columns

This lesson explores how to create new columns derived from existing columns. 

Imagine that you need to calculate your company’s net income (revenue minus expenses) by month. You have a table that includes one column that details the company’s monthly revenue and a second column that details the company’s monthly expenses. Good news: you can easily engineer a *new* column that calculates the difference between these two columns… and then populates the new column with that information.  

Here’s a second example: imagine that you have a column that includes the city and the state of an event. The report that you’re working on requires information about only the state of each event. No problem; you can create a new column that extracts just the state into that new column. 

## Learning objectives
*By the end of this lesson, you will be able to:*
* Engineer new columns from existing columns
* Extract substrings from strings
* Create date parts such as quarter, month, and week
<br>
<br>

## Prework
* [Video: Excel Formulas and Functions (4:04)](https://www.youtube.com/watch?v=moF8Zy9Fe7E)
* [Video: How to Split Date and Time in Excel (3:15)](https://www.youtube.com/watch?v=-V2W8l8b4bA)
* [Video: How to Convert Dates in Excel into Year, Month, or Day Using the Text Formula (3:48)](https://www.youtube.com/watch?v=yPkFF3eYVkQ)
<br>

## In-class work                     

### Code-along: extract leading and trailing substrings (15 min)
* Use the da_ingredients.ingredients table and extract a spreadsheet showing the first 10,000 rows
* Extract leading and trailing substrings using [LEFT](https://support.office.com/en-us/article/left-leftb-functions-9203d2d2-7960-479b-84c6-1ea52b99640c) and [RIGHT](https://support.office.com/en-us/article/right-rightb-functions-240267ee-9afa-4639-a02b-f19e1786cf2f)
* Extract substrings using position/length with the [MID](https://support.office.com/en-us/article/mid-midb-functions-d5f9e25c-d7d6-472e-b568-4ecb12433028) function
<br>

### !challenge

* type: paragraph
* id: d8d7d712-e152-407a-91d8-f98ae49392a7
* title: Extract part of a text cell

##### !question

**Exercise: extract left, right, and middle parts of text (15 min)**
* Work in pairs
* Use data extracted from the da_pronto.trip data
  * Prepare new columns with substrings extracted from other columns
    * In a new column, use LEFT to extract the text part of the bikeid
    * In a new column, use RIGHT to extract the numerical part of the bikeid
Submit a GitHub link to your spreadsheet

##### !end-question

##### !placeholder

Paste link here

##### !end-placeholder

### !end-challenge


### Code-along: extract text parts from text cells (15 min)
* Use the da_ingredients.ingredients table and extract 10,000 rows spreadsheet
* Use FIND to locate a character's position in a string
* Use FIND with LEFT and RIGHT to extract to the left or right of any substring
  * Extract before or after the character
    * =RIGHT(A1,LEN(A1)-FIND(",",A1)) 
    * =LEFT(A1,FIND(",",A1)-1)
* Identify if the text contains a substring
  * [SEARCH](https://support.office.com/en-us/article/search-searchb-functions-9ab04538-0e55-4719-a72e-b6f54513b495)

### !challenge

* type: paragraph
* id: dfd5cd48-f7da-4d97-9a6a-0c48c741fc3b
* title: Extract part of a text cell based on substring match

##### !question
**Exercise: extract text that is left or right of a substring pattern (15 min)**
* Work in pairs
* * For this exercise, use the Pronto trip data you imported into Excel in the previous exercise
  * In a new column, use FIND with LEFT or RIGHT to extract the *numerical* part of the station_id
  * In a new column, use FIND with LEFT or RIGHT to extract the *character* part of the station_id
  * Create a new column that indictes whether Occidental is in the to_station_name column in each row
*Submit a link to this spreadsheet

* Extra learning:  Reasearch and use Excel's IFERROR function to create a column that shows the starting location of the word "Occidental" or a "" when Occidental is not in the to_station_name column.

##### !end-question

##### !placeholder
Paste link here

##### !end-placeholder

### !end-challenge

### Code-along: create date part columns (20 min)
* Review documentation for Excel date functions
* Export a sample of the Readychef event table and import into Excel
* Create a month and year column
* Create a quarter column

### !challenge

* type: paragraph
* id: 5c751c0e-8041-48d7-b8db-c33575f7ed71
* title: Create date and time part columns

##### !question
    
**Exercise: Pronto bike share data (40 min)**
* Work in pairs
* Export a sample of 50,000 rows from the da_pronto.trip database table 
* Create columns derived from existing columns 
  * Create a year column
  * Create a month column
  * Create a quarter column
  * Create an hour column
    * Search to find solutions in documentation or other resources on the web
* Submit a GitHub link to this spreadsheet

##### !end-question

##### !placeholder
Paste link here

##### !end-placeholder

### !end-challenge
