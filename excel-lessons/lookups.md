# VLOOKUP & HLOOKUP

<div class='bg-info' style='padding:8px;border-style:solid;border-width:2px;border-color:#00BFFF'>
<strong>Aside:</strong><br>

The lessons *VLOOKUP* and *INDEX and MATCH* explore Excel functions that are similar to SQL joins in that they allow you to combine data from multiple tables. Since data analysts often work with both Excel and SQL, it’s important to know how to combine data from multiple tables in both platforms.
</div>

<br>

This lesson covers `VLOOKUP` and `HLOOKUP`, Excel functions that find and retrieve data from a specific column or row in a table. For example, if you have a list that contains products and the price of each product, you can search for the price of a *specific* product. 

With VLOOKUP, the value that you look up must exist in the first *column* of the table, with the value being returned existing in an adjacent column. With HLOOKUP, the value that you look up must exist in the first *row* of the table, with the value being returned existing in an adjacent row. (The “V” in `VLOOKUP` stands for “vertical”, and the “H” in `HLOOKUP` stands for “horizontal.”) VLOOKUP is more common, since most tables are organized vertically. 

## Learning objectives
*By the end of this lesson, you will be able to:*
* Use `VLOOKUP` and `HLOOKUP` to fetch data.
* Apply parameters to alter a LOOKUP.
 
## Prework
* Video: [2 Practical Excel Lookup Examples](https://www.youtube.com/watch?v=hwL6KKJP-_I).

---

## In-class work

### Discuss: overview of the VLOOKUP function (10 min)
* Use online documentation.
* LOOKUPs allow you to join data from one Excel table to another table.
* You need to typically set the "Range LOOKUP" parameter to FALSE!
    * It's beneficial to look at default parameters and the other options that are available to you.
    * Note limitations such as LOOKUPs returning only the first match of the external table.

### Code-along: use `VLOOKUP` to fetch data (15 min)

**Notes:**

* Use LOOKUPs to join data from different Excel tables (a very limited type of join).
* Use these three "sales" CSV files:
    * [purchases.csv](https://drive.google.com/uc?export=download&id=1Nxvo7RzIfWELSglbDKOb1eVASXBvKgEW). 
    * [customers.csv](https://drive.google.com/uc?export=download&id=1_69gMSjnx7owplIVzKu1SGdNLdNmXGez).
    * [products_horz.csv](https://drive.google.com/uc?export=download&id=1Hj1LauM6mS9qM-cbIydTgXs_Acu-iney).

**Instructions:**
 
1. Use `VLOOKUP` to add the customer name and city from the customer table to each row of the purchases table.
    * Eventually you get errors as you copy the formula to all the rows.
    * You must use absolute references; otherwise, the table_range moves when you copy the `VLOOKUP` formula to another cell.
2. Modify the formula to use absolute references and show the results.
3. Alternately, use range names as the reference table range in the LOOKUPs. Change the `VLOOKUP` reference table_array value to a range name and use that in the `VLOOKUP` formula.

### !challenge

* type: paragraph
* id: 03e30b6b-8e09-4eaf-a9e5-60d532341d22
* title: Fetch data with LOOKUPs

##### !question
**Exercise: fetch data from other tables (15 min)**

**Notes:**

* Work in pairs.
* Use the TCP-H Benchmark data set.
    * Download and unzip [this](https://drive.google.com/uc?export=download&id=1rvKe9g7IU7MXVYQMKTy9ulYY-J60-an3) file containing the TCP-H tables. Alternately, download the files individually [here](https://drive.google.com/open?id=1dwWXz3uoB_JVc0lcJXaDDU6nyt9v5aEl).
* [TCP-H data Schema diagram](https://drive.google.com/uc?export=download&id=150VWoQ2ZmqrOr2VZsA-EMtX9VJWDiXDI).

**Instructions:**

1. Import orders.csv into an Excel worksheet. Name the worksheet "Orders."
2. Import customers.csv into a second worksheet. Name the worksheet "Customers."
3. Using `VLOOKUP`, add a column to the Orders sheet named "Cust_name" that contains the name of the customer for each order row.
4. Using `VLOOKUP`, add another column to the Orders sheet named "Mrkt_segment" that contains the market segment for the customer for each order row.
5. Submit a GitHub link to the spreadsheet in the box below.

##### !end-question

##### !placeholder

Paste your GitHub link here:

##### !end-placeholder

### !end-challenge

### Code-along: use `HLOOKUP` to fetch data from another table (10 min)

**Notes:**

Continue using the spreadsheet that you finished with in the previous code-along.

**Instructions:**

1. Import the [products_horz.csv](https://drive.google.com/open?id=1Hj1LauM6mS9qM-cbIydTgXs_Acu-iney) file into a new tab.
2. Looking at the imported data, note that the id values that you want to join are in columns rather than rows; you can use `HLOOKUP` to retrieve the name of the product for each purchase in the purchase table.
3. Use `HLOOKUP` to add the product name and price to each record in the purchases table.
    
### !challenge

* type: paragraph
* id: 6f4149ae-909b-40c5-8732-768fa5bc397d
* title: Use LOOKUPS to fetch data from tables

##### !question

**Exercise: use LOOKUPs to fetch data from other tables (25 min)**

**Notes:**

* Work in pairs.
* Continue using the spreadsheet that you created in the last challenge.

**Instructions:**

1. Refer to the [TCP-H_Schema](https://drive.google.com/file/d/150VWoQ2ZmqrOr2VZsA-EMtX9VJWDiXDI/view?usp=sharing) diagram to determine connections between the tables.
2. Add the country and region of the customer to each row of the orders table; to do this...
    * Import the nation.csv file into an Excel tab (worksheet). (See the previous exercise for the location of the nation.csv file.)
    * Import the [region_horz.csv](https://drive.google.com/open?id=1d7TUbr475M_9HNiKcGUcOsMPKeklwrbj) file into an Excel tab.
    * Use `HLOOKUP` to add a Region column to the country.
    * Use a LOOKUP to add the country and region to each line of the orders table.
3. Submit a GitHub link to the spreadsheet in the box below.

##### !end-question

##### !placeholder

Paste your GitHub link here:

##### !end-placeholder

### !end-challenge

---

## Solutions
Example solutions to the exercises in this lesson above are available in [this](https://drive.google.com/uc?export=download&id=1I5THzik_mmM8ISn7HKi_zj58mAgvVdny) spreadsheet. These are intended for use after the exercises are completed.

