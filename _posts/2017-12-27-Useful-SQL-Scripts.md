# Useful SQL Server Scripts

I'm going to start accumulating useful generic SQL Server Scripts in this repository: <https://github.com/richardlucas761/SQLScripts>

Starting off with a simple script to filter the output of the SP_WHO2 command which is always useful, particularly when debugging whether configuration settings are correct and whether something is *actually* connecting to the database you think it should be.

The basic sp_who2 command can't be filtered so this script puts output into a temporary table you can filter or sort to give more useful results.

<https://github.com/richardlucas761/SQLScripts/blob/master/FilterSPWho2Output.sql>

The script is taken from this StackOverflow post:

<https://stackoverflow.com/questions/2234691/sql-server-filter-output-of-sp-who2>
