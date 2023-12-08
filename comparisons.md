## It is useful to compare the runtimes for the same query on the different table types.

<img src="/images/run_times.png" alt="run times" width="1200"/>  
<br>
<br>
- A comparison of the run times for the same query on the different table types shows that the partitioned table has the lowest run time of about 0.49 seconds, followed by the cached table with about 0.64 seconds, and then the temporary table with about 1.16 seconds.
<br>
<br>
- The query on the partitioned table has the lowest run time because partitioning reduces the amount of data processed during the query execution. 
<br>
<br>
- The query on the cached table has a lower run time than the query on the temporary table because the cached table is stored in memory, which is faster to access than disk.
<br>
<br>
- The query on the temporary table has the highest run time because the temporary table is not cached in memory nor partitioned.
<br>
<br>
- In conclusion, cache and partioning are generally recommended for optimizing the run time of queries on Spark DataFrames because they tend to have lower run times than running queries on temporary tables.  