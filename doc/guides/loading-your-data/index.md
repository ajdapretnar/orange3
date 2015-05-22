Loading your Data
=================

Orange comes with its own its own data format\<tab-delimited\>, but can
also handle standard comma or tab delimited data files. The input data
set would usually be a table, with data instances (samples) in rows and
data attributes in columns. Data attributes can be of different types
(continuous, discrete, and strings) and kinds (input variables, meta
attributes, and a class). Data attribute type and kind can be provided
in the data table header and can be changed later, after reading the
data, with several specialized widgets, like Select Attributes.

In a Nutshell
-------------

-   Orange can import any comma or tab-delimited data file. Use File
    widget and then, if needed, select class and meta attributes in
    Select Attributes widget.
-   To specify the domain and the type of the attribute, attribute names
    can be preceded with a label followed by a hash. Use c for a class
    and m for meta attribute, i to ignore a column, and C, D, S to
    continuous, discrete and string attribute type. Examples: C\#mpg,
    mS\#name, i\#dummy. Make sure to set **Import Options** in File
    widget and set the header to **Orange simplified header**.
-   Orange’s native format is a tab-delimited text file with three
    header rows. The first row contains attribute names, the second the
    domain (**continuous**, **discrete** or **string**), and the third
    optional type (**class**, **meta** or **string**).

Data from Excel
---------------

Say we have the data (sample.xlsx \<sample.xlsx\>) in some popular
spreadsheet application, like Excel:

![image][]

To move this data to Orange, we need to save the file in a tab or comma
separated format. In Excel, we can use a **Save As …** command from the
**File** menu:

![image][1]

and select **Comma Separated Values (.csv)** as an output format:

![image][2]

We can now save the data in, say, a file named
sample.csv \<sample.csv\>.

To load the data set in Orange, we can design a simple workflow with
File and Data Table widget,

![image][3]

open the File widget (double click on its icon) and click on the file
browser icon,

![image][4]

change the file type selector to csv,

![image][5]

locate the data file sample.csv which we have saved from Excel and open
it. The **File** widget should now look something like this:

![image][6]

Notice that our data contains 8 data instances (rows) and 7 data
attributes (columns). We can explore the contents of this data set in
the Data Table widget (double click its icon to open it):

![image][7]

Question marks in the data table denote missing data entries. These
entries correspond to empty cells in the Excel table. Rows in

  [image]: spreadsheet.png
  [1]: save-as.png
  [2]: save-as-csv.png
  [3]: file-data-table-workflow.png
  [4]: file-browser-icon.png
  [5]: csv-selector.png
  [6]: file-widget.png
  [7]: data-table-widget.png
