# KickStart My Chart

## Background

Over two billion dollars have been raised using the massively successful crowdfunding service, Kickstarter, but not every project has found success. Of the over 300,000 projects launched on Kickstarter, only a third have made it through the funding process with a positive outcome.

Since getting funded on Kickstarter requires meeting or exceeding the project's initial goal, many organizations spend months looking through past projects in an attempt to discover some trick to finding success. For this week's homework, you will organize and analyze a database of four thousand past projects in order to uncover any hidden trends.

![Kickstarter Table](Images/FullTable.PNG)

* Using the Excel table provided, we modified and analyzed the data of four thousand past Kickstarter projects as you attempt to uncover some of the market trends.

* Used conditional formatting to fill each cell in the `state` column with a different color, depending on whether the associated campaign was "successful," "failed," "cancelled," or is currently "live".

* Created a new column at column O called `percent funded` that uses a formula to uncover how much money a campaign made towards reaching its initial goal.

  * Used conditional formatting to fill each cell in the `percent funded` column using a three-color scale. The scale should start at 0 and be a dark shade of red, transitioning to green at 100, and then moving towards blue at 200.

* Created a new column at column P called `average donation` that uses a formula to uncover how much each backer for the project paid on average.

* Created two new columns, one called `category` at Q and another called `sub-category` at R, which use formulas to split the `Category and Sub-Category` column into two parts.

  ![Category Stats](Images/CategoryStats.PNG)

  * Created a new sheet with a pivot table that analyzed the initial worksheet to count how many campaigns were "successful," "failed," "cancelled," or are currently "live" per **category**.

    * Created a stacked column pivot chart that can be filtered by `country` based on the table created.

  ![Subcategory Stats](Images/SubcategoryStats.PNG)

  * Created a new sheet with a pivot table that will analyze the initial sheet to count how many campaigns were "successful," "failed," "cancelled," or are currently "live" per **sub-category**.

    * Created a stacked column pivot chart that can be filtered by `country` and `parent-category` based on the table you have created.

* The dates stored within the `deadline` and `launched_at` columns are using unix timestamps. Fortunately for us, [there is a formula](http://spreadsheetpage.com/index.php/tip/converting_unix_timestamps/) out there that can be used to convert these timestamps into a normal date.

  * Created a new column named `Date Created Conversion` that will use [this formula](http://spreadsheetpage.com/index.php/tip/converting_unix_timestamps/) to convert the data contained within `launched_at` into Excel's Date format

  * Created a new column named `Date Ended Conversion` that will use [this formula](http://spreadsheetpage.com/index.php/tip/converting_unix_timestamps/) to convert the data contained within `deadline` into Excel's Date format

  ![Outcomes Based on Launch Date](Images/LaunchDateOutcomes.PNG)

  * Created a new sheet with a pivot table with a column of `state`, rows of `Date Created Conversion`, values based on the count of `state`, and filters based on `parent category` and `Years`.

  * Then created a pivot chart line graph that visualizes this new table.

* Created a report in Microsoft Word and answer the following questions...

1. What are three conclusions we can make about Kickstarter campaigns given the provided data?
2. What are some of the limitations of this dataset?
3. What are some other possible tables/graphs that we could create?


* Created a new sheet with 8 columns: `Goal`, `Number Successful`, `Number Failed`, `Number Canceled`, `Total Projects`, `Percentage Successful`, `Percentage Failed`, and `Percentage Canceled`

  * In the `goal` column, create twelve rows with the following headers...

    * Less Than 1000
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

    ![Goal Outcomes](Images/GoalOutcomes.PNG)

  * Used the `COUNTIFS()` formula to find, count how many successful, failed, and canceled projects were created with goals within those ranges listed above. Populated the `Number Successful`, `Number Failed`, and `Number Canceled` columns with this data.

  * Added up each of the values in the `Number Successful`, `Number Failed`, and `Number Canceled` columns to populate the `Total Projects` column. Then, using a mathematic formulae, found the percentage of projects which were successful, failed, or were canceled per goal range.

  * Create a line chart which graphs the relationship between a goal's amount and its chances at success, failure, or cancellation.
