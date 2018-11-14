# Data importing

At work, data analysts encounter multiple formats of data text files (computer files that only contain numbers and text with no special formatting), which are used to transfer data between databases and analytics tools. Each format of text file has different advantages and disadvantages—for example, some are more human-readable, others are more compatible with the outputs of modern web design—and it’s important to know how to adapt to each. 

This lesson teaches you how to work with the most common types of data text files: comma separated values (CSV) files, JSON files, and Extensible Markup Language (XML) files. 

## Lesson objectives

*By the end of this lesson, you will be able to:*
* Describe the difference between CSV, delimited, JSON, and XML data transfer files
* Load data text files including CSV, TSV, and files with other delimiters
* Set data types on intake

## Prework
* If you don't have a version of Excel 2013 or newer on your laptop, install a recent version of Excel. This typically requires purchasing and installing Microsoft Office—at least the Excel portion.
  * Ensure that you're installing the laptop version and not the Office 356 version (cloud only)
  * The Home and Student version of Microsoft Office is sufficent
* Download and install Microsoft's [Power Query for Excel](https://www.microsoft.com/en-us/download/details.aspx?id=39379&CorrelationId=ceb0208b-85a3-444c-acfe-b09fffa6498d) add-on. You use this add-on to import additional data filetypes into Excel.
  * For the add-on to become active in Excel, you must activate a setting in Excel. You will do that in class, but if you want to activate it in Excel beforehand to play with it, you can:
    * Open Excel
    * Click File > Options > Add-Ins
    * When the dialog box opens, click on the "Manage" dropdown near the bottom of the dialog, select "COM Add-ins" and click Go
    * In the COM Add-ins dialog click "Microsoft Power Query for Excel"
    *  You should now see "Power Query" as one of the choices in the Excel menu bar

* [Video: Adding Data to a Spreadsheet (2:18)](https://teamtreehouse.com/library/adding-data-to-a-spreadsheet)
* [Reading: CSV vs XML vs JSON – Which is the Best Response Data Format?](https://applerepairstation.co.uk/csv-vs-xml-vs-json-which-is-the-best-response-data-format/)

## In-class work

### Discuss three types of text file formats for storing data - 15 min**
  * Rows and column text files such as CSV and delimited files
  * JSON
  * XML

### Code-along: import csv files delimited with various delimiters - 15 min**
  * Although many people use the names synonymously, there are differences between CSV and simpler delimited files
  * Download these files again if you don't have them available
    * [products.csv](https://s3-us-west-2.amazonaws.com/learn-assets.galvanize.com/gSchool/ds-curriculum/precourse/products.csv)
    * [purchases.txt](https://s3-us-west-2.amazonaws.com/learn-assets.galvanize.com/gSchool/ds-curriculum/precourse/purchases.txt)
  In a file manager (Explorer on Windows, Finder on Mac), click on the products.csv file to open it in Excel
    * Note that the data imported successfully; this is because this CSV file happens to designated the columns and data in a way that matches Excel's default import settings
  * Import the purchases.txt file by clicking on it 
    * Note that the data didn't import into Excel successfully; this is because you can't depend on the "click on the file in a file manager" way of importing data
  * Import using Excel's Data > From Text functionality

### !challenge

* type: paragraph
* id: bab86a06-eb77-4050-9937-e54a74110340
* title: Import data text files

##### !question

### Exercise: import files with different delimiters - 15 min**
* Work in pairs
* Import a new file using Data > From Text
* Download these Pronto files for use with Excel:
  * [2015_trip_data.csv](https://drive.google.com/file/d/1O56RgQLiOM86uH1rUizypgfzR8h1lYKI/view?usp=sharing)
  * [station.csv](https://drive.google.com/file/d/1pozO2ne6Q8SJJ0olimZqg_-xUUq08V09/view?usp=sharing)
  * [weather.csv](https://drive.google.com/file/d/1_M91l3njt9PIPurfIKz_sCVnzfwEenDy/view?usp=sharing)
* Import the 2015_trip_data.csv file into a tab (worksheet) in Excel
* Import the station.csv file into a tab in Excel
* Import the weather.csv file into a tab in Excel
* Submit a GitHub link to the spreadsheet

##### !end-question

##### !placeholder

Paste link here

##### !end-placeholder

### !end-challenge

### Code-along: import data into a JSON file - 15 min**
* ["Microsoft Power Query for Excel"](https://support.office.com/en-us/article/connect-to-a-json-file-f65207ab-d957-4bf0-bec3-a08bb53cd4c0#ID0EAACAAA=Newer_versions)
  * Note that the page contains a selection tab to select use instructions from Excel 2013 and earlier or recent versions of Excel
* Download the [heath.json](https://drive.google.com/file/d/1lsMQQzdcIHJjE6W-NfC4VMxBAUxBE5mx/view?usp=sharing) file of disease volume by US state
 * Import the JSON file into Excel from the web
   * Click on the Excel Power Query tab and then "From Web"
   * Cut/Paste this URL in the URL box: '''https://think.cs.vt.edu/corgis/json/health/health.json'''
     * Dataset description](https://think.cs.vt.edu/corgis/json/health/health.html)
   * In the dialog, enter the path and filename of the JSON file
   * Click OK
   * When the list of records appears in the editor, click transform -> to table
   * Click to expand the columns and review the column names
   * Click on Save and Load to exit and populate the Excel worksheet with the data
 * Show that to read in a JSON file that local on your laptop you use exactly the same steps but with the path and filename as the URL

### !challenge

* type: paragraph
* id: a01facea-487e-445a-b04f-0196965c00e4
* title: Import a JSON File

##### !question
**Exercise: Import a JSON file into Excel - 15 min**
* Work in pairs
* Import the [cars.json data](https://think.cs.vt.edu/corgis/json/cars/cars.html) using a downloaded file
* In an Excel worksheet tab, import the cars.json data using the URL of the file location on the web
* Submit a link to the spreadsheet

##### !end-question

##### !placeholder

Paste link here

##### !end-placeholder

### !end-challenge


### !challenge

* type: paragraph
* id: be634953-530c-4eb7-ba8e-bd5136b0dc7a
* title: Import an XML data File

##### !question

### Optional learning: import an XML file into Excel**
* Import the orders.xml file into Excel
  * Download the orders.xml file from the TPC-H Relational Database Benchmark section on [this page](http://aiweb.cs.washington.edu/research/projects/xmltk/xmldata/www/repository.html#tpc-h)
  * Use Data > Get Data > From File > From XML to import into Excel
    * Note - Depending on which version of excel you have the menu navigation may be different  

##### !end-question

##### !placeholder

Paste link here

##### !end-placeholder

### !end-challenge
 
