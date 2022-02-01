# Introduction to Data Science Coursera
> Here lies my assignments for course [_Introduction to Data Science in Python_](https://www.coursera.org/learn/python-data-analysis).
> There were 3 assignments based on using Python and its libraries for Data Science.
> Numeration of assignments responds to numeration on Coursera.


## Table of Contents
* [Assignment 2](#assignment-2)
* [Assignment 3](#assignment-3)
* [Assignment 4](#assignment-4)
* [List of used libraries](#list-of-used-libraries)


## Assignment 2
This assignment is called ***Pandas introduction*** and is divided in 2 parts.

### Part 1
Code for part 1 of this assignment loads the olympics dataset [`olympics.csv`](https://github.com/Cybersheralt/Introduction-to-DS-Coursera/blob/main/Assignment%202/olympics.csv), which was derrived from the Wikipedia entry on [All Time Olympic Games Medals](https://en.wikipedia.org/wiki/All-time_Olympic_Games_medal_table).
This part consists of 4 questions which are based on making some basic data cleaning using Pandas library.

#### Example of question
Which country has the biggest difference between their summer gold medal counts and winter gold medal counts relative to their total gold medal count? Only include countries that have won at least 1 gold in both summer and winter.

### Part 2
In part 2 we are using [census data](https://github.com/Cybersheralt/Introduction-to-DS-Coursera/blob/main/Assignment%202/census.csv) from the [United States Census Bureau](http://www.census.gov). This dataset contains population data for counties and states in the US from 2010 to 2015.
This part consists of 4 questions which are based on making some data cleaning using Pandas library.

#### Example of question
Which county has had the largest absolute change in population within the period 2010-2015? (Hint: population values are stored in columns POPESTIMATE2010 through POPESTIMATE2015, you need to consider all six columns.)
e.g. If County Population in the 5 year period is 100, 120, 80, 105, 100, 130, then its largest change in the period would be |130-80| = 50.


## Assignment 3
This assignment is called ***More Pandas*** and based on analyzing Excel files in Python using Pandas library.

### Question 1 (Preparation for work)
First of all it was neccessary to load next datasets:
  - [`Energy Indicators.xls`](https://github.com/Cybersheralt/Introduction-to-DS-Coursera/blob/main/Assignment%203/Energy%20Indicators.xls), which is a list of indicators of energy supply and renewable electricity production from the [United Nations](http://unstats.un.org/unsd/environment/excel_file_tables/2013/Energy%20Indicators.xls) for the year 2013;
  - the GDP data from the file [`world_bank.csv`](https://github.com/Cybersheralt/Introduction-to-DS-Coursera/blob/main/Assignment%203/world_bank.csv), which is a csv containing countries' GDP from 1960 to 2015 from [World Bank](http://data.worldbank.org/indicator/NY.GDP.MKTP.CD);
  - the [Sciamgo Journal and Country Rank data for Energy Engineering and Power Technology](http://www.scimagojr.com/countryrank.php?category=2102) from the file [`scimagojr-3.xlsx`](https://github.com/Cybersheralt/Introduction-to-DS-Coursera/blob/main/Assignment%203/scimagojr-3.xlsx), which ranks countries based on their journal contributions in the aforementioned area.
 
 After that data was cleaned to make it readable. Main task was "Join the three datasets: GDP, Energy, and ScimEn into a new dataset (using the intersection of country names). Use only the last 10 years (2006-2015) of GDP data and only the top 15 countries by Scimagojr 'Rank' (Rank 1 through 15)."
 
 ### Main part
 Main part of this assignment consisted of 12 question, which were based on analyzing dataset from Question 1 using Pandas library.
 
 #### Example of question
 Create a new column with a 1 if the country's % Renewable value is at or above the median for all countries in the top 15, and a 0 if the country's % Renewable value is below    the median.
 
 
## Assignment 4
This assignment is called ***Hypothesis Testing*** and based on running t-test in order to check hypothesis. It can be divided in 2 parts.

**Hypothesis**: University towns have their mean housing prices less effected by recessions. Run a t-test to compare the ratio of the mean price of houses in university towns the quarter before the recession starts compared to the recession bottom.

Next datasets were used for this assignment:
  - From the [Zillow research data site](http://www.zillow.com/research/data/) there is housing data for the United States. In particular the datafile for all homes at a city level, [`City_Zhvi_AllHomes.csv`](http://files.zillowstatic.com/research/public/City/City_Zhvi_AllHomes.csv), has median home sale prices at a fine grained level;
  - From the Wikipedia page on college towns is a list of [university towns in the United States](https://en.wikipedia.org/wiki/List_of_college_towns#College_towns_in_the_United_States) which has been copy and pasted into the file [`university_towns.txt`](https://github.com/Cybersheralt/Introduction-to-DS-Coursera/blob/main/Assignment%204/university_towns.txt);
  - From Bureau of Economic Analysis, US Department of Commerce, the [GDP over time](http://www.bea.gov/national/index.htm#gdp) of the United States in current dollars (use the chained value in 2009 dollars), in quarterly intervals, in the file [`gdplev.xls`](https://github.com/Cybersheralt/Introduction-to-DS-Coursera/blob/main/Assignment%204/gdplev.xls). For this assignment, only GDP data from the first quarter of 2000 onward was used.

### Preparation
This part consists of 5 tasks:
  - Getting list of university towns and cleaning it from unnecessary data;
  - Searching for start of recession;
  - Searchinh for end of recession;
  - Searching for bottom of recession;
  - Converting housing data to quarters.

### Main part
Function `run_ttest()` works like described below.
First creates new data showing the decline or growth of housing prices between the recession start and the recession bottom. Then runs a t-test comparing the university town values to the non-university towns values, return whether the alternative hypothesis (that the two groups are the same) is true or not as well as the p-value of the confidence.


## List of used libraries
- Pandas
- Numpy
- Scipy
- re
