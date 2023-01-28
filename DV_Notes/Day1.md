# Notes:

## Day 1:
### Problem 1: count number of records where category is selected category and inventory is more than 1000.

### Problem 2: count number of records where category is selected category and sales is less than value selected in drop down.



## Day 2:
Location Sheet
B1 : E157


## Day 3: Linear Regression
Profit = 3.040261769 +
Margin	* 0.734616817 +
Sales	* 0.421887012+
COGS	* -0.275604118+
Total Expenses	* -1.309824644+
Marketing	* -0.051838478+
Inventory	* -0.00587207

130	219	89	36	24	777

3.040261769 + 130	* 0.734616817 +219	* 0.421887012+89	* -0.275604118+36	* -1.309824644+24	* -0.051838478+777	* -0.00587207



### Tableau
it is a story telling software, with visualization and data
	a. What is Tableau? 
	- tableau will help anyone understand data better, as it gives one access to the amount of data in easily digestible visuals
	- details https://intellipaat.com/blog/what-is-tableau/
	
### Types of tableau
a. Public
	1. Free
	2. no support of RDBMS 
	3. does not allow local machine storage, everything has to be stored in cloud
b. Desktop
	1. Paid
	2. support of RDBMS
	3. allows files to be stored in office/local machine like laptop and desktop 
c. Server
	1. to host yourself
	2. Integrate data insights where you work
	3. flexibility
d . measure is a numeric feild (with or without decimal) on which stats or maths operations can be performed to get meaningful results.
	eg :: sales ,quantity , marks , discount , tax, profit, expenses etc.

	1:: Any primary or foreign key with numeric value can't be classified as measure.
	2:: Dimension -- Dimension is eighter a numeric or chracter or date feild which is used to group the measure feild data.
			Usually dimensions are categorical feilds eg:: date ,survey ratings etc.
			only maths operations permitted on dimensions is count.
		Dimensions 7 measure are combined to create management reports. eg:: Dimension = city & measure = sales ,report = Citywise Sales
e. Components of Tablue
	
	1:: Worksheet
	2:: Dashboard :: Dashboard can be created using worksheet . story can be created using worksheet or dashboard . but dashboard can't be
		  created using story
	3:: Story	  
f. Data Types in Tableau
	1:: String 
	2:: Number
	3:: Date 
	4:: Date Time
	5:: True/False
	6:: Geographic (Lattitude & Longitude)
 
g. Use of colours in tableau -

	1:: Dimension are displayed in blue colour while measure are displayed in green colour
	2:: Dates in Tableau has two types - discrete & continous 
	3:: Discrete dates are displayed in blur color and continous dates are displayed in green color.

h. Tableau provides 24 different types of chart by default divides as 8 rows & 3 columns . Every Chart shows its requirments

	
i. two functions for count and mean/average

SUM() function calculates grand total
AVG() function calculates average value
COUNT() function calculates total NO. of records including duplicates while COUNTD() function calculates no of unique records only
by removing duplicates

			COUNT 		COUNT DISTINCT
BINDERS	 	6152			5392


How Many Types of Bar Charts are available in Tableau?
1. Simple bar chart - one dimension
2. Side by Side chart - multi dimension
3. Stacked bar chart - multi dimension

Show me button row number 3

Dimension in Rows
and Measure in Columns
use swap button to make it vertical


Colors to solve business problem

Identify the regions have total sales less than 750k

# 2 MEASURES IN BAR CHART:
-----------------------------
Rows = category
Columns = Qty
Profit = Color under marks
Quantity by Sub-Category highlighted by Profit


problem: 
--------
1. Sales by Region highlighted by Profit
2. Shipping Cost by Market highlighted by Profit = Shipping cost and Profit vary together, linear relationship


# Stacked Bar Chart:
---------------------

1. Horizontal Bar: Sales % by Sub-Category & Segment(100% Stacked Bar)
	1. Sub-Category on Rows
	2. Sales on Columns to make normal bar chart with labels on Sales
	3. Segment on Color
	4. Percentage of Row i.e. Sub Category % to make stacked
	
problem:
--------
1. Quantiy % by Region & Category (100% Stacked bar)
2. Shipping Cost % by Market & Ship Mode (100% Stacked bar)

