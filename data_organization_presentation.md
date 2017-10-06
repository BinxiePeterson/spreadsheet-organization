Data organization in spreadsheets
========================================================
author: Bianca Peterson
date: 24 October 2017
autosize: false

<div class="midcenter" style="margin-left:200px; margin-top:100px; background-color:transparent; border:0px; box-shadow:none;">
<img src="img/dc_nwu_logo.png"></img>
</div>

Data Organization in Spreadsheets
========================================================

This presentation is based on the [Data Carpentry Spreadsheet Ecology Lesson](http://www.datacarpentry.org/spreadsheet-ecology-lesson/)

Introduction
========================================================

- Good data organization is the foundation of any research project
- Structure data the way that computers need it
- Much of your time will be spent in this 'data wrangling' stage

In this lesson, you will learn:
========================================================

- Good data entry practices - formatting data tables in spreadsheets
- How to avoid common formatting mistakes
- Approaches for handling dates in spreadsheets
- Basic quality control and data manipulation in spreadsheets
- Exporting data from spreadsheets

Questions
========================================================

- How many people have used spreadsheets in their research?
- What kind of operations do you do in spreadsheets? 
- Which ones do you think spreadsheets are good for?
- How many people have accidentally done something that made them frustrated or sad?

We can use spreadsheets for:
========================================================

- Data entry
- Organizing data
- Subsetting and sorting data
- Statistics
- Plotting

Problems with spreadsheets:
========================================================

- Generating tables for publications in a spreadsheet is not optimal
- The graphical, drag and drop nature of spreadsheet programs makes it very difficult, if not impossible, to replicate your steps - When doing calculations in a spreadsheet, it's easy to accidentally apply a slightly different formula to multiple adjacent cells

Using spreadsheets for data entry and cleaning
========================================================

- Clean data prior to importation into a statistical analysis program
- Check your data quality
- Produce preliminary summary statistics

Formatting data tables in spreadsheets
========================================================

- Most common mistake: rely on context, notes in the margin, spatial layout of data and fields to convey information
- Humans can (usually) interpret these things, but computers don't view information the same way
- We have to set up our data for the computer to understand it in order to analyze it fast and efficiently

Keeping track of your analyses
========================================================

- Don't modify original dataset
- Create a new file/tab with cleaned/analyzed data
- Keep track of steps used for data cleaning/analysis

Structuring data in spreadsheets
========================================================

- Put all variables in columns
- Put each observation in its own row
- Don't combine multiple pieces of information in one cell
- Leave raw data raw - don't change it!
- Export cleaned data to text-based format (CSV) - anyone can use the data and it is required by most data repositories

Survey of small mammals in a desert ecosystem
========================================================

<div class="midcenter" style="margin-left:10px; margin-top:100px;">
<img src="img/Figure1.png"></img>
</div>
***
- Variables: species, plot, weight, sex and date collected
- Problem: species and sex in the same field
- Thus not able to look at a single species or look at different weight distributions by sex

Let's look at a messy version of the data
========================================================

Download the data from FigShare: https://ndownloader.figshare.com/files/2252083 
- Two tabs: 2 field assistants conducted surveys, one in 2013 and one in 2014
- Identify what is wrong with this spreadsheet
- Discuss the steps you would need to take to clean up the data and put them all together in one spreadhseet

Common spreadsheet errors: using multiple tables
========================================================

<div class="midcenter" style="margin-left:10px; margin-top:50px;">
<img src="img/Figure2.png"></img>
</div>
***

- This confuses the computer
- You're drawing false associations between things for the computer, which sees each row as an observation
- You're potentially using the same field name in muliplte places, which makes it harder to clean the data up into a usable form

Common spreadsheet errors: using multiple tabs
========================================================

- The computer will not be able to see connections in the data
- You are more likely to accidentally add inconsistencies to your data when recording data in a new tab everytime
- This will add an extra step for yourself, because data will need to be combined before analyzing it
- Ask yourself: Can I avoid adding a new tab by adding another column to the original spreadsheet?
- The data sheet may get very long - freeze column headers so that they remain visible

Common spreadsheet errors: not filling in zeros
========================================================

- There's a difference between a zero and a blank cell
- Zero = actual data | blank cell = no measurement
- Missing/null/unknown values can cause problems with subsequent calculations or analyses

Common spreadsheet errors: using problematic null values
========================================================

<div class="midcenter" style="margin-left:10px; margin-top:50px;">
<img src="img/Figure3.png"></img>
</div>
***

<div class="midcenter" style="margin-top:50px;">Article: Nine simple ways to make it easier to (re)use your data by White et al., 2013 https://peerj.com/preprints/7/
</div>

Common spreadsheet errors: using formatting to convey information
========================================================

<div class="midcenter" style="margin-left:100px; margin-top:50px;">
<img src="img/Figure4.png"></img>
</div>
***
<div class="midcenter" style="margin-right:100px; margin-top:50px;">
<img src="img/Figure5.png"></img>
</div>

Common spreadsheet errors: using formatting to make the data sheet look pretty
========================================================

- Example: merging cells
- Solution: restructure your data in such a way that you will not need to merge cells to organize your data

Common spreadsheet errors: placing comments or units in cells
========================================================

- Solution: create another field to add notes or units to cells

Common spreadsheet errors: entering more than one piece of information in a cell
========================================================

- Solution: create another column to record all the information you need

Common spreadsheet errors: using problematic field names
========================================================

<div class="midcenter" style="margin-left:80px; margin-top:50px;">
<img src="img/Figure6.png"></img>
</div>

Common spreadsheet errors: using problematic field names
========================================================

- Solution: choose descriptive field names; do not include spaces, numbers, or special characters of any kind
- Spaces can be misinterpreted by parsers that use whitespace as delimiters 
- Some programs don't like field names that are text strings that start with numbers
- Underscores (_) are a good alternative to spaces
- Consider writing names in camel case (like this: ExampleFileName) to improve readability

Common spreadsheet errors: using special characters in data
========================================================

- Example: line breaks when writing longer text in a cell; when copying data in from other applications such as Word; using fancy non-standard characters (such as left- and right-aligned quotation marks)
- Solution: avoid adding characters such as newlines, tabs, and vertical tabs; only use text and spaces

Common spreadsheet errors: inclusion of metadata in data table
========================================================

- Example: adding legends to the top or bottom of your data table to explain column meaning, units, exceptions, etc.
- Solution: recording data about your data ("metadata") is essential, but should not be contained in the data file itself
- Your future self and other people may want to examine or use your data to understand your findings, verify your findings, review your submitted publication, replicate your results, design a similar study, or archive your data for access and re-use
- Store metadata as a separate plain text file in the same directory as your data file

Dates as data
========================================================

- Not best practice to store dates in a single column
- Exercise: extract month, day and year from the dates tab of your spreadsheet to new columns
- Use the funtions MONTH(), DAY() and YEAR()
- Make sure the new column is formatted as a number and not as a date
- What do you see?

Dates as data
========================================================

(According to your computer's settings...)

- NOW() - returns the current date and time
- TODAY() - returns the current date
- NOW()-TODAY() - returns the current time in a decimal value
- HOUR(), MINUTE() and SECOND() will extract the respective time units

Preferred date format
========================================================

- Store MONTH, DAY and YEAR in separate columns
- Excel is unable to parse dates from before 1899-12-31 (referred to as the 1900 date system) - be careful if you're working with historical data
- Alternatively, Excel may use the 1904 date system where a different serial number is assigned
- Be careful when exporting data from Excel - dates may be ~4 years off!

Date formats in spreadsheets
========================================================

![alt text](img/Figure7.png)

Integers (numbers) - it counts the days from a default of December 31, 1899 (beware, defaults differ for different versions of Excel)

Date formats in spreadsheets
========================================================
incremental: true

- Exercise: save the currently active sheet as a CSV (comma delimited) (.csv) file and open it with a plain text editor
- What do you see?
- Now open the file with Excel again
- What do you see?
- As you can see, exporting data from Excel and then importing it back into Excel fundamentally changed the data!

Quality assurance/control
========================================================

- Quality assurance versus Quality control
- Quality assurance = techniques implemented prior to entering data
- Quality control = techniques used after entering data to check for errors

Quality assurance
========================================================

Only allow valid values during data entry by using Data Validation (Excel) or Validity (Libre Office)

![alt text](img/Figure8.png)

Quality assurance
========================================================
incremental: true

- Exercise: set the plot column to only allow plot values that are integers between 1 and 24
- Now try to enter a new value in the plot column that isn't valid
- Make a dropdown list for species names

Quality control: Sorting
========================================================

Download the semi-cleaned data file: https://figshare.com/articles/survey_data_messy_quality_control/4830016
- Sorting - bad values often sort to the bottom or top of the column (sort data by each field, one at a time)
- On the Data tab, click on the AZ sort button
- Remember to expand your sort to prevent data corruption, i.e. all the data in one row should move together

Quality control: Conditional formatting
========================================================

- Conditional formatting - color code values by some criteria or lowest to highest
- This makes it easy to scan your data for outliers
- In the main Excel menu bar, click Format > Conditional Formatting... > +
- Apply a 2-Color-Scale formatting rule to the Weight_grams column, with lowest values set to orange and highest values set to yellow
- What do you see?

Exporting data
========================================================

Storing data in Excel default file format (*.xls or *.xlsx) isn't a good idea, because...
- It's proprietry format - in future it might become inconvenient/impossible to open the file
- Other spreadsheet software may not be able to open files in this format
- Different versions of Excel may handle data differently, leading to inconsistencies
- More journals and grant agencies are requiring data to be deposited in a data repository, and most of them don't accept Excel format
- Use tabs as delimiter (.tsv file) when the data contains commas

Key points
========================================================

- Good data organization is the foundation of any research project
- Never modify your raw data - always make a copy before making any changes
- Keep track of all the steps you take to clean your data
- Organize your data according to tidy data principles
- Have a look at Hadley Wickhams' manuscript about Tidy Data: https://www.jstatsoft.org/article/view/v059i10 
