# Importing data (Excel)

At work, data analysts encounter multiple formats of data text files (computer files that only contain numbers and text with no special formatting), which are used to transfer data between databases and analytics tools. Each format of text file has different advantages and disadvantages—for example, some are more human-readable, others are more compatible with the outputs of modern web design—and it’s important to know how to adapt to each. 

This lesson teaches you how to import the most common types of data text files to Excel: comma separated values (CSV) files, JSON files, and Extensible Markup Language (XML) files. 

## Lesson objectives

*By the end of this lesson, you will be able to:*
* Describe the difference between CSV, delimited, JSON, and XML data transfer files.
* Load data text files including CSV, TSV, and files with other delimiters.
* Set data types on intake.

## Prework
* If you don't have a version of Excel 2013 or newer on your laptop, install a recent version of Excel. (The Home and Student version of Microsoft Office is sufficient.)
    * Ensure that you're installing the laptop version and not the Office 356 version (cloud only).
* Video: [adding data to a spreadsheet](https://teamtreehouse.com/library/adding-data-to-a-spreadsheet).
* Text: [CSV vs XML vs JSON – which is the best response data format?](https://applerepairstation.co.uk/csv-vs-xml-vs-json-which-is-the-best-response-data-format/).

## In-class work

### Discuss CSV, JSON, and XML files (15 min)

* Search for and find descriptions and documentation for these three data text files. They're all file types that store data as text.
* Compare and contrast these data text files and their formats:
    * **CSV** and other delimited files, rows and column data text files. (Although many people use the names synonymously, there are differences between CSV and simpler delimited files.)
    * **JSON**. (You work with JSON in more depth in _Tableau part 2_.)
    * **XML**.

### Code-along: import CSV files delimited with various delimiters (15 min)

**Notes:**

Download the files [products.csv](https://s3-us-west-2.amazonaws.com/learn-assets.galvanize.com/gSchool/ds-curriculum/precourse/products.csv) and [purchases.txt](https://s3-us-west-2.amazonaws.com/learn-assets.galvanize.com/gSchool/ds-curriculum/precourse/purchases.txt).

**Instructions:**

1. In your file manager (Explorer on Windows, Finder on Mac), click on the _products.csv_ file to open it in Excel. 
    * Note that the data imports successfully because this CSV file is encoded in a way that matches Excel's default import settings.
2. In your file manager, click on the purchases.txt file to open it in Excel. 
    * Note that the data doesn't import into Excel successfully. Analysts can't depend on the click-the-file-in-a-file-manager way of importing data into Excel. Rather, import CSV and delimited files using Excel's Data > From Text functionality.
3. View the purchases.txt file in a text editor such as Notepad (Windows), TextEdit (Mac), or a text editor with more functionality, like VSCode (preferred by Galvanize), ATOM, or Sublime.
4. Import purchase.txt using Excel's menu ribbon Data > From Text functionality.
    * Select settings in the From Text dialog to import the data successfully from the file.

### !challenge

* type: paragraph
* id: bab86a06-eb77-4050-9937-e54a74110340
* title: Import data text files

##### !question

**Exercise: import files with different delimiters (15 min)**

**Notes:**

* Import several delimited text data files into Excel.
* Work in pairs.
* Be sure to import dates as _dates_ in Excel rather than import dates as text fields in Excel.

**Instructions:**

1. Import a new file using Data > From Text functionality.
2. Download these Pronto files:
    * [2015_trip_data.csv](https://drive.google.com/uc?export=download&id=1O56RgQLiOM86uH1rUizypgfzR8h1lYKI).
    * [Station.csv](https://drive.google.com/uc?export=download&id=1pozO2ne6Q8SJJ0olimZqg_-xUUq08V09).
    * [Weather.csv](https://drive.google.com/uc?export=download&id=1_M91l3njt9PIPurfIKz_sCVnzfwEenDy).
3. Import the 2015_trip_data.csv file into a new tab (worksheet) in Excel.
4. Import the station.csv file into a new tab in Excel.
5. Import the weather.csv file into a new tab in Excel.
6. Submit a GitHub link to the spreadsheet in the box below.

##### !end-question

##### !placeholder

Paste your GitHub link here:

##### !end-placeholder

### !end-challenge

### Code-along: import data into a JSON file (15 min)

**Notes:**

* Import data from a text data file that has data encoded in the JSON format.
* For simplicity, convert JSON files into CSV files using an online converter. There are also converters for your laptop that you can use for very large data files or files with information that should not be shared publicly.

**Instructions:**

1. Download the [heath.json](https://drive.google.com/uc?export=download&id=1lsMQQzdcIHJjE6W-NfC4VMxBAUxBE5mx) file of disease instances per US state.
2. Examine the JSON file in a text editor and note that it's different from a delimited file in format.
3. Use an online JSON to CSV converter such as [this one](http://www.convertcsv.com/json-to-csv.htm) to convert the file. Discuss the available settings.
4. Download the resulting CSV file.
5. Import the data into Excel.
6. Examine the results to determine if the file conversion and import was successful.

### !challenge

* type: paragraph
* id: a01facea-487e-445a-b04f-0196965c00e4
* title: Import a JSON File

##### !question
**Exercise: Import a JSON file into Excel (15 min)**

**Notes:**

* Import the [cars.json](https://think.cs.vt.edu/corgis/json/cars/cars.html) data into Excel. 
* Work in pairs.

**Instructions:**

1. Download the [cars.json](https://think.cs.vt.edu/corgis/json/cars/cars.html) data JSON file.
2. Convert the file to a CSV or other delimited file.
3. Load data from the resulting CSV or delimited file into an Excel worksheet tab.
4. For optional learning: 
    * Open another tab in Excel.
    * Use an online converter to convert to the JSON data to a CSV file, but this time have the converter retrieve the cars.json file directly from its web URL rather than downloading the file first. (Hint: look for the option to retrieve the file from the web in the converter's options.)
5. Submit a GitHub link to the spreadsheet in the box below.

##### !end-question

##### !placeholder

Paste your GitHub link here:

##### !end-placeholder

### !end-challenge

### Optional code-along: import an XML data file

**Notes:**

Import an XML data file into Excel. 

**Instructions:**

1. Download the part.xml file from the TPC-H Relational Database Benchmark section on [this](http://aiweb.cs.washington.edu/research/projects/xmltk/xmldata/www/repository.html#tpc-h) page.
2. Use Data > From Other Sources > From File > From XML Data Import functionality to import the part.xml data into an Excel tab.
3. Examine results of the data import into Excel to confirm that it loaded correctly.

## Solutions
Example solutions to the exercises in this lesson above are available in [this](https://drive.google.com/uc?export=download&id=1JKcyAntKu4jzQHzJtgkmq1hXyb6QfFFJ) spreadsheet. These are intended for use after the exercises are completed.