# Side by side bar chart:
------------------------
Shipping Cost by Category & Ship Mode(Side by Side bar chart)
Columns: Category with Ship mode side by side
Rows: Shipping Cost
Color: Ship Mode

problems:
----------
1. Profit by Category & Ship Mode(Side by side bar chart)
2. Profit by Segment & Category(Side by side bar chart)
3. Quantity by Ship Mode & Category(Side by side bar chart)
4. Sales by Ship Mode & Segment(Side by side bar chart)


Last bar chart
Using Count
to show number of products
Rows: Country (147)
Label: Product ID (Dimension, blue)
		we make it Measure with Count Distinct
Column: CNTD(Product ID)
Rows: Market, Country

Number of Product in Each country and each market
Color: Market


# LINE CHARTS
--------------


Problem: 
--------
Highlight the Sub-Category & Ship-Mode combinations that have sales more than 500K.

	
Tree map with parent & child dimensions:
----------------------------------------

This technique is used to group the child values by parent values.
eg. State and City 
	State will be parent
	City will be child

in superstore dataset
1. sub-category and category
2. market and region
3. country and state
One to Many type of relationship


Steps
-----
1. create simple tree map with text table
2. put parent in color
3. we will observe sum largest on top left that is 1st, then 2nd below it
4. to the right we will find lower sum



Geographical Chart:
-------------------
1. symbol map
	* for each value it will show a small circle 	
	* symbol for differentiation
2. solid map (choropleth)
	* entire area is given a particular color in background 	
	* color for differentiation
	
	

Requirement:
At least one geological field




# SCATTERPLOT
----------------

Actual Sales vs Actual Profit
x vs y
without aggregation 

P-value:	< 0.0001
Equation:	Actual Profit = 0.536582*Actual Sales + -42.456

Coefficients
Term	Value	StdErr	t-value	p-value
Actual Sales	0.536582	0.0062333	86.0837	< 0.0001
intercept	-42.456	1.52785	-27.7881	< 0.0001


R square is 0.63 i.e. 63% variation in Profit due variation in Sales.
Rest 37% variation is due to unknown factors.

1. Using the line equation, predict the profit if Sales reaches 1100.
2. Predict how much sales is required to get Profit of 1000?


A1. 547.78 ~ 548
A2. 1942.77



COGS & Profit
-------------

P-value:	< 0.0001
Equation:	Actual Profit = 0.666183*Actual COGS + 5.14896

Coefficients
Term	Value	StdErr	t-value	p-value
Actual COGS	0.666183	0.0202602	32.8814	< 0.0001
intercept	5.14896	2.19923	2.34126	0.019265


Analysis:
Equation:	Actual Profit = 0.666183*Actual COGS + 5.14896

R Square is 0.20 i.e. 20% varition in Profit due to variation in COGS.
Rest 80% variation is due to unknown factors.

for 1000 Profit 1493.3599926746856 COGS


# Business Question:

1. Compare two products - Decaf Espresso  & Lemon 
2. Which one is better and why?
3. Decaf is better! same profit with less amount of sales. 


# Histogram
1. bin size = 10
2. each bin with 10 values
3. 0-9 there are 10 values. 
4. 10-19
5. 20-29
6. 30-39
7. 40-49...
8. 620 is count for marketting in records bin of 0-9
9. 1226, 938, 404, 328...
10. total 4248 at left bottom
11. 4248 is total, 1228 is 28% values
12. so 1226 records having marketting value between 10-19

# Histogram for Profit
1. bin size in right hand side edit and set to 100
2. so we have 0-99 starting values in the 1st bin
3. we can observe 0-99, 100-199, 200-299 ... 
4. and -1 to -100, -101 to -200
5. highest value 2748 occupies 65% of count
6. as profit increases, no of records decreases
7. So there are
8. 65% of records have profit value between 0-99



# Calculated Field
Average Sales per Order
SUM([Sales])/[No. of Orders]

Average Profit per Order
SUM([Profit])/[No. of Orders]


Average Qty per Order
SUM([Quantity])/[No. of Orders]


# CONDITIONAL CALCULATIONS
Calculate profit for year 2013 & 2014.


# Profit Ratio
total profit / total sales


