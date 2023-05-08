# Home sale analysis with SparkSQL

In this project, we use SparkSQL to determine key metrics about home sales data. Spark is used to create temporary views, partition the data, cache and uncache a temporary table, and verify that the table has been uncached.

## Method

1. The home_sales_revised.csv data is read into a Spark DataFrame.

2. A temporary table called home_sales is created.

3. The average price for a four-bedroom house sold for each year is determined, the answer is rounded to two decimal places.

4. The average price of a home for each year it was built that has three bedrooms and three bathrooms is determined, the answer is rounded to two decimal places.

5. The average price of a home for each year that has three bedrooms, three bathrooms, two floors, and is greater than or equal to 2,000 square feet is determined, the answer is rounded to two decimal places. 

6. The  "view" rating for homes costing more than or equal to $350,000 is deermined. Also, the run time for query is recorded, the answer is rounded to two decimal places.

7. The termporary table home_sales is cached.

8. We check to see if temporary table is cached. 

9. Using the cached data, a query is run that filters out the view ratings with an average price of greater than or equal to $350,000. The runtime is recorded and compared to uncached runtime.

10. The data was partitioned by the "date_built" field on the formatted parquet home sales data.

11. A temporary table was created for the parquet data.

12. A query that filters out the view ratings with an average price of greater than or equal to $350,000 was run. The runtime is recorded and compared to uncached runtime.

13. The home_sales temporary table was unchached.

14. We verify that the home_sales temporary table is uncached using PySpark.
