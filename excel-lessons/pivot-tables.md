# Pivot tables

This lesson explores pivot tables. An Excel pivot table allows you to quickly and easily calculate aggregates grouped by dimensions.  Because it provides an easy drag-and-drop method, you can rapidly slice the data with different dimensions.  

<div class='bg-info' style='padding:8px;border-style:solid;border-width:2px;border-color:#00BFFF'>
<strong>Aside:</strong><br>
Excel pivot tables are similar to SQL’s `GROUP BY` statement and Tableau’s tables. Since data analysts often work with each of these platforms, it’s good to know how to perform this functionality in each. 

</div>

<br>

For example, imagine that you want to know how users interact with the videos on your company’s website. You have data on each user’s age, gender, and the amount of time that they spent watching each video. With this data, you can quickly create a pivot table that displays the average amount of time that users spent watching videos by age, and then rearrange the data to create a second pivot table that displays the average amount of time that users spent watching videos by gender. You can even add filters that allow you to see the averages for a specific video.

## Learning objectives
*By the end of this lesson, you will be able to:*
* Describe what a pivot table is.
* Describe how the pivot table's logic is simialr to SQL's aggregates with GROUP BY.
* Apply Excel's pivot table capabilities to generate aggregates grouped by distinct values of columns.

## Prework
* Video: [advanced Excel - creating pivot tables in Excel tutorial 2018](https://www.youtube.com/watch?v=BkmxrvIfDGA&list=PL_iwD7O7FG7jzLQIYm6-9Gx3hvXVUG7C5&index=11).
* Video: [advanced Excel - using "recommended pivot tables"](https://www.youtube.com/watch?v=ebdgGbsTWs8&list=PL_iwD7O7FG7jzLQIYm6-9Gx3hvXVUG7C5&index=12).

## In-class work

### Discuss: overview of pivot tables (20 min)
* Discuss the purpose, importance, and structure of pivot tables.
* Share how pivot tables are Excel's method for calculating aggregates grouped by distinct column values.
* Review Excel's pivot table capabilities and limitations. ([Here](https://support.office.com/en-us/article/overview-of-pivottables-and-pivotcharts-527c8fa3-02c0-445a-a2db-7794676bce96)'s a good source of information.)

### Code-along: export data from a database using pgAdmin (10 min)

**Notes:**

* Use data from the da_readychef schema.
* Work in pairs.

**Instructions:**

1. Extract data from the da_readychef schema.
2. Explain this SQL code to your partner:

```SQL
   Select e.dt, e.meal_id, event, type as meal_type, price as meal_price
   From da_readychef.events e
      Left Join da_readychef.meals m ON e.meal_id = m.meal_id
      -- Note: INNER JOIN would work if we are sure the meal_id column in da_readychef.meal contains primary keys
   Where TRUE
      And e.dt Between '2013-12-01' And '2013-12-31'
      And event = 'bought'
```

3. Run the query to extract data from the da_readychef schema.
4. Export the data to a CSV file using a "|" delimiter example.
5. Show that the export preferences are set in pgAdmin by clicking `File -> Preferences -> SQL Editor -> CSV Output`.

### Code-along: create pivot tables in Excel (20 min)

**Notes:** 

* Create a pivot table.
* Use the readychef table from the previous code-along to provide the data for this Excel code-along.

**Instructions:**

1. Import the CSV file into an Excel spreadsheet tab.
2. In Excel, select the data table and give it a range name of "readychef_meals."
3. Create a pivot table that displays each date (as pivot table ROWS) and the total price of meals (as pivot table VALUE).
4. Modify the pivot table by adding meal type to the rows.
5. Show the effect of moving the meal_type above and then below the date attribute in the ROWS pane.
6. Position the meal_type above the date in the ROWS pane.
7. Demonstrate how to change the aggregation type in the VALUES pane with meal price.
8. Add an average price column to the VALUES pane.

### !challenge

* type: paragraph
* id: b077b94d-e453-46f6-9ab6-270ef1386c45
* title: Create a pivot table

##### !question

**Exercise: create a pivot table that contains aggregates (25 min)**

**Notes:**

* Use a pivot table to determine the dates in early fall of 2015 that people used bikes the longest.
* Use the da_pronto.trip table.
* Work in pairs.

**Instructions**

1. Extract data from the da_pronto.trip table.
2. Run the following query to extract the date, from station name, from station id, to_station_id, gender, birthyear, and tripduration from the da_pronto.trip table:

```
   Select date(starttime), from_station_name, from_station_id, to_station_id, gender, birthyear, tripduration
   From da_pronto.trip
   Where date(starttime) Between '2015-08-01' And '2015-10-31'
```  

3. Export this data to a CSV file.
4. Read the CSV file into an Excel spreadsheet tab.
5. In Excel, select the data table and give it a range name.
6. Create a pivot table that displays the date, and the sum and average trip duration for each of those dates.
7. Determine which date has the longest average trip duration.
8. Determine which from_stations have the longest rental times. 
9. Modify the pivot table by adding the from_station_id *below* the date in the ROWS area.
10. Move the from_station_id above the data attribute in the ROWS pane to group the pivot table by from_station_id and then date.
11. Add a column of the _minimum_ trip duration to the pivot table.
12. Add a column of the _maximum_ trip duration to the pivot table.
13. Determine which station has the rental with the longest trip duration.
14. Submit a GitHub link to the spreadsheet in the box below.
15. Optional: play around with adding fields to various panes of the pivot table editor and see the changes that you make to the pivot table.

##### !end-question

##### !placeholder

Paste your GitHub link here:

##### !end-placeholder

### !end-challenge


### Code-along: improve the user experience by formatting pivot tables (20 min)

**Notes:**

Continue using the spreadsheet from the previous code-along.

**Instructions:** 

1. Demonstrate that pivot tables don't auto update.
2. Demonstrate how to manually trigger an update.
3. Format pivot tables to make them easier to interpret.
4. Sort the columns in the pivot tables (primary and secondary sorts) including a sort of a pivot table aggregate column.
    * Note that the sort of an aggregate pivot table field sorts within the group bys defined by the ROW field values.
5. Add subtotals and grand totals.
6. Add filters for a couple of dimensions in the pivot table.
    * Add a filter for the meal type in the pivot table's FILTER area.
    * Show that a filter can be either in the FILTERS area or in ROWS or COLUMNS, but not both.
    * For an attribute in ROWS or COLUMNS, use the filter drop-down in the pivot table location.
8. Show that row and column names, such a "Row Labels," can be manually changed to make it easier for the user to interpret. 

### !challenge

* type: paragraph
* id: 75c9e17d-5cae-4605-9518-91d8d8a4acf2
* title: Format pivot tables

##### !question

**Exercise: improve the formatting of a pivot table (25 min)**

**Notes:** 

Continue using the Pronto spreadsheet from the first challenge.

**Instructions:** 

1. Modify the pivot table by adding gender to the COLUMNS pane.
2. Remove the MIN and MAX fields from the pivot table.
3. Sort by the sum of the trip duration descending.
4. Make a change to the subtotals and total settings.
5. Add a filter for birth year.
6. Modify column names in the pivot table to make them easier to understand (if needed).
7. Remove unnecessary decimal digits from the numerical values.
8. Submit a GitHub link to the spreadsheet in the box below.

##### !end-question

##### !placeholder

Paste your GitHub the link here:

##### !end-placeholder

### !end-challenge

### Exercise: create pivot table analysis from project data (55 min)

**Notes:**

* Work individually.
* Create pivot table analysis from data extracted from database data.

**Instructions:**

1. Create and submit queries to your project database to get data from two tables.
2. Import data from your queries into Excel.
3. Clean each raw data table.
4. Create a new worksheet and use INDEX/Match to combine data from the data tables into a single table.
5. Extract text or date parts into a new column.
6. Create at least two pivot tables to analyze the data.
7. Sort and format the pivot tables so that they're ready to share with a stakeholder.

## Solutions
Example solutions to the exercises in this lesson above are available in [this](https://drive.google.com/uc?export=download&id=1o5tJpQQ6mcPWhNaNE4SR5El2FhWCTF9Y) spreadsheet. These are intended for use after the exercises are completed.

## Postwork
Complete the Excel portion of your Student Project. 
