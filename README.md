## Excel-challenge
### Background
Over $2 billion has been raised using the massively successful crowdfunding service, Kickstarter, but not every project has found success. Of the more than 300,000 projects launched on Kickstarter, only a third have made it through the funding process with a positive outcome.
Getting funded on Kickstarter requires meeting or exceeding the project's initial goal, so many organizations spend months looking through past projects in an attempt to discover some trick for finding success. For this week's project, you will organize and analyze a database of 4,000 past projects in order to uncover any hidden trends.
### Steps
The provided Excel table was used to modify and analyze the data of 4,000 past Kickstarter projects for uncovering some market trends.
* Conditional formatting was used to fill each cell in the `state` column with a different color, depending on whether the associated campaign was successful, failed, or canceled, or is currently live.
  * A new column O called `Percent Funded` was created that uses a formula to uncover how much money a campaign made to reach its initial goal.
* Conditional formatting was used to fill each cell in the `Percent Funded` column using a three-color scale. The scale starts at 0 and is a dark shade of red, transitioning to green at 100, and blue at 200.
  * A new column P called `Average Donation` was created that uses a formula to uncover how much each backer for the project paid on average.
  * Two new columns were created, one called `Category` at Q and another called `Sub-Category` at R, which use formulas to split the `Category and Sub-Category` column into two parts.
  ![Category Stats](https://github.com/changrita1114/Excel-challenge/blob/master/images/05_Pivot_Table_1.png?raw=true)
  * A new sheet was created with a pivot table that analyzed the initial worksheet to count how many campaigns were successful, failed, canceled, or are currently live per **category**.
  * A stacked column pivot chart was plotted that can be filtered by country based on the table you have created.
  ![Subcategory Stats](https://github.com/changrita1114/Excel-challenge/blob/master/images/06_Pivot_Table_2.png?raw=true)
  * A new sheet with a pivot table was created that analyzed the initial sheet to count how many campaigns were successful, failed, or canceled, or are currently live per **sub-category**.
  * A stacked column pivot chart was plotted that could be filtered by country and parent-category based on the table you have created.
* The dates stored within the `deadline` and `launched_at` columns use Unix timestamps.
  * A new column named `Date Created Conversion` was created that used [a formula](https://www.extendoffice.com/documents/excel/2473-excel-timestamp-to-date.html) to convert the data contained within `launched_at` into Excel's date format.
  * A new column named `Date Ended Conversion` was created that used [a formula](https://www.extendoffice.com/documents/excel/2473-excel-timestamp-to-date.html) to convert the data contained within `deadline` into Excel's date format.
  ![Outcomes Based on Launch Date](https://github.com/changrita1114/Excel-challenge/blob/master/images/07_Pivot_Table_3.png?raw=true)
  * Create a new sheet with a pivot table with a column of `state`, rows of `Date Created Conversion`, values based on the count of `state`, and filters based on `parent category` and `Years`.
  * A pivot chart line graph was plotted that visualized the new table.
* A report in a [PDF](https://github.com/changrita1114/Excel-challenge/blob/master/analysis_results.pdf) was generated to answer the following questions.
1. Given the provided data, what are three conclusions we can draw about Kickstarter campaigns?
2. What are some limitations of this dataset?
3. What are some other possible tables and/or graphs that we could create?

### Further Analysis
* Create a new sheet with 8 columns:
  * `Goal`
  * `Number Successful`
  * `Number Failed`
  * `Number Canceled`
  * `Total Projects`
  * `Percentage Successful`
  * `Percentage Failed`
  * `Percentage Canceled`
* In the `Goal` column, created 12 rows with the following headers:
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
  ![Goal Outcomes](https://github.com/changrita1114/Excel-challenge/blob/master/images/08_Excel_Bonus.png?raw=true)
* The `COUNTIFS()` formula was used to count how many successful, failed, and canceled projects were created with goals within the ranges listed above. The `Number Successful`, `Number Failed`, and `Number Canceled` columns with this data were populated.
* Each of the values in the `Number Successful`, `Number Failed`, and `Number Canceled` columns to populate the `Total Projects` column were added up. Then, a mathematical formula was used to find the percentage of projects that were successful, failed, or canceled per goal range.
* A line chart was created that graphs the relationship between a goal's amount and its chances at success, failure, or cancellation.
### Statistical Analysis
If one were to describe a successful crowdfunding campaign, most people would use the number of campaign backers as a metric of success. One of the most efficient ways that data scientists characterize a quantitative metric, such as the number of campaign backers, is by creating a summary statistics table.
* A new worksheet was created in the workbook, and a column each for the number of backers of successful campaigns and unsuccessful campaigns was created.
  ![Images/backers01.png](https://github.com/changrita1114/Excel-challenge/blob/master/images/09_Excel_Bonus_2.png?raw=true)
* The following variables were evaluated using Excel for successful campaigns, and then for unsuccessful campaigns were calculated:
  * The mean number of backers.
  * The median number of backers.
  * The minimum number of backers.
  * The maximum number of backers.
  * The variance of the number of backers.
  * The standard deviation of the number of backers.
## Disclaimer
The resources of this master branch are only for educational purposes. All reserved rights belong to UCSD Data Science and Visualization Boot Camp.
