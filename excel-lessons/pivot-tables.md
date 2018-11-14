# Pivot tables

2 hrs
<br><br>
 
One of the most important analysis techniques is determining aggregate values for each distinct value in a category column.  For example, you may want to determine the total web page impressions by country for a website. pivot tables are a quick and interactive way to do that. In this lesson, you create pivot tables that provide the aggregations that you need.

### Learning objectives:
*By the end of this lesson, you will be able to:*
* Define what a pivot table is
* Describe how split-aggregate-combine logic creates a pivot table
* Apply Excel's pivot table capability to generate aggregates grouped by distinct values of columns
<br>

## Pre-work:
* [Video: Pivot Tables (13:10)](https://www.youtube.com/watch?v=BkmxrvIfDGA&list=PL_iwD7O7FG7jzLQIYm6-9Gx3hvXVUG7C5&index=11)
* [Video: Pivot Tables Made Easy with Recommended Pivot Tables (5:16)](https://www.youtube.com/watch?v=ebdgGbsTWs8&list=PL_iwD7O7FG7jzLQIYm6-9Gx3hvXVUG7C5&index=12)

### Use pivot tables to look at aggregates sliced by categories
**Overview of pivot tables - 20 min**
* Discuss the purpose, importance, and structure of pivot tables
* Share how pivot tables are Excel's method for creating aggregates group by distinct column values
  * [pivot tables - split apply combine in Excel](https://www.safaribooksonline.com/library/view/learning-pandas/9781783985128/graphics/5128OS_09_01.jpg)
* Review Excel's pivot table capabilities and limitations
<br>

**Code-along: export data from a database using pgAdmin - 10 min**
* Extract data from the da_readychef schema
* Work in pairs and explain the SQL code below to each other

```
   Select e.dt, e.meal_id, event, type as meal_type, price as meal_price
   From da_readychef.events e
      Left Join da_readychef.meals m ON e.meal_id = m.meal_id
      -- Note: INNER JOIN would work if we are sure the meal_id column in da_readychef.meal contains primary keys
   Where TRUE
      And e.dt Between '2013-12-01' And '2013-12-31'
      And event = 'bought'
```

* Run the query to extract data from the da_readychef schema
 * Export to a CSV file using a "|" delimiter example
   * Show that export preferences are set in pgAdmin by clicking ```File -> Preferences -> SQL Editor -> CSV Output```


**Code-along: create pivot tables in Excel - 20 min**
* Use the readychef table from the previous code-along to provide the data for this Excel code-along
* Create a pivot table  
  * Read the CSV file into an Excel spreadsheet tab
  * Select the data table and turn it into an Excel table named readychef_meals
  * Create a pivot table that displays each date (as pivot table ROWS) and the total price of meals (as pivot table VALUE)
* Modify the pivot table by adding meal type to the rows
  * Show the effect of moving the meal_type above and then below the date attribute in the ROWS pane
  * Position the meal_type above the date in the ROWS pane
* Demonstrate how to change the aggregation type in the VALUES pane by demonstrating with meal price
  * Add an average price column to the VALUES pane
<br>


### !challenge

* type: paragraph
* id: b077b94d-e453-46f6-9ab6-270ef1386c45
* title: Create a pivot table

##### !question
**Exercise: create a pivot table that sums - 25 min**
* Answer the question "What dates in early fall of 2015 did people use bikes the longest?"
* Work in pairs
* Extract data from the da_pronto.trip table
  * Run the query below to extract the date, from station name, from station id, to_station_id, gender, birthyear, and tripduration from the da_pronto.trip table

```
   Select date(starttime), from_station_name, from_station_id, to_station_id, gender, birthyear, tripduration
   From da_pronto.trip
   Where date(starttime) Between '2015-08-01' And '2015-10-31'
```  
  * Export to a CSV file
* Create a pivot table 
  * Read the CSV file into an Excel spreadsheet tab
  * Select the data table and turn it into an Excel table with a range name
  * Create a pivot table that displays the date and sum and average trip duration for each of those dates
  * Determine which date has the longest average trip duration
* Determine which from_stations had the longest rental times 
  * Modify the pivot table by adding the from_station_id *below* the date in the ROWS area
    * Move the from_station_id above the data attribute in the ROWS pane to group the pivot table by from_station_id and then date
  * Add a column of the minimum trip duration to the pivot table
  * Add a column of the maximum trip duration to the pivot table
* Determine which station has the rental with the longest trip duration
* Submit a GitHub link to your spreadsheet
* Additional learning: play around with adding fields to various panes of the pivot table editor and see the changes that you make to the pivot table 
<br>

##### !end-question

##### !placeholder

Submit the link here

##### !end-placeholder

### !end-challenge


**Code-along: improve user experience by formatting pivot tables - 20 min**
* Continue using the spreadsheet from the previous code-along
* Demonstrate that pivot tables don't auto update
  * Demonstrate how to manually trigger an update
* Format pivot tables to make them easier to interpret
 * Sort of columns in pivot tables (primary and secondary sorts) including a sort of trip duration
   * Note that what is primary and what is secondary is dependent on the position of the column in the pivot table
   * Note how the sort is a sort of the trip duration values within the grouping defined by the ROW field values
 * Add subtotals and grand totals
 * Add filters for dimensions in a pivot table
   * Add a filter for the meal type in the pivot table's FILTER area
   * Show that a filter can be either in the FILTERS area or in ROWS or COLUMNS, but not both
     * For an attribute in ROWS or COLUMNS, use the filter drop-down in the pivot table location
 * Show that row and column names, such a "Row Labels," can be manually changed to make it easier for the user to interpret 

### !challenge

* type: paragraph
* id: 75c9e17d-5cae-4605-9518-91d8d8a4acf2
* title: Format pivot tables

##### !question

**Exercise: make a pivot table more useful - 25 min**
* Continue using the Pronto spreadsheet from the first challenge
* Modify the pivot table by adding gender to the COLUMNS pane
* Make the following changes to improve the user experience
  * Sort by the sum of the duration decending
  * Add subtotals where you think that they're appropriate
  * Format the table; add more descriptive column headers
  * Add a filter for birthyear
  * Modify column names in the pivot table to make them easier to understand (if needed)
* Submit a GitHub link to the spreadsheet

##### !end-question

##### !placeholder

Submit the link here

##### !end-placeholder

### !end-challenge
