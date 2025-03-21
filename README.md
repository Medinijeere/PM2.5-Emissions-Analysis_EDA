# PM2.5-Emissions-Analysis_EDA
Exploratory-Data-Analysis-Project on ExData

The data for this assignment are available from the course web site as a single zip file:

Data for Peer Assessment
 [29Mb]

The zip file contains two files:

PM2.5 Emissions Data (
summarySCC_PM25.rds
summarySCC_PM25.rds): This file contains a data frame with all of the PM2.5 emissions data for 1999, 2002, 2005, and 2008. For each year, the table contains number of tons of PM2.5 emitted from a specific type of source for the entire year. Here are the first few rows.
##     fips      SCC Pollutant Emissions  type year
## 4  09001 10100401  PM25-PRI    15.714 POINT 1999
## 8  09001 10100404  PM25-PRI   234.178 POINT 1999
## 12 09001 10100501  PM25-PRI     0.128 POINT 1999
## 16 09001 10200401  PM25-PRI     2.036 POINT 1999
## 20 09001 10200504  PM25-PRI     0.388 POINT 1999
## 24 09001 10200602  PM25-PRI     1.490 POINT 1999

fips
fips: A five-digit number (represented as a string) indicating the U.S. county

SCC
SCC: The name of the source as indicated by a digit string (see source code classification table)

Pollutant
Pollutant: A string indicating the pollutant

Emissions
Emissions: Amount of PM2.5 emitted, in tons

type
type: The type of source (point, non-point, on-road, or non-road)

year
year: The year of emissions recorded

Source Classification Code Table (
Source_Classification_Code.rds
Source_Classification_Code.rds): This table provides a mapping from the SCC digit strings in the Emissions table to the actual name of the PM2.5 source. The sources are categorized in a few different ways from more general to more specific and you may choose to explore whatever categories you think are most useful. For example, source “10100101” is known as “Ext Comb /Electric Gen /Anthracite Coal /Pulverized Coal”.

You can read each of the two files using the 
readRDS()
readRDS() function in R. For example, reading in each file can be done with the following code:
## This first line will likely take a few seconds. Be patient!
NEI <- readRDS("summarySCC_PM25.rds")
SCC <- readRDS("Source_Classification_Code.rds")

as long as each of those files is in your current working directory (check by calling 
dir() and see if those files are in the listing).
