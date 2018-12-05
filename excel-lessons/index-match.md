# INDEX and MATCH

<div class='bg-info' style='padding:8px;border-style:solid;border-width:2px;border-color:#00BFFF'>
<strong>Aside:</strong><br>

The lessons *LOOKUP* and *INDEX and MATCH* explore Excel functions that are similar to SQL joins in that they allow you to combine data from multiple tables. Since data analysts often work with both Excel and SQL, it’s important to know how to combine data from multiple tables in both platforms.
</div>

<br>

Imagine that you have one table that contains data on the customers who have purchased products from your company and the products that they have purchased. You have a second table that contains data on the location of each customer, which you want to add to your first table. You can do this using `INDEX` and `MATCH`, the topic of this lesson. 

`INDEX` and `MATCH` performs the same function as LOOKUPs but works better with larger tables (>50,000 rows) or spreadsheets that contain a lot of interdependent logic, since `INDEX` and `MATCH` requires less computation and, therefore, performs faster. 

## Learning objectives
*By the end of this lesson, you will be able to:*
* Describe the advantages of `INDEX` and `MATCH` over LOOKUPs.
* Use `INDEX` and `MATCH` to fetch data.

## Prework
Video: [how to use Excel INDEX MATCH (the right way)](https://www.youtube.com/watch?v=F264FpBDX28) (11:31)

## In-class work

### Discuss: overview of `INDEX` and `MATCH` (15 min)
* Refer to online documentation.
* Highlight the compute efficiency advantages of `INDEX` and `MATCH`over LOOKUPs.

### Code-along: use `INDEX` and `MATCH` to fetch data from other tables (15 min)

**Notes:**

* Use these "sales" CSV files: 
    * [purchases.csv](https://drive.google.com/uc?export=download&id=1Nxvo7RzIfWELSglbDKOb1eVASXBvKgEW),
    * [customers.csv](https://drive.google.com/uc?export=download&id=1_69gMSjnx7owplIVzKu1SGdNLdNmXGez),
    * [products_horz.csv](https://drive.google.com/uc?export=download&id=1Hj1LauM6mS9qM-cbIydTgXs_Acu-iney).
* Use this lesson's [code-along solution spreadsheet's](https://drive.google.com/uc?export=download&id=1AtV3_yeH3aTi8h4eFKkhJ1_dqeeoVPtV) "INDEX MATCH to Customers" tab as an example for this code-along.

**Instructions:**
Use `INDEX` and `MATCH` to add the customer name and city from the customer table to each row of the purchases table.

1. Open a new Excel workbook and import the purchases.csv file and the customers.csv file into the same worksheet so that they are both visible.
2. In an empty column in the spreadsheet create a formula that uses MATCH to find the location of the purchases table custid in the customers table.  
3. In another column create a formula using INDEX that references the MATCH cell to retrieve the customer name.
4. In another column create a single formula using the INDEX and MATCH logic that also returns the customer name.
5. In another column modify the combined formula to retrieve the customer's city 

### !challenge

* type: paragraph
* id: 00dde750-1ac8-4667-a591-cdd9896f62fa
* title: Fetch data with INDEX and MATCH

##### !question
**Exercise: fetch data from other tables (20 min)**

**Notes:**

* Work in pairs
* Use the TCP-H Benchmark CSV files from the _LOOKUP_ lesson or download and unzip [this](https://drive.google.com/file/d/1rvKe9g7IU7MXVYQMKTy9ulYY-J60-an3/view?usp=sharing) file, which contains the TCP-H tables. Alternately, you can download the files individually [here](https://drive.google.com/drive/folders/1dwWXz3uoB_JVc0lcJXaDDU6nyt9v5aEl?usp=sharing).
* [TCP-H data Schema diagram](https://drive.google.com/file/d/150VWoQ2ZmqrOr2VZsA-EMtX9VJWDiXDI/view?usp=sharing).

**Instructions:**

1. Import orders.csv into an Excel worksheet and name the worksheet "Orders."
2. Import customers.csv into a second worksheet and name the worksheet "Customers."
3. Using `INDEX` and `MATCH`, add a column to the Orders sheet named "Cust_name" that contains the name of the customer for each order row.
4. Using `INDEX` and `MATCH`, add another column to the Orders sheet named "Mrkt_segment" that contains the market segment for the customer for each order row.
5. Submit a GitHub link to this spreadsheet in the box below.

##### !end-question

##### !placeholder

Paste your GitHub link here:

##### !end-placeholder

### !end-challenge

### Code-along: use `INDEX` and `MATCH` to fetch data from a horizontal table (15 min)

**Notes:**

* Continue using the spreadsheet that you finished with in the previous code-along.
* Use this lesson's [code-along solution spreadsheet's](https://drive.google.com/uc?export=download&id=1AtV3_yeH3aTi8h4eFKkhJ1_dqeeoVPtV) "INDEX MATCH to Products" tab as an example for this code-along.

**Instructions:**

1. Open a new Excel tab and import the [purchases.csv](https://drive.google.com/uc?export=download&id=1Nxvo7RzIfWELSglbDKOb1eVASXBvKgEW) file and the [products_horz.csv](https://drive.google.com/uc?export=download&id=1Hj1LauM6mS9qM-cbIydTgXs_Acu-iney) file into the same worksheet so that they are both visible.
2. In an empty column in the spreadsheet create a formula that uses MATCH to find the location of the purchases table prodid in the products table.  
3. In another column create a formula using INDEX that references the MATCH cell to retrieve the product name.
4. In another column create a single formula using the INDEX and MATCH logic that also returns the product name.
5. In another column modify the combined formula to retrieve the product's price 
    
### !challenge

* type: paragraph
* id: e70eeab2-5569-46b2-9041-38bbd9fb883a
* title: Use INDEX and MATCH to fetch data from tables

##### !question

**Exercise: use INDEX and MATCH to fetch data from other tables (25 min)**

**Notes:** 

* Work in pairs.
* Continue using the spreadsheet that you created in the previous challenge.
* Refer to the [TCP-H data Schema diagram](https://drive.google.com/file/d/150VWoQ2ZmqrOr2VZsA-EMtX9VJWDiXDI/view?usp=sharing) to determine connections between the tables.

**Instructions:**

1. Use `INDEX` and `MATCH` to add the country and region of the customer to each row of the orders table.
2. Submit a GitHub link to the spreadsheet in the box below.

##### !end-question

##### !placeholder

Paste your GitHub link here:

##### !end-placeholder

### !end-challenge

## Solutions
Example solutions to the exercises in this lesson are available in [this](https://drive.google.com/uc?export=download&id=1I5THzik_mmM8ISn7HKi_zj58mAgvVdny) spreadsheet. These are intended for use after the exercises are completed.

## Resources
Video: [Excel INDEX MATCH advanced: look up multiple criteria in rows or columns](https://www.youtube.com/watch?v=ontXHp9cwOQ) (10:21)
