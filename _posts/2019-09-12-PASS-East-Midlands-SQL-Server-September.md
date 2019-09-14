# Nottingham SQL Server user group September Meeting

<https://www.meetup.com/PASSEastMidlands/events/256620864/>

## Tobiasz Koprowski, Player No 1 in Security Centered World

> Cloud Services are everywhere. Data is everywhere. As Data Professionals we know what we should do to secure our data and leverage responsibility (just a little with moving it to the provider side). But we can do little more. We (especially if we are players) can play a little with game where points are pointless but our actions not. Using Microsoft Security Center which is free, powerful and huge service located in the centre of our Azure Subscription, we can look for our databases from a little different perspective. Maybe even see completely new horizon. During this session (90% demo focused) we will discover Microsoft Security Advisor and how features of MSA can support process of increasing security for SQL Azure Database and SQL Server Database too.

Tobias gave us a brief history of SQL Server on Azure and Microsoft's policy of making new features for SQL Server "cloud first" so they appear on this platform before the on premise version.

As a database name needs to be globally unique on the Azure platform this might cause issues with existing naming conventions, similarly for the admin account as "sa" will already exist!

The talk gave details of the Advanced Data Security option for databases, a free trial at first although we didn't look into the costs after the trial had ended. This gives periodic scan reports of the security health of databases and can alert on SQL injection attempts, unexpected data extracts or unexpected client logins (from a different country for example).

The Security Center on the Azure Dashboard was demonstrated which gave a security score for individual databases or per tag or account, useful for regulatory compliance or seeing which virtual machines need updates installing.

Data Discovery and Classification recommendations report on potentially sensitive data in your databases, running the report against the standard AdventureWorks database highlighted some columns and row data which could be GDPR or PCI data. The column name scanning only works for English names at the moment. It's also possible to classify your own columns to describe the data they contain, flagging certain columns as highly confidential for example.

It was interesting to note that new Azure SQL databases have Transparent Data Encryption (encryption at rest) enabled for free. You can either trust Microsoft (as you're using their platform already) or use your own certificates.

## Barney Lawrence, DAX Explained Through Dance, Memes and Dad Jokes

> Moving beyond the basics of DAX can be tough, there are several key concepts that can be hard to grasp before more complex expressions can be confidently written. This session will help anyone who is either looking to move their formulae up to the next level or looking to support others in doing the same by providing new ways of thinking about some of these concepts. You will learn how filter and row contexts are like a barn dance, how CALCULATE can work like a distracted boyfriend, explore filtering with punchlines and discover what makes a Zebra Fish blush.

I don't work with Power BI so most of this talk went over my head a little!

Barney described a training process for the Power BI DAX query language and how it was possible to get "simple" results quickly but how quickly you run into problems when trying to get more complicated results.

With some understanding of how the query language works it's possible to solve these issues in Power BI rather than shifting the problem to the left and creating either calculated columns or special views in the database to provide the information needed.

This would be important in an environment where it takes 2 weeks to make a database change or read-only access to the source databases is the only option and database changes aren't possible.

Iterators, filters and calculation operations were described, I'll update this post later if I can find a copy or link to Barney's slides.

## Links

<https://twitter.com/KoprowskiT>

<https://twitter.com/SQLBarney>