**The Basics of Good T-SQL Coding Style (On Simple Talk)**

This is a handy reference for the basics of T-SQL and I've added the Simple Talk feed into my The Old Reader feeds as it looks like there are some other good articles on this site.

Being mostly self taught I've probably picked up a few bad habits over the years learning SQL Server on the job; habits that haven't been corrected yet:

I should stop writing TOP statements like this:

```SQL
SELECT TOP 10 Title, FirstName, LastName
FROM Person.Person;
```

And start writing them like this instead:

```SQL
SELECT TOP(10) Title, FirstName, LastName
FROM Person.Person;
```

I should probably stop referring to tables without specifying a schema (when I know there is only one schema) like this as well, but I only do this when I'm fixing things or tinkering with databases, I almost never do this in production T-SQL!

```SQL
SELECT Title FROM Person..Person;
```

It should be like this (assuming the schema is dbo):

```SQL
SELECT Title FROM Person.dbo.Person;
```

**Links**

<https://www.simple-talk.com/sql/t-sql-programming/basics-good-t-sql-coding-style/>

<https://theoldreader.com/>
