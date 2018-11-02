# LOOKUP

1.25 hrs
<br><br>
In this lesson, you continue to prepare data by fetching and combining data from several spreadsheets into a worksheet.

### Learning objectives
*By the end of this lesson, you will be able to:*
* Use VLOOKUP and HLOOKUP to fetch data from another table
* Apply parameters to alter the LOOKUP
<br>
 
## Pre-work
* [Introducing LOOKUP Functions (00:30)](https://teamtreehouse.com/library/introducing-lookup-functions)
* [Using VLOOKUP to Search in a Column (00:30)](https://teamtreehouse.com/library/using-vlookup-to-search-in-a-column)
* [Using HLOOKUP to Search in a Row (00:30)](https://teamtreehouse.com/library/using-hlookup-to-search-in-a-row)
* [LOOKUP Tips and Common Errors (00:30)](https://teamtreehouse.com/library/lookup-tips-and-common-errors)

### Combine data from different sources using LOOKUPs
**Overview of the VLOOKUP function - 10 min**
* Use online documentation 
* Emphasize the need to typically set the "Range LOOKUP" parameter to FALSE!
  * This is a good example of the benefit of looking at default paramaters and the other options that are available to you
  * Note limitations such as LOOKUPs returning only the first match of the external table  
<br>

**Code-along: use VLOOKUP to fetch data from other tables - 15 min**
* Use the three "sales" CSV files [purchases.csv](https://drive.google.com/file/d/1Nxvo7RzIfWELSglbDKOb1eVASXBvKgEW/view?usp=sharing), [customers.csv](https://drive.google.com/file/d/1_69gMSjnx7owplIVzKu1SGdNLdNmXGez/view?usp=sharing), and [products_horz.csv](https://drive.google.com/file/d/1Hj1LauM6mS9qM-cbIydTgXs_Acu-iney/view?usp=sharing)
* Use VLOOKUP to add the customer name and city from the customer table to each row of the purchases table
* Danger! You must use absolute references; otherwise the table_range moves when you copy the VLOOKUP formula to another cell
    * You can also use range names. Change your VLOOKUP reference table_array value to a range name.
<br>

### !challenge

* type: paragraph
* id: 03e30b6b-8e09-4eaf-a9e5-60d532341d22
* title: Fetch data with VLOOKUP

##### !question
**Exercise: fetch data from other tables - 15 min**
* Work in pairs
* Use the TCP-H Benchmark data set
  * Download and unzip [this file](https://drive.google.com/file/d/1rvKe9g7IU7MXVYQMKTy9ulYY-J60-an3/view?usp=sharing) containing the TCP-H tables
    * Alternately, download the files individually [here](https://drive.google.com/drive/folders/1dwWXz3uoB_JVc0lcJXaDDU6nyt9v5aEl?usp=sharing)
  * [TCP-H data Schema diagram](https://drive.google.com/file/d/150VWoQ2ZmqrOr2VZsA-EMtX9VJWDiXDI/view?usp=sharing)
* Import orders.csv into an Excel worksheet
  * Name the worksheet "Orders"
* Import customers.csv into a second worksheet and name the worksheet "Customers"
* Using VLOOKUP, add a column to the Orders sheet named "Cust_name" that contains the name of the customer for each order row
* Using VLOOKUP, add another column to the Orders sheet named "Mrkt_segment" that contains the market segment for the customer for each order row
* Submit a GitHub link to this spreadsheet
<br>

##### !end-question

##### !placeholder

Paste link here

##### !end-placeholder

### !end-challenge

**Code-along: use HLOOKUP to fetch data from another table - 10 min**
* Continue using the spreadsheet from the previous code-along
* Import the [products_horz.csv](https://drive.google.com/open?id=1Hj1LauM6mS9qM-cbIydTgXs_Acu-iney) file into a new tab
* Use HLOOKUPs to add the product name and price to each record in the purchases table
    
### !challenge

* type: paragraph
* id: 6f4149ae-909b-40c5-8732-768fa5bc397d
* title: Use LOOKUPS to fetch data from tables

##### !question

**Exercise: use LOOKUPs to fetch data from other tables - 25 min**
* Work in pairs
* Continue using the spreadsheet that you created in the last challenge
* Refer to the [TCP-H data Schema diagram](https://drive.google.com/file/d/150VWoQ2ZmqrOr2VZsA-EMtX9VJWDiXDI/view?usp=sharing) to determine connections between the tables
* Add the country and region of the customer to each row of the orders table; to do this:
  * Import the nation.csv file into an Excel tab (worksheet)
  * Import the [region_horz.csv](https://drive.google.com/open?id=1d7TUbr475M_9HNiKcGUcOsMPKeklwrbj) file into an Excel tab
  * Use HLOOKUP to add a Region column to the Country
  * Use a LOOKUP to add the country and region to each line of the orders table
* Submit a GitHub link to this spreadsheet

##### !end-question

##### !placeholder

Paste link here

##### !end-placeholder

### !end-challenge
