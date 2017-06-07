# Functions

## Donutzz

To create a donut chart within R, please use my function by calling the following commands:
```
source_github <- function( url ) {
  # load package
  require(RCurl)
  
  # read script lines from website and evaluate
  script <- getURL(url, ssl.verifypeer = FALSE)
  eval(parse(text = script), envir=.GlobalEnv)
} 

source_github("https://raw.githubusercontent.com/icps86/Functions/master/donutzz.R")
```
Now the function `donutzz` is available in your global environment for use! 

Here is an example of how to use it:
```
# Create a vector of numeric values
xval <- c(10, 20, 40, 80, 100)
# Create a factor vector of labels corresponding to each numeric value
xnames <- as.factor( c("H", "E", "L", "X", "O") )
# Create the donut chart
first.donut.chart <- donutzz( x = xval, lev = xnames, main = "Place Title Here" )
# Display the donut chart
first.donut.chart
```
