# Kickstart My Chart

## Project goal & actions

This project is trying to uncover some market trends. Using the Excel table provided, I modified and analyzed the data of 4,000 past Kickstarter projects attempting to figure out market trends.

### Background

Over $2 billion has been raised using the massively successful crowdfunding service, Kickstarter, but not every project has found success. Of the more than 300,000 projects launched on Kickstarter, only a third have made it through the funding process with a positive outcome.

Getting funded on Kickstarter requires meeting or exceeding the project's initial goal, so many organizations spend months looking through past projects in an attempt to discover some trick for finding success. For this week's homework, you will organize and analyze a database of 4,000 past projects in order to uncover any hidden trends.

### Working with the data

The modification on the Excel file ocurred as follows:

1- I filled each cell in the `state` column with a different color, depending on whether the associated campaign was successful, failed, or canceled, or is currently live.

2- I created a new column O called `Percent Funded` that uses a formula to uncover how much money a campaign made to reach its initial goal.

3- I used conditional formatting to fill each cell in the `Percent Funded` column using a three-color scale. The scale started at 0 being a dark shade of red, transitioning to green at 100, and blue at 200.

4- I created a new column P called `Average Donation` that uses a formula to uncover how much each backer for the project paid on average.

5- I created two new columns, one called `Category` at Q and another called `Sub-Category` at R, which use formulas to split the `Category and Sub-Category` column into two parts.

### Final Table
![Kickstarter Table](Images/FullTable.PNG)


6- I created a new sheet with a pivot table that analyzes the initial worksheet to count how many campaigns were successful, failed, canceled, or are currently live per **category**.

7- I created a stacked column pivot chart that can be filtered by country based on the new table created.

### Final Table
  ![Category Stats](Images/CategoryStats.PNG)

8- I created a new sheet with a pivot table that analyzes the initial sheet to count how many campaigns were successful, failed, or canceled, or are currently live per **sub-category**.

9- I created a stacked column pivot chart that can be filtered by country and parent-category based on the table I created.

### Final Table
  ![Subcategory Stats](Images/SubcategoryStats.PNG)


10- I created a new column named `Date Created Conversion` that uses [this formula](https://www.extendoffice.com/documents/excel/2473-excel-timestamp-to-date.html) to convert the data contained within `launched_at` into Excel's date format.

11- I created a new column named `Date Ended Conversion` that uses [this formula](https://www.extendoffice.com/documents/excel/2473-excel-timestamp-to-date.html) to convert the data contained within `deadline` into Excel's date format.

Note: Since the dates stored within the `deadline` and `launched_at` columns use Unix timestamps, I used a formula to convert these timestamps to a normal date. (https://www.extendoffice.com/documents/excel/2473-excel-timestamp-to-date.html)

12- I created a new sheet with a pivot table with a column of `state`, rows of `Date Created Conversion`, values based on the count of `state`, and filters based on `parent category` and `Years`.

13- Finallly, I created a pivot chart line graph that visualizes this new table.

### Final Table
   ![Outcomes Based on Launch Date](Images/LaunchDateOutcomes.PNG)

14- I created a report in Microsoft Word and answered the following questions:

	- What are three conclusions we can draw about Kickstarter campaigns?
	- What are some limitations of this dataset?
	- What are some other possible tables and/or graphs that we could create?

## Beyond first analisys

1- I created a new sheet with 8 columns:

  	* `Goal`	* `Number Successful`	* `Number Failed`	* `Number Canceled`	* `Total Projects`
  	* `Percentage Successful`	* `Percentage Failed`	* `Percentage Canceled`

2- In the `Goal` column, I created 12 rows with the following headers:

  * Less than 1000
  * 1000 to 4999
  * 5000 to 9999
  * 10000 to 14999
  * 15000 to 19999
  * 20000 to 24999
  * 25000 to 29999
  * 30000 to 34999
  * 35000 to 39999
  * 40000 to 44999
  * 45000 to 49999
  * Greater than or equal to 50000

3- Using the `COUNTIFS()` formula, I counted how many successful, failed, and canceled projects were created with goals within the ranges listed above. Then, I populated the `Number Successful`, `Number Failed`, and `Number Canceled` columns with this data.

2- I added up each of the values in the `Number Successful`, `Number Failed`, and `Number Canceled` columns to populate the `Total Projects` column. Then, using a mathematical formula, I found the percentage of projects that were successful, failed, or canceled per goal range.

4- I create a line chart that graphs the relationship between a goal's amount and its chances at success, failure, or cancellation.

### Table Table  
![Goal Outcomes](Images/GoalOutcomes.PNG)


## Statistical Analysis

In this part of the project I evaluated the number of backers of successful and unsuccessful campaigns by creating "my own" summary statistics table.

1- I created a new worksheet, and created a column each for the number of backers of successful campaigns and unsuccessful campaigns. Then I evaluated the following for successful campaigns, and then for unsuccessful campaigns:

  * The mean number of backers.
  * The median number of backers.
  * The minimum number of backers.
  * The maximum number of backers.
  * The variance of the number of backers.
  * The standard deviation of the number of backers.

