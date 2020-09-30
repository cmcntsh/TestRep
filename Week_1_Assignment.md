Getting Started
===============

#### What is your name?

Type your name here:

Introduction:
-------------

If you’re reading this you have successfully installed R and RStudio.
Good job!

This assignment is written as an Rmarkdown file and can be used to
generate formatted output. You can try it out now by clicking the
Preview (or Knit) button at the top of this window. Some of the output
will look better in the popup window than it will when you run the code
blocks here. It might be helpful to generate that window by hitting the
button again as you work through some of the steps of this assignment.

One of the advantages of this output is it includes the code with the
output. If you ever need to recreate an analysis in the future, it’s
probably more important to have a record of the code used than the
actual output. (Always save your code with your data file(s).)

Directions:
-----------

Complete each step of the assignment below.

Install/Load needed packages
----------------------------

Run the following code block to install the R packages needed for this
assignment and load them into memory. (This may take a few minutes if
you haven’t installed the packages before. If you get any errors or
warnings, try running the block another time.)

``` r
# List the packages needed
packages <- c("tidyverse", "rio")

# Check if each package is installed already. If not, install the package.
for (i in packages){
  if(! i %in% installed.packages()){
    install.packages(i,dependencies = TRUE)
  }
  # Show each package that is checked.
  print(i)
  
  # Load each package into memory so we can use it.
  library(i,character.only=TRUE)
}
```

    ## [1] "tidyverse"

    ## -- Attaching packages ----------------------------------------------------------------------------------------- tidyverse 1.3.0 --

    ## v ggplot2 3.3.1     v purrr   0.3.4
    ## v tibble  3.0.1     v dplyr   1.0.0
    ## v tidyr   1.1.0     v stringr 1.4.0
    ## v readr   1.3.1     v forcats 0.5.0

    ## -- Conflicts -------------------------------------------------------------------------------------------- tidyverse_conflicts() --
    ## x dplyr::filter() masks stats::filter()
    ## x dplyr::lag()    masks stats::lag()

    ## [1] "rio"

Open a csv data file
--------------------

CSV files can be opened using the menus in RStudio or by executing code.
Open your data file by using the menu (File - Import Dataset) or
executing the code block below to open the Week1.csv file. If you use
the menus, make sure to select From Text (readr)… We will use Tidyverse
packages as much as possible in this class. The readr package is a
Tidyverse package. The rio packages tries to make data import and export
simple. The following code block uses the rio import() function. When
you open the dataset, notice that a new Data object appears in the
Environment pane in the top right window of RStudio. (If the Environment
pane isn’t showing, click on the Environment tab.) You can see the
variables in the dataset by clicking on the circle with the triangle in
it next to the name of the data object. You can see the data in a
spreadsheet like window by clicking on the name of the data object.
Click on the tab with this assignment to come back to it after looking
at the dataset pane. Try both of them out.

``` r
# https://cran.r-project.org/web/packages/rio/vignettes/rio.html
library(rio)
csvdataset <- rio::import(file.choose())
```

Open an Excel workbook
----------------------

Excel files can be opened using the menus in RStudio or by executing
code. Open your data file by using the menu (File - Import Dataset) or
executing the code block below to open the Week1.xlsx file. The rio
packages tries to make data import and export simple. The following code
block uses the rio import() function. When you open the dataset, notice
that a new Data object appears in the Environment pane in the top right
window of RStudio. (If the Environment pane isn’t showing, click on the
Environment tab.) You can see the variables in the dataset by clicking
on the circle with the triangle in it next to the name of the data
object. You can see the data in a spreadsheet like window by clicking on
the name of the data object. Click on the tab with this assignment to
come back to it after looking at the dataset pane. Try both of them out.

``` r
# https://cran.r-project.org/web/packages/rio/vignettes/rio.html
library(rio)
xlsdataset <- rio::import(file.choose())
```

Open an SPSS data file (.sav file)
----------------------------------

SPSS data files can be opened using the menus in RStudio or by executing
code. Open your data file by using the menu (File - Import Dataset) or
executing the code block below to open the Week1.xlsx file. The rio
packages tries to make data import and export simple. The following code
block uses the rio import() function. When you open the dataset, notice
that a new Data object appears in the Environment pane in the top right
window of RStudio. (If the Environment pane isn’t showing, click on the
Environment tab.) You can see the variables in the dataset by clicking
on the circle with the triangle in it next to the name of the data
object. You can see the data in a spreadsheet like window by clicking on
the name of the data object. Click on the tab with this assignment to
come back to it after looking at the dataset pane. Try both of them out.

``` r
# https://cran.r-project.org/web/packages/rio/vignettes/rio.html
library(rio)
savdataset <- rio::import(file.choose())
```

Feedback
--------

#### What did you think of this assignment?

Answer:

#### What would you change?

Answer:

Save your output.
-----------------

Save this assignment as an html file by following these steps:

1.  Click the preview or knit button at the top of this window.
    -   RStudio will execute each block of code and save the results to
        create the output. You may need to select each file like you did
        when you ran the code blocks one at a time.
    -   A popup should appear with all the output for the assignment.
    -   Or a page should appear in the Viewer pane in the bottom right
        corner of RStudio.
    -   If the button said knit, a new html file should appear in the
        same folder as your .Rmd file with the same name. you can submit
        that file for your assignment.(You can check that by clicking on
        the Files tab to see if a new html file is in the folder. Click
        on the Viewer tab to go back to the output viewer.)
    -   If the button said Preview, you probably need to continue on to
        the next steps.
2.  Click the Open in Browser button or Show in New Window button at the
    top of that window.
    -   Your output should open up in your web browser.
3.  Save the page in the web browser.
    -   Usually you can right click and select save as…
    -   Or select save as from the browser menu

Submit your assignment.
-----------------------

Submit the output you just saved for your assignment.
