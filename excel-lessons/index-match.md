# INDEX and MATCH

1.5 hours
<br><br>
In this lesson, you continue preparing data by fetching and combining data from several spreadsheets into a worksheet. This time, you use INDEX and MATCH in place of LOOKUPs, since INDEX and MATCH reduce the amount of processing to find the right data due their method's greater efficiency on larger tables.

### Learning objectives
*By the end of this lesson, you will be able to:*
* Describe the advantages of INDEX and MATCH over LOOKUPs
* Use INDEX and MATCH to fetch data from another table
<br>

## Pre-work
* [Video: Excel Index Match: the Basics of Index and Match for Complex Excel Lookup Problems (11:31)](https://www.youtube.com/watch?v=F264FpBDX28)
* [Video: Excel Index Match Advanced: Lookup Multiple Criteria in Rows or Columns (10:21)](https://www.youtube.com/watch?v=ontXHp9cwOQ)

### Combine data from different sources using INDEX/MATCH
**Overview of INDEX and MATCH functions - 15 min**
* Refer to information in the online documentation and search
* Highlight the compute efficiency advantages of INDEX/MATCH over LOOKUPs
  * For larger files it's worth the extra effort to INDEX/MATCH

**Code-along: use INDEX and MATCH to fetch data from other tables - 15 min**
* Use the three "sales" CSV files [purchases.csv](https://drive.google.com/file/d/1Nxvo7RzIfWELSglbDKOb1eVASXBvKgEW/view?usp=sharing), [customers.csv](https://drive.google.com/file/d/1_69gMSjnx7owplIVzKu1SGdNLdNmXGez/view?usp=sharing), and [products_horz.csv](https://drive.google.com/file/d/1Hj1LauM6mS9qM-cbIydTgXs_Acu-iney/view?usp=sharing)
* Use INDEX and MATCH to add the customer name and city from the customer table to each row of the purchases table
<br>

### !challenge

* type: paragraph
* id: 00dde750-1ac8-4667-a591-cdd9896f62fa
* title: Fetch data with INDEX and MATCH

##### !question
**Exercise: fetch data from other tables - 20 min**
* Work in pairs
* Use the TCP-H Benchmark csv files from the LOOKUPs lesson or:
  * Download and unzip [this file](https://drive.google.com/file/d/1rvKe9g7IU7MXVYQMKTy9ulYY-J60-an3/view?usp=sharing) containing the TCP-H tables
    * Alternately, you can download the files individually [here](https://drive.google.com/drive/folders/1dwWXz3uoB_JVc0lcJXaDDU6nyt9v5aEl?usp=sharing)
  * [TCP-H data Schema diagram](https://drive.google.com/file/d/150VWoQ2ZmqrOr2VZsA-EMtX9VJWDiXDI/view?usp=sharing)
* Import orders.csv into an Excel worksheet
  * Name the worksheet "Orders"
* Import customers.csv into a second worksheet and name the worksheet "Customers"
* Using INDEX and MATCH, add a column to the Orders sheet named "Cust_name" that contains the name of the customer for each order row
* Using INDEX and MATCH, add another column to the Orders sheet named "Mrkt_segment" that contains the market segment for the customer for each order row
* Submit a GitHub link to this spreadsheet
<br>

##### !end-question

##### !placeholder

Paste link here

##### !end-placeholder

### !end-challenge

**Code-along: use INDEX and MATCH to fetch data from another table - 15 min**
* Continue using the spreadsheet from the previous code-along
* Import the products_horz.csv file into a new tab
* Use INDEX and MATCH to add the product name and price to each record in the purchases table
    
### !challenge

* type: paragraph
* id: e70eeab2-5569-46b2-9041-38bbd9fb883a
* title: Use INDEX and MATCH to fetch data from tables

##### !question

**Exercise: use INDEX and MATCH to fetch data from other tables - 25 min**
* Work in pairs
* Continue using the spreadsheet that you created in the last challenge
* Refer to the [TCP-H data Schema diagram](https://drive.google.com/file/d/150VWoQ2ZmqrOr2VZsA-EMtX9VJWDiXDI/view?usp=sharing) to determine connections between the tables
* Use INDEX and MATCH to add the country and region of the customer to each row of the orders table
* Submit a GitHub link to this spreadsheet

##### !end-question

##### !placeholder

Paste link here

##### !end-placeholder

### !end-challenge