# PARAMTERS:

1. Some variable you pass to function
2. we use them in calculated fields and filters
3. where to create? in Data pane, small inverted arrow
4. independent paramter: used in top/bottom filter eg. top-5,top-10,top-15 dynamically
5. once created, it can be reused multiple times
6. interview question: what is the difference between value and display as
7. # green color, numeria
8. edit field and in top menu select paramter
9. show paramter will show the parameter 
10. we will choose single value list
11. we will use Format to change animation to 1 second
12. parameter with reference line
13. we have to decide starting, ending and step value for reference line
14. 100K to 1000K and gap 100000 => sales reference parameter
15. we can add shaded area by format-> fill below for the reference line
16. create calculated field with SUM([Sales]) <= [Sales Reference Limit]
17. CREATE BAR CHART FOR SUB-CATEGORY & QUANTITY, BUILD PARAMTER 'QTY REF LIMIT' 
	with min = 3000, max = 20000, step = 1000
18. parameter to select the fields
19. so we have 3 techniques:
							1. independent parameter
							2. parameter with reference line
							3. parameter to select fields
20. tool tip can also be edited
21. first create a list with Values as name of the column, remember that column values are case sensitive
22. solid geo map based on country, paramter, field on label
23. whenever parent-child relationship don't use in row-column so we will choose:
	1. Market
	2. Order Priority
	3. Segment
	4. Ship Mode
24. Table Calculations -  white verticle triangle
	This technique is Tableau is used to convert normal measure values into
	1. running total - quick table calculations,
	2. Difference 
	3. % difference
	4. Rank - with and without date(quick table calculation in Marks) by default they go horizontally, computing using Table(down) for column wise
	5. % of Total
	6. Moving Average - used by stock market analysts to reduce noise and fluctuations in share data,to make the line smooth. 
					  - Default setting is 3 period moving average. Current + 2 previous / 3
					  - JUN+MAY+APR/3 = PRICE(JUN)
					  - Date field is compulsory
					  - Table calculation for choice of period
					  - for Aug =?

25. Calculated fields using conditional statements: 
	1. Creating conditions based on numeric range - color chart on multiple colors on different range
		1. sales < 200K -- very low
		2. sales above 200K and below 500K -- Average
		3. sales above 500K and below 1000K -- Good
		4. sales above 1000K -- Excellent 
	2. =Abc in blue, character calculated field
	3. Treemap with custom calculated fields
		1. < 5k - q1
		2. <= 5k and > 10k - q2
		3. <= 10k and > 15k - q3
		4. <= 15k and > 20k - q4
		5. \> q5 	
		
26. LOD (level of detail) expression
	1. Fixed
	2. Include
	3. Exclude
	Mostly used for 
		1. PROFIT BY REGION - LOD
		2. QTY BY CATEGORY - LOD

# DASHBOARD CREATION
1. Copied images into C:\Users\admin\Documents\My Tableau Repository\Shapes
2. Topics for today:
	1. analytics in tableau
	2. dashboards
	3. story 

## Analytics options
1. Constant Line - fixed target, double click to add to view, right click-> format
	1. constant cannot be controled by paramter
	2. reference line can be controlled by parameter  
	3. create scatterplot by double click 1st measure then 2nd mesasure, drag region on view
	4. with scatterplot we can use 2 constant lines
2. Average Line - to compare below n above
	1. in Analytics, drag it to view and choose table
	2. can be set to pane
	3. line position changes based on selection, in constant line position cannot change
	4. shading can be added and it does not change position, avg line position change on select 
3. Trend Line - 
4. Forecasting - for time series analysis
	1. what is difference between forecasting and prediction ? 
		1. prediction is done with linear regression, independent variable vs dependent variable and we don't care about time
		2. in case of forecasting, the forecasting is done on time series value, time based forecast is done and future values are predicted. We don't use linear regression.
	2. Forecasting applied only on line chart
	3. Date in column
	4. Sales in rows
	5. Switch to continuous month, bottom month option in right click menu
	6. Double click Forecast on Analytics pane
	7. Forecast options in right click on shaded new line on the view
	8. Source data ignore last 0
	9. Automatic next 12 months
	10. Exactly year, qtr, month
	11. Forecast Model: choose option which is suitable
	12. the shaded region outside trend line is the 95% confidence interval
