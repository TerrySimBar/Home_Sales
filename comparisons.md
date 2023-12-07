## It is useful to compare the runtimes for the same query on the different table types.

<img src="/images/run_times.png" alt="run times" width="1200"/>  

- A comparison of the run times for the same query on the different table types shows that the partitioned table has the highest run time, followed by the the temporary view, and then the cached table. 

- The query on the partitioned table was expected to have the lowest run time, but it could be that partitioning the data by the `date_built` column, but not using that column in the query is causing the query to run slower. The phenomenon could also be due to issues in the computing environment. A good next step would be to compare the run times for the same query that uses the `date_built` column on the different table types.

- The query on the temporary view has the second highest run time because the data is not cached in memory. 

- The query on the cached table has the lowest run time because the data is cached in memory.

- In conclusion, cache and partioning are generally recommended for optimizing the run time of queries on Spark DataFrames. 
