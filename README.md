# Kickstarting with Excel

## Overview of Project

### Purpose
This project was meant to show how the "plays" subcategory fared in relation to the launch date and the funding goal. From there, visualizations were created to help visually display the 
calculations that were made.

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date
This analysis was performed by going to the main Kickstarter sheet and creating a table using all the data on the sheet. The sheet was renamed "Theater Outcomes by Launch Date" to properly discribe what was on the sheet. A pivot table was created using "Parent Category" and "Years" as filters, "Outcomes" as columns, "Date Created Conversion" as rows, and Count of "Outcomes" as the value being display for each row. I removed the "live" outcomes from the column labels. Using the "Parent Category" filter, theater was selected. A line chart was created to visualize the date display in the pivot table. Below is a picture of the chart that was created:
![](/Resources/Theater_Outcomes_vs_Launch.png)

### Analysis of Outcomes Based on Goals
For this anaylsis, to start, a new workbook was created and labeled "Outcomes Based on Goals". The following columns were created: Goal, Number Successful, Number Failed, Number Canceled, Total Projects, Percentage Successful, Percentage Failed, and Percentage Canceled. In the Goal column, starting with less than 1000 and continuing to 1000 to 4999 all the way to greater that 50000 as the dollar ranges to check against for the number columns. In the Number columns, the number of successful, failed, and canceled shows for each dollar range was calculated using COUNTIFS() functions. The COUNTIFS() were populated by filtering the Kickstarter "outcome" column, on the "goal" amount column using the dollar range created earlier, and using "plays" from the "Subcategory" column as the criteria. The Total projects was calculated by adding the three number columns together. The percentage columns for populated by dividing the number for each outcome by the total project and doing that for each dollar range. A line chart was created to visualize the relationship between goal-amount ranges and the percentage of successful, failed, or canceled projects. Below is a picture of the chart that was created:
![](/Resources/Outcomes_vs_Goals.png)

### Challenges and Difficulties Encountered
It was difficult to understand the COUNTIFS() functions at first, trying to understand what order everything goes in but once I took my time and looked at some documentation, it was easier to understand.

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?
One conclusion is that May and June are the peak months for theater shows. The other conclusion is the amount of canceled shows is less than 10 and it peaks in January.

- What can you conclude about the Outcomes based on Goals?
There are no canceled plays for the dollar ranges that were being filtered on.

- What are some limitations of this dataset?
One of the limitations as using on on Parent Catergory or Subcategory. If a better overview of this was wanted. The dollar range is another limitations if there is the possibility that a different Subcategory is used and is has a larger dollar range that could be broken down.

- What are some other possible tables and/or graphs that we could create?
A cluster column chart for be used on both datasets. A pie graph can be used on the Outcomes vs Goals sheet as well as a box and whisker chart.
