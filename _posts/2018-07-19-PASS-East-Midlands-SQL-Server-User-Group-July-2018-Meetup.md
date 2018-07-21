# [July 2018 Meetup](https://www.meetup.com/PASSEastMidlands/events/252558555/)

## Effective Unit Testing for SQL Server by Gavin Campbell

> We've all written lot's of T-SQL, but how much of it has been tested to make sure it actually works. What does happen if someone submits a negative value to that payroll script?

> In this session Gav will walk through the why and how of testing your T-SQL code. Untested code is just a bug waiting to be discovered.

There has been a continuing theme of unit testing things you perhaps wouldn't normally consider unit testing in the recent PowerShell and SQL Server meet ups, I wonder whether it's because Continuous Integration or Continuous Delivery into either Virtual Machine or Containerised environments is driving this?

Gavin's talk was introducing the concept of unit testing SQL server and gave a brief history of unit testing from the _sUnit_ testing platform for SmallTalk through _NUnit_ and to [tSQLt](https://tsqlt.org/).

(As a side note Gavin mentioned a sample testing database I hadn't heard about before, the ["Chinook"](https://github.com/lerocha/chinook-database) database)

I've done limited work with tSQLt myself a few years ago but only as a proof of concept rather than anything serious but some of the information presented was at least familiar to me.

The installation of the tSQLt framework was discussed, it's possible to install it using the [DBATools](https://dbatools.io/) framework and the DLL is whitelisted for installation on Azure SQL DB.

tSQLt makes it possible to create test classes even though SQL Server doesn't have a concept of a "class" so each test resides in a schema. tSQLt also provides tools for mocking tables, the ability to create shared set up actions for a suite of tests (although this hides some of the arranging details for test, helpers or builder classes are probably better) and the ability to "spy" on procedure calls to ensure a call took place.

As per previous posts this and the Pester testing of PowerShell is very familiar to me as a C# developer and it's good to hear about automated testing of SQL Server.

## ETL orchestration in TSQL by Richard Swinbank

> There are many techniques for orchestrating ETL processes, but the difference between good ones and great ones is how they perform when things go wrong. Desirable behaviours – like fault tolerance, quick fault finding and easy resume after error – often aren't available and sometimes seem hard to achieve. In my session I'll present an approach to doing this using only TSQL and the SQL Server Agent, and which also enables parallel processing, adapts to evolving workloads and provides a wide variety of monitoring and diagnostic information.

I haven't worked with SSIS myself but I have seen it discussed at previous PASS SQL Server User Group sessions.

Richard's talk presented strategies for ETL and outlined options for carrying out data loading using various methods and outlined five desirable aspects of a good ETL system, being:

* Parallel, the ability to run multiple processes at once
* Easy to locate faults
* Easy to resume
* Restartable with as little work to do as possible
* Easy to add new processes

Methods discussed were using SQL Server Agent Jobs and using a master SSIS package, each with their own strengths and problems.

Richard introduced his [Sprockit](https://www.richardswinbank.net/sprockit) tool for ETL orchestration which is composed entirely of T-SQL.

The tool satisfies all of the five desirable aspects as laid out above and includes useful database tables about the interdependencies of processes, being able to use this information to display information using [GraphViz](http://graphviz.org/) was also discussed, I've only ever created simple diagrams using this markup language myself in Confluence.

## Links

["Chinook" Sample database for SQL Server, Oracle, MySQL, PostgreSQL, SQLite, DB2 ](https://github.com/lerocha/chinook-database)

[tSQLt testing framework for SQL Server](https://tsqlt.org/)

[DBATools](https://dbatools.io/)

[Richard Swinbank, Sprockit](https://www.richardswinbank.net/)

[GraphViz](http://graphviz.org/)