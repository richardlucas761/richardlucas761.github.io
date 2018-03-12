# [East Midlands SQL User Group March 2018 meetup](https://www.meetup.com/PASSEastMidlands/events/246932899/)

## DBA Emergency Toolkit

> This month we'll be welcoming Rich Benner <https://richbenner.com/> along. He'll be talking about what a DBA needs to have in their toolkit to cope with today's SQL server problems and issues. He';ll be discussing tools and scripts you want to know about, and then more importantly how to analyse their out and act upon it. More details on the session here - <https://groupby.org/conference-session-abstracts/making-your-emergency-toolkit/>

The scripts that Rich presented were primarily used for on premises fixes of customer databases.

It was interesting that some of the examples were using a SQL server database data dump of the StackOverflow database, not a massive amount of tables but certainly plenty of rows of data. I've included a link at the bottom of this article.

It's been a while since I've been even a development DBA (previously at PAREXEL) but it was interesting to hear about someone who has to maintain production databases which is something I haven't done for even longer.

I've created my own new repository for SQL scripts that I find useful but since I'm rarely touching SQL Server databases at the moment I haven't had the opportunity to fill this directory!

[Rich Benner Emergency Toolkit presentation](https://groupby.org/conference-session-abstracts/making-your-emergency-toolkit/)

[My SQL Server toolkit on Github](https://github.com/richardlucas761/SQLScripts)

## Under the hood of SQL Server backups

> I'll be talking about what goes on under the hood of SQL Server backups. By it's nature this is going to be a bit of a dive into the world of transaction process, write ahead logging and SQL Server internal structures and buffers. But by understanding what's going on internally you can build better backup and restore plans.

This was an interesting insight into the internal workings of SQL server backups and also how SQL Server itself works at a lower level, this gave me a better understanding of why SQL Server famously uses up so much memory.

[Stuart Moore Backup Internals script and power point](https://github.com/PassEastMidlands/Presentations/tree/master/Stuart-Moore-Backup-Internals-08032018)

## Links

[Rich Benner](https://richbenner.com/)

[Stuart Moore on Twitter](https://twitter.com/napalmgram/)

[Stuart Moore Website](https://stuart-moore.com/)

[Stack Exchange Data Dump sample databases](https://archive.org/details/stackexchange)