5. Cluster 
	1. take profit and sales to create scatterplot
	2. we added country
	3. filter region
	4. central filter
	5. double click cluster in analytics now
	6. now we choose which number looks good
	7. we can get the following data in right click on marks card for clusters




Inputs for Clustering

Variables:	Sum of Profit
Sum of Sales
Level of Detail:	Country
Scaling:	Normalized


Summary Diagnostics

Number of Clusters:	4
Number of Points:	12
Between-group Sum of Squares:	2.1293
Within-group Sum of Squares:	0.11589
Total Sum of Squares:	2.2452


								Centers								
Clusters					Number of Items			Sum of Profit				Sum of Sales				
Cluster 1					6			23937.0				1.0235e+05				
Cluster 2					3			-29425.0				73060.0				
Cluster 3					2			1.0818e+05				7.4389e+05				
Cluster 4					1			39706.0				5.0124e+05				
Not Clustered					0	

Analysis:
GERMANY PROFIT AND SALES 107323,109029
CLUSTER 3 SCORES ARE CLOSER TO IT SO ITS SAME AS FRANCE


# DASHBOARD

1. Create KPIs:
	1. Calculated Field: Profit Ratio : sum of profit/ sum of sales
		1. Default Property: number format: percentage
	2. Calculated Field: Number of Order: COUNTD of order id
	3. Calculated Field: Number of Customers: COUNTD of Customer id
	4. Calculated Field: Number of Products: COUNTD of products id
	5. Calculated Field: Avg of Sales
		1. Default Property: number format: percentage
	6. Calculated Field: Avg Profit
		1. Default Property: number format: currency custom decimal = 1
	7. Calculated Field: Avg Qty
		1. Default Property: number format: decimal places = 0
	8. Calculated Field: count of row id
2. Sheet number 1 - Sub-Category icons
	1. Drop sub-category in columns
	2. change automatic to shape, drop subcategory in shape option
	3. shape, reload shapes, choose the image shapes in Select Shape Pallet
	4. set size and remove legends
	5. hide field lables for column in view 
	6. rename sheet Sub-Category icons
3. Sheet number 2 - Person
	1. set view to Entire View
	2. Person on shapes
	3. choose right pallete 
	4. remove legend
	5. increase size
	6. hide label
	7. name of sheet Manager icons
4. Sheet number 3 - Market icons
5. Add new Dashboard with + dashboard at bottom next to sheet
	1. Dashboard object options
		1. Container -  
		2. Blank - 
		3. Web Page - static/dynamic from online pages like WHO, wikipedia, UN, Yahoo finance etc.
		4. Image - factory, product image etc.
		5. Text - some text intro or info
		6. Navigation - to move from one dashboard to another
		7. Download - download dashboard to machine
6. we created a pie chart with category and orders count, name Category Master
7. another for segment - Segment master
8. two line charts next with continuous quarter for sales, profit with names Quarterly Sales and Quarterly Profit	
9. Geographic chart - Country Master
10. next, bar chart for Sub-Category & Sales/Profit etc
11. Scatterplot with avg line
12. Go to dashboard - Size - Automatic
13. Choose vertical object
14. drop bar chart 
15. hide title
16. choose next sheet that is line chart and drag till you see desired shaded region
17. we will have source-target relationship between top and bottom with Actions..
	1. add filter in Actions under Dashboard menu
	2. Filter Sales by SubCategory, source bar chart, target line chart
	3. run action on select
	4. show all values
	5. OK!
18. Dashboard 3
	1. Market
	2. qrtly sales
	3. qrtly profit
19. Dashboard 4
	1. logo - manager 
	2. countries - scatterplot
	3. two filters
20. this layout [+]
	1. (1) cate pie
	2. (2) sales line
	3. (3) seg pie
	4. (4) profit line
21. Webpage demo
	1. https://en.m.wikipedia.org/wiki/India
	2. https://en.m.wikipedia.org/wiki/Canada 
22. Highlight Action
	1. with parent child relationship
	2. add category on detail for bar and scatter
	3. make dashboard with pie chart for category
	4. add highlight filter for source as category
	5. 