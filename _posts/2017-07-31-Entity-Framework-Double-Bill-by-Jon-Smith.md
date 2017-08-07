On 31 July I attended the **Dot Net Notts** meetup at the Unidays offices in Nottingham.

There were two presentations on Entity Framework given by Jon P Smith:

> Building Better Entity Framework Applications
>
>Entity Framework is designed to make accessing a database easy, but a bit of forethought can help to keep things from becoming a mess. Jon Smith will share some of the approaches, patterns and packages he has found useful in building robust, refactorable and well performing application quickly using Entity Framework. Suitable for both newcomers to Entity Framework and experts.
>
>DevOps and Entity Framework – migrating your production database
>
>Changing a database structure (e.g. the tables, columns in a database) isn't a trivial thing to do, especially when the database contains live data from real users. Jon Smith with describe some of the issues that can occur and why you need to be careful. He then shows some of the different ways you can change a database structure, using Entity Framework as an example.

**Building Better Entity Framework Applications**

Jon described a system architecture using EF and recommended we ignore the Microsoft examples for EF because they are just showing how easy it is to use EF rather than having a scalable, testable architecture.

The architecture outlined used a DTO layer to separate concerns, making the design simpler, easier to test and which passes “just the facts” though to the process requesting data from the DTO layer. DTO is made easier using AutoMapper (or other mapper).

Jon has created a generic service layer which is here on GitHub https://github.com/JonPSmith/GenericServices with an example at http://samplemvcwebapp.net/

The architecture also had an extra layer of business logic to further separate concerns and let the business logic care about the business processes only; the business logic doesn’t need to know about the persistence or presentation layers.

Jon gave some useful background on EF Core, describing it as a rewrite from the ground up so it’s better for non relational (NoSQL) databases and commenting that plugins for Oracle, MySQL and etc. easier to create for EF Core. Some of the methods have changed from EF 6.x and EF Core is now open source.

**DevOps and Entity Framework – migrating your production database**

Jon talked about various methods of migrating changes made in development to production databases.

One option is EF migrations. Using the EF Add-Migration method from the console and then calling the .Migrate() method to carry out the change. Add-Migration creates a set of migration files which EF uses to update the database. The difference with EF Core is that unlike EF6 migrations are not automatic. You need to explicitly call .Migrate() which you could put into the application start-up method. EF migrations can be hard to test or debug when they don’t work on the production database.

Another option is to reverse engineer an existing database using Scaffold-DBContext which recreates EFs “picture” of the database tables but you need to delete the existing classes and re-create them, which might cause issues in code. It’s important to note that EF has it’s own metadata on how the database is structured which is separate from the actual database schema.

A further option is to have SQL change scripts. You can use DBUp to run the scripts and use RedGate tools or the tools built into Visual Studio to help create the scripts by comparing development and production databases. You still have the problem of having to update EFs “picture” of the database tables.

It is possible to compare the database schema with EFs model of the database but this is apparently quite painful. Can use the https://github.com/JonPSmith/EfSchemaCompare tool to compare and this will be easier in EF Core because it has better methods exposing the EF metadata.

Jon also talked about database change problems; describing changes as either non-breaking or breaking schema changes. Non-breaking changes would be new fields or new database tables. Breaking changes would be removing fields or database tables for example.

To work round this you can take a website down for maintenance although this may not be possible, set a database to read only mode whilst changes are made or have a continuous service implementation. This reminded me of the last Dot Net Notts session on Building Scalable and Resilient Applications.

One concept I hadn’t heard about before was Azure Staging Slots which enables “hot swapping” of an old and new versions of a deployed application: Azure Staged Publishing

**Links**

<http://www.thereformedprogrammer.net/>

<http://efcoreinaction.com/>

<http://automapper.org/>

<https://github.com/JonPSmith/GenericServices>

<http://samplemvcwebapp.net/>

<https://dbup.github.io/>

<https://github.com/JonPSmith/EfSchemaCompare>

<https://docs.microsoft.com/en-us/azure/app-service-web/web-sites-staged-publishing>
