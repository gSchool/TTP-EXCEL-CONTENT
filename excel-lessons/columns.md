# Columns

This lesson explores how to create new columns derived from existing columns. 

Imagine that you need to calculate your company’s net income (revenue minus expenses) by month. You have a table that includes one column that details the company’s monthly revenue and a second column that details the company’s monthly expenses. Good news: you can easily engineer a *new* column that calculates the difference between these two columns… and then populates the new column with that information.  

Here’s a second example: imagine that you have a column that includes the city and the state of an event. The report that you’re working on requires information about only the state of each event. No problem; you can create a new column that extracts just the state into that new column. 

## Learning objectives
*By the end of this lesson, you will be able to:*
* Engineer new columns from existing columns
* Extract substrings from strings
* Create date parts such as quarter, month, and week

## Prework
* [Video: Excel Formulas and Functions (4:04)](https://www.youtube.com/watch?v=moF8Zy9Fe7E)
* [Video: How to Split Date and Time in Excel (3:15)](https://www.youtube.com/watch?v=-V2W8l8b4bA)
* [Video: How to Convert Dates in Excel into Year, Month, or Day Using the Text Formula (3:48)](https://www.youtube.com/watch?v=yPkFF3eYVkQ)

## In-class work                     

### Code-along: extract leading and trailing substrings (15 min)

**Notes:**

* Create new columns with data extracted from other Excel columns.
* Use data from the da_airbnb schema.

**Instructions:**

1. Use a SQL query to retrieve 1,000 random rows from the da_airbnb.listings table in the online database.

    ```SQL
    SELECT id, listing_url, host_location
    FROM da_airbnb.listings
    ORDER BY RANDOM()
    LIMIT 1000
    ```
    
2. From pgAdmin, export the retrieved data into a CSV file using the download button in the SQL editor pane. (If you need to change the the export delimiter settings in pgAdmin you can do this with File-> Preferences-> Query Tool-> CSV Output Settings.)
3. Open a new workbook in Excel and import the data into Excel using Data -> From Text functionality.
4. Extract leading substrings using [LEFT](https://support.office.com/en-us/article/left-leftb-functions-9203d2d2-7960-479b-84c6-1ea52b99640c) to extract the "https://" part of the strings in the url_listing column into a new column.

    ```
    =LEFT(B2, 8)
    ```
    
5. Extract trailing substrings from the host location using [RIGHT](https://support.office.com/en-us/article/right-rightb-functions-240267ee-9afa-4639-a02b-f19e1786cf2f). 

   *   Looking at the documentation, you need to provide the starting location counted from the end of the string. Use the LEN() function so that you can use the length of the text in your calculation of the substring starting position.
   
    ```
    =RIGHT(B2, LEN(B2)-8)
    ```

6. Extract substrings using position/length with the [MID](https://support.office.com/en-us/article/mid-midb-functions-d5f9e25c-d7d6-472e-b568-4ecb12433028) function.

    ```
    =MID(B2,9,14)
    ```

### !challenge

* type: paragraph
* id: d8d7d712-e152-407a-91d8-f98ae49392a7
* title: Extract part of a text cell

##### !question

**Exercise: extract left, right, and middle parts of text (15 min)**

**Notes:**
* Create new columns with data extracted from other Excel columns.
* Use data from the da_pronto schema.
* Work in pairs.

**Instructions:**

1. Extract 1,000 random rows from the da_pronto.trip online database table and import it into Excel.
2. In a new column, use `LEFT` to extract the text part of the bike ID.
3. In a new column, use `RIGHT` to extract the numerical part of the bike ID.
4. Submit a GitHub link to the spreadsheet in the box below.

##### !end-question

##### !placeholder

Paste your GitHub link here:

##### !end-placeholder

### !end-challenge

### Code-along: extract text parts from text cells (15 min)

**Notes:**
* Create new columns that contain text extracted from existing columns.
* Continue using the Excel Airbnb workbook from the previous code-along.

**Instructions:**

1. Use [FIND](https://support.office.com/en-us/article/find-findb-functions-c7912941-af2a-4bdf-a553-d0d89b0a0628) in a formula to find the position of the first comma in the host_location values.

    ```
    =FIND(",",C2)
    ```
    
2.  Use `FIND` with `LEFT` to extract the substring to the left of the comma.

    ```
    =LEFT(C2, FIND(",",C2) - 1)
    ```
  
3.  Use `FIND` with `RIGHT` to extract the substring to the right of the comma.

    ```
    =RIGHT(C2,LEN(C2)-FIND(",",C2))
    ```

4. Note the #VALUE! errors in your formula columns. This happens when the values don't have a comma in them such as when the value is US. Handle that error in the formulas with the [IFERROR](https://support.office.com/en-us/article/iferror-function-c526fd07-caeb-47b8-8bb6-63f3e417f611) function.

    ```
    =IFERROR(LEFT(C2, FIND(",",C2) - 1), C2)
    ```
    
    ```
    =IFERROR(RIGHT(C2,LEN(C2)-FIND(",",C2)), "")
    ```

5. Create a new column that indicates if a particular city is in the host_location value.

    * [SEARCH](https://support.office.com/en-us/article/search-searchb-functions-9ab04538-0e55-4719-a72e-b6f54513b495)
    
    ```
    =IFERROR(SEARCH("Seattle",C2), 0)
    ```

### !challenge

* type: paragraph
* id: dfd5cd48-f7da-4d97-9a6a-0c48c741fc3b
* title: Extract part of a text cell based on substring match

##### !question
**Exercise: extract text that is left or right of a substring pattern (15 min)**

**Notes:**

* Work in pairs.
* Continue using the Pronto trip data that you imported into Excel in the previous exercise.

**Instructions:**

1. In a new column, use `FIND` with `LEFT` or `RIGHT` to extract the *numerical* part of the from_station_id.
2. In a new column, use `FIND` with `LEFT` or `RIGHT` to extract the *character* part of the from_station_id.
3. Create a new column that indicates whether Occidental is in the to_station_name column in each row.
4. Optional: Research and use Excel's `IFERROR` function to create a column that shows the starting location of the word "Occidental" or a 0 when Occidental is not in the to_station_name column.
5. Submit a GitHub link to the spreadsheet in the box below.

##### !end-question

##### !placeholder
Paste your GitHub link here:

##### !end-placeholder

### !end-challenge

### Code-along: create date part columns (20 min)

**Notes:**
* Create new columns that contain date parts of an existing column.
* Continue using the Excel Airbnb workbook from the previous code-along.

**Instructions:**

1. Retrieve 1,000 rows with several columns from the da_airbnb.

    ```SQL
    SELECT listing_id, id, date, reviewer_id, reviewer_name
    FROM da_airbnb.reviews
    ORDER BY RANDOM()
    LIMIT 1000
    ```

2. Download and import the data into an new Excel tab.
3. Review documentation for [Excel date functions](https://support.office.com/en-us/article/date-and-time-functions-reference-fd1b5961-c1ae-4677-be58-074152f97b81).
4. Create a new column that contains the day from the date column.

    ```Excel
    =DAY(C2)
    ```
5. Create a month column.

    ```Excel
    =MONTH(C2)
    ```

6. Create a year column.

    ```Excel
    =YEAR(C2)
    ```

7. Extract the quarter from the data.
    * There is no quarter function in the Excel date functions documentation, but you can find a formula that calculates the calendar quarter of the data. (A search for "excel quarter from date" gets you to a page similar to [this](https://www.extendoffice.com/documents/excel/3471-excel-find-quarter-from-date.html).)
    * Create a formula in a new column.
 
    ```Excel
    =ROUNDUP(MONTH(C2)/3,0)
    ```

### !challenge

* type: paragraph
* id: 5c751c0e-8041-48d7-b8db-c33575f7ed71
* title: Create date and time part columns

##### !question

**Exercise: Pronto bike share data (40 min)**

**Notes:**

* Work in pairs.
* Use the da_pronto.trip database table. 

**Instructions:**

1. Export a sample of 50,000 rows from the da_pronto.trip database table. 
2. Create columns derived from existing columns.
3. Create a year column.
4. Create a month column.
5. Create a quarter column.
6. Create an hour column. (Search to find solutions in documentation or other resources on the web.)
7. Submit a GitHub link to the spreadsheet in the box below.

##### !end-question

##### !placeholder
Paste your GitHub link here:

##### !end-placeholder

### !end-challenge

## Solutions
These solutions are intended for use after the exercises are completed:
* Solutions to the code-alongs in this lesson are available in the [columns_codealongs.xlsx](https://drive.google.com/uc?export=download&id=15ba5zPqGaBaMdHei7Bm6FIqa7Tn2qyE6) spreadsheet.
* Example exercise solutions for text extraction exercises are in the [columns_pronto_exercises - Solutions.xlsx](https://drive.google.com/uc?export=download&id=1OiHUrfdPGHpCMpBqW0NA93B_Fk1qnjFv) spreadsheet.
* Example exercise solutions for date part extraction exercises are in the [datepart_exercise - Solutions.xlsx](https://drive.google.com/uc?export=download&id=1YsvPUz44vGBEl54I7gdKYFEOskZJWkoe).
