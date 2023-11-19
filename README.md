# Module 22 Home Sales Challenge
# Overview of the Analysis

* The purpose of this analysis is your knowledge of SparkSQL to determine key metrics about home sales data. Then use Spark to create temporary views, partition the data, cache and uncache a temporary table, and verify that the table has been uncached.

* Objective of analysis is to review key metrics of home sales and create tables with data.

## Results
* Average price for 4 bedroom house sold in each year:

 date_built avg_price
       2010 296800.75 
       2011  302141.9
       2012 298233.42
       2013 299999.39
       2014 299073.89
       2015 307908.86
       2016 296050.24
       2017 296576.69


* Average price of a home for each year the home was built that have 3 bedrooms and 3 bathrooms: 
 
 date_built avg_price 

       2010 292859.62 
       2011 291117.47 
       2012 293683.19
       2013 295962.27
       2014 290852.27
       2015  288770.3
       2016 290555.07
       2017 292676.79


* Average price of a home for each year built that have a 3 bedrroms, 3 bathrooms, with two floors and are great than or equal to 2,000 square feet:
+----------+---------+
|date_built|avg_price|
+----------+---------+
|      2010|285010.22|
|      2011|276553.81|
|      2012|307539.97|
|      2013|303676.79|
|      2014|298264.72|
|      2015|297609.97|
|      2016| 293965.1|
|      2017|280317.58|
+----------+---------+

* What is the view rating for the average price of a home where the homes are greater than or equal to $350,000:
----+---------+
|view|avg_price|
+----+---------+
|   0|403848.51|
|   1|401044.25|
|   2|397389.25|
|   3| 398867.6|
|   4|399631.89|
|   5|401471.82|
|   6|395655.38|
|   7|403005.77|
|   8|398592.71|
|   9|401393.34|
|  10|401868.43|
|  11|399548.12|
|  12|401501.32|
|  13|398917.98|
|  14|398570.03|
|  15| 404673.3|
|  16|399586.53|
|  17|398474.49|
|  18|399332.91|
|  19|398953.17|
+----+---------+
only showing top 20 rows
* What is the run time?  
--- 2.0374855995178223 seconds ---

* Cache the temporary table home_sales:  
True

* Run a query that filters out the view ratings with average price great than or equal to $350,000.  

+----+---------+
|view|avg_price|
+----+---------+
|   0|403848.51|
|   1|401044.25|
|   2|397389.25|
|   3| 398867.6|
|   4|399631.89|
|   5|401471.82|
|   6|395655.38|
|   7|403005.77|
|   8|398592.71|
|   9|401393.34|
|  10|401868.43|
|  11|399548.12|
|  12|401501.32|
|  13|398917.98|
|  14|398570.03|
|  15| 404673.3|
|  16|399586.53|
|  17|398474.49|
|  18|399332.91|
|  19|398953.17|
+----+---------+
only showing top 20 rows

--- 0.9196372032165527 seconds ---

*Also, determine the runtime and compare it to the uncached run time. 
Cached is 2 times faster than uncached.

*Run a query that filters out the view ratings with the average price of greater than or equal to $350,000 with the parquet DataFrame.  

+----+---------+
|view|avg_price|
+----+---------+
|   0|403848.51|
|   1|401044.25|
|   2|397389.25|
|   3| 398867.6|
|   4|399631.89|
|   5|401471.82|
|   6|395655.38|
|   7|403005.77|
|   8|398592.71|
|   9|401393.34|
|  10|401868.43|
|  11|399548.12|
|  12|401501.32|
|  13|398917.98|
|  14|398570.03|
|  15| 404673.3|
|  16|399586.53|
|  17|398474.49|
|  18|399332.91|
|  19|398953.17|
+----+---------+
only showing top 20 rows

--- 0.7788023948669434 seconds ---
* Also, determine the runtime and compare it to the cached version.
This version is .14 seconds faster than the cached version.  Overall the parquet DF is the faster and more effecient way.

## Summary
*With this project determined that the parquet DataFrame was the faster version compared to the cached and uncached versions.  
  
