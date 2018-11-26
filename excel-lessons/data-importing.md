# Importing Data

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
* [Video: Adding Data to a Spreadsheet (2:18)](https://teamtreehouse.com/library/adding-data-to-a-spreadsheet)
* [Reading: CSV vs XML vs JSON – Which is the Best Response Data Format?](https://applerepairstation.co.uk/csv-vs-xml-vs-json-which-is-the-best-response-data-format/)

## In-class work

### Discuss three types of text file formats for storing data - 15 min

Search and find descriptions and documentation for these three data text files.  They all are file types that store data as text.

Compare and contrast these data text files and their formats
  * CSV and other delimited files - Rows and column data text files
      * Although many people use the names synonymously, there are differences between CSV and simpler delimited files
  * JSON
      We will work with JSON in much more depth in Tablea part 2 when we retrieve data from APIs 
  * XML

### Code-along: import CSV files delimited with various delimiters - 15 min

**Instructions:**

1. Download these files for use in this code along
    * [products.csv](https://s3-us-west-2.amazonaws.com/learn-assets.galvanize.com/gSchool/ds-curriculum/precourse/products.csv)
    * [purchases.txt](https://s3-us-west-2.amazonaws.com/learn-assets.galvanize.com/gSchool/ds-curriculum/precourse/purchases.txt)
2. In a file manager (Explorer on Windows, Finder on Mac), click on the products.csv file to open it in Excel
    * Note that the data imported successfully; this is because this CSV file *happens* to be encoded in a way that matches Excel's default import settings
3. In a file manager such as Finder (Mac) or Explorer (Windows) click on the purchases.txt file to import it
    * Note that the data didn't import into Excel successfully.   As analyts we can not depend on the "click the file in a file manager" way of importing data into Excel!
        * Rather,  our habit for importing CSV and delimited files should be to import delimited files using Excel's Data > From Text functionality
4. View the purchases.txt file in a text editor such as Notepad (Windows), TextEdit (Mac) or a text editor with more functionality such as Atom (preferred by Galvanize) or Sublime
4. Import purchase.txt using Excel's menu ribbon Data > From Text
      * Chose settings in the From Text dialog to import the data successfully from the file

### !challenge

* type: paragraph
* id: bab86a06-eb77-4050-9937-e54a74110340
* title: Import data text files

##### !question

### Exercise: import files with different delimiters - 15 min

**Notes:**

* In this exercise you will import several delimited text data files into Excel.
* Make sure you import dates as dates in Excel rather than be importing into Excel text fields 

**Instructions:**

In this exercise you will import several delimited text data files into Excel.

1. Work in pairs
2. Import a new file using Data > From Text
3. Download these Pronto files for use with Excel:
    * [2015_trip_data.csv](https://drive.google.com/uc?export=download&id=1O56RgQLiOM86uH1rUizypgfzR8h1lYKI)
    * [station.csv](https://drive.google.com/uc?export=download&id=1pozO2ne6Q8SJJ0olimZqg_-xUUq08V09)
    * [weather.csv](https://drive.google.com/uc?export=download&id=1_M91l3njt9PIPurfIKz_sCVnzfwEenDy)
4. Import the 2015_trip_data.csv file into a tab (worksheet) in Excel
5. Import the station.csv file into a new tab in Excel
6. Import the weather.csv file into a new tab in Excel
7. Submit a GitHub link to the spreadsheet

##### !end-question

##### !placeholder

Paste link here

##### !end-placeholder

### !end-challenge

### Code-along: import data into a JSON file - 15 min

**Notes:**

* In this code-along we will import data from a text data file that has data encoded in the JSON format.  Right now, we will not go deep into the detail of the JSON file format.  However, we will examine the JSON file format in more depth in the Tableau part 2 "Retrieve data with APIs" lesson.  In this code-along we focus on importing data from JSON files.

* For simplicity we will convert JSON files into CSV files using an online converter.  There are also converters for your laptop that you can use for very large data files or files with information that should not be shared publically.

**Instructions:**

1. Download the [heath.json](https://drive.google.com/uc?export=download&id=1lsMQQzdcIHJjE6W-NfC4VMxBAUxBE5mx) file of disease instances per US state
2. Examine the JSON file in a text editor and note that it is quite different from a delimited file in format.
3. Use an online JSON to CSV converter such as [this one](http://www.convertcsv.com/json-to-csv.htm) to convert the file.
    * Discuss the setting available
4. Download the resulting CSV file.
5. Import the data into Excel.
6. Examine the results to determine if the file conversion and import was successful.

### !challenge

* type: paragraph
* id: a01facea-487e-445a-b04f-0196965c00e4
* title: Import a JSON File

##### !question
**Exercise: Import a JSON file into Excel - 15 min**

**Notes:**

In this lesson you will import the [cars.json data](https://think.cs.vt.edu/corgis/json/cars/cars.html) data into Excel. 

**Instructions:**

1. Work in pairs
2. Download the [cars.json data](https://think.cs.vt.edu/corgis/json/cars/cars.html) JSON file
3. Convert it to a CSV or other delimited file
4  Load data from the resulting CSV or delimited file into an Excel worksheet tab
5. Optional learning
    * Open another tab in Excel
    * Use an online converter to convert to the JSON data to a CSV file but this time have the converter retrieve the cars.json file directly from its web  URL rather than downloading the file first.
        * Hint: look for the option to retieve from the web in the converter's options
* Submit a link to the spreadsheet location in Github

##### !end-question

##### !placeholder

Paste link here

##### !end-placeholder

### !end-challenge

### Code-along: *optional* extra learning - Import an XML data file

**Notes:**

In this code-along you will import an XML data file into Excel. 

**Instructions:**

1. Download the part.xml file from the TPC-H Relational Database Benchmark section on [this page](http://aiweb.cs.washington.edu/research/projects/xmltk/xmldata/www/repository.html#tpc-h)
2. Use Data > From Other Sources > From File > From XML Data Import to import the parts data into an Excel tab
3. Examine results of the date import into Excel to confirm the data loaded correctly

## Solutions
Example solutions to the exercises in this lesson above are available in [this spreadsheet](https://drive.google.com/uc?export=download&id=1JKcyAntKu4jzQHzJtgkmq1hXyb6QfFFJ). These are intended for use after the exercises are completed.
