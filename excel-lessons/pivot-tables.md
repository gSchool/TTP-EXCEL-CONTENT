# Pivot tables

This lesson explores pivot tables. A pivot table allows you to quickly and automatically summarize large amounts of data using an easy drag-and-drop method, which you can then reorganize (or, in other words, “pivot”) and add to or take away from.

<div class='bg-info' style='padding:8px;border-style:solid;border-width:2px;border-color:#00BFFF'>
<strong>Aside:</strong><br>
Excel pivot tables are similar to SQL’s `GROUP BY` statement and Tableau’s tables. Since data analysts often work with each of these platforms, it’s important to know how to perform this functionality in each. 

</div>

<br>

For example, imagine that you want to know how users interact with the videos on your company’s website. You have data on each user’s age, gender, and the amount of time that they spent watching each video. With this data, you can quickly create a pivot table that displays the average amount of time that users spent watching videos by age, and then rearrange the data to create a second pivot table that displays the average amount of time that users spent watching videos by gender. You can even add filters that allow you to see the averages for a specific video.

## Learning objectives:
*By the end of this lesson, you will be able to:*
* Define what a pivot table is
* Describe how split-aggregate-combine logic creates a pivot table
* Apply Excel's pivot table capability to generate aggregates grouped by distinct values of columns
<br>

## Prework:
* [Video: Pivot Tables (13:10)](https://www.youtube.com/watch?v=BkmxrvIfDGA&list=PL_iwD7O7FG7jzLQIYm6-9Gx3hvXVUG7C5&index=11)
* [Video: Pivot Tables Made Easy with Recommended Pivot Tables (5:16)](https://www.youtube.com/watch?v=ebdgGbsTWs8&list=PL_iwD7O7FG7jzLQIYm6-9Gx3hvXVUG7C5&index=12)

## In-class work

### Overview of pivot tables (20 min)
* Discuss the purpose, importance, and structure of pivot tables
* Share how pivot tables are Excel's method for creating aggregates group by distinct column values
  * [pivot tables - split apply combine in Excel](https://www.safaribooksonline.com/library/view/learning-pandas/9781783985128/graphics/5128OS_09_01.jpg)
* Review Excel's pivot table capabilities and limitations

### Code-along: export data from a database using pgAdmin (10 min)

1. Extract data from the da_readychef schema
2. Work in pairs and explain the SQL code below to each other

```SQL
   Select e.dt, e.meal_id, event, type as meal_type, price as meal_price
   From da_readychef.events e
      Left Join da_readychef.meals m ON e.meal_id = m.meal_id
      -- Note: INNER JOIN would work if we are sure the meal_id column in da_readychef.meal contains primary keys
   Where TRUE
      And e.dt Between '2013-12-01' And '2013-12-31'
      And event = 'bought'
```

3. Run the query to extract data from the da_readychef schema
4. Export to a CSV file using a "|" delimiter example
5. Show that export preferences are set in pgAdmin by clicking ```File -> Preferences -> SQL Editor -> CSV Output```


### Code-along: create pivot tables in Excel (20 min)

1. Use the readychef table from the previous code-along to provide the data for this Excel code-along
2. Create a pivot table using the following steps 
3. Read the CSV file into an Excel spreadsheet tab
4. In Excel select the data table and give it a range name of readychef_meals
5. Create a pivot table that displays each date (as pivot table ROWS) and the total price of meals (as pivot table VALUE)
6. Modify the pivot table by adding meal type to the rows
7. Show the effect of moving the meal_type above and then below the date attribute in the ROWS pane
8. Position the meal_type above the date in the ROWS pane
9. Demonstrate how to change the aggregation type in the VALUES pane by demonstrating with meal price
10. Add an average price column to the VALUES pane

### !challenge

* type: paragraph
* id: b077b94d-e453-46f6-9ab6-270ef1386c45
* title: Create a pivot table

##### !question

### Exercise: create a pivot table that contains aggregates (25 min)

**Notes:**

In this exercise you will answer the question "What dates in early Fall of 2015 did people use bikes the longest?"

**Instructions**

1. Work in pairs
2. Extract data from the da_pronto.trip table
3. Run the query below to extract the date, from station name, from station id, to_station_id, gender, birthyear, and tripduration from the da_pronto.trip table

```
   Select date(starttime), from_station_name, from_station_id, to_station_id, gender, birthyear, tripduration
   From da_pronto.trip
   Where date(starttime) Between '2015-08-01' And '2015-10-31'
```  

4. Export to a CSV file
5. Create a pivot table with the following steps
6. Read the CSV file into an Excel spreadsheet tab
7. IN Excel select the data table and give it a range name
8. Create a pivot table that displays the date and sum and average trip duration for each of those dates
9. Determine which date has the longest average trip duration
10. Determine which from_stations had the longest rental times 
11. Modify the pivot table by adding the from_station_id *below* the date in the ROWS area
12. Move the from_station_id above the data attribute in the ROWS pane to group the pivot table by from_station_id and then date
13. Add a column of the minimum trip duration to the pivot table
14. Add a column of the maximum trip duration to the pivot table
15. Determine which station has the rental with the longest trip duration
16. Submit a GitHub link to your spreadsheet

Optional additional learning: play around with adding fields to various panes of the pivot table editor and see the changes that you make to the pivot table 
<br>

##### !end-question

##### !placeholder

Submit the link here:

##### !end-placeholder

### !end-challenge


### Code-along: improve user experience by formatting pivot tables (20 min)

1. Continue using the spreadsheet from the previous code-along
2. Demonstrate that pivot tables don't auto update
3. Demonstrate how to manually trigger an update
4. Format pivot tables to make them easier to interpret
5. Sort of columns in pivot tables (primary and secondary sorts) including a sort of trip duration
   * Note that the sort is a sort of the trip duration values within the grouping defined by the ROW field values
6. Add subtotals and grand totals
7. Add filters for a couple of dimensions in the pivot table
   * Add a filter for the meal type in the pivot table's FILTER area
   * Show that a filter can be either in the FILTERS area or in ROWS or COLUMNS, but not both
     * For an attribute in ROWS or COLUMNS, use the filter drop-down in the pivot table location
8. Show that row and column names, such a "Row Labels," can be manually changed to make it easier for the user to interpret 

### !challenge

* type: paragraph
* id: 75c9e17d-5cae-4605-9518-91d8d8a4acf2
* title: Format pivot tables

##### !question

### Exercise: make a pivot table more useful by improving the formatting (25 min)

1. Continue using the Pronto spreadsheet from the first challenge
2. Modify the pivot table by adding gender to the COLUMNS pane
3. Make the following changes to improve the user experience:
4. Sort by the sum of the duration decending
5. Add subtotals where you think that they're appropriate
6. Format the table; add more descriptive column headers
7. Add a filter for birthyear
8. Modify column names in the pivot table to make them easier to understand (if needed)
9. Submit a GitHub link to the spreadsheet

##### !end-question

##### !placeholder

Submit the link here:

##### !end-placeholder

### !end-challenge

## Solutions
* Example solutions to the exercises in this lesson above are available in [this spreadsheet](https://drive.google.com/uc?export=download&id=1o5tJpQQ6mcPWhNaNE4SR5El2FhWCTF9Y). These are intended for use after the exercises are completed.

### Resources
