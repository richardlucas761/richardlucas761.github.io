[January Nottingham SQL Server group meetup](https://www.meetup.com/PASSEastMidlands/events/256620837/)

# Kubernetes and Big Data Clusters - Chris Adkin

> SQL Server 2019 ushers in a new data platform in the form of big data clusters, this runs on Kubernetes, a container orchestration framework. But why do we require container orchestration frameworks, what is Kubernetes, its a platform, but how is it different from one has gone before and what are the essential things that Microsoft data platform professionals need to know about it, This session will aim to answer all of these questions and more.

Chris gave an overview of Kubernetes in the context of [Microsoft Big Data Clusters](https://docs.microsoft.com/en-us/sql/big-data-cluster/big-data-cluster-overview?view=sqlallproducts-allversions) (running on Kubernetes).

I'm currently working with Open Shift which is an enterprise container platform so it was interesting to hear about some of the underlying technologies of Docker and Kubernetes.

# Data Masking in SQL Server - Stuart Moore

> We'll look at Dynamic Data Masking introduced with SQL Server 2016 which allowed you to dynamically mask data based on user rights. And we'll look at the incoming Static Data Masking functionality that makes it simpler to mask data as it's moved to a test environment or sent to a 3rd party.

Stuart discussed the options for data masking including the [Dynamic Masking](https://docs.microsoft.com/en-us/sql/relational-databases/security/dynamic-data-masking?view=sql-server-2017) introduced in SQL Server 2016 and [Static Masking](https://azure.microsoft.com/en-us/blog/static-data-masking-preview/) (note the preview so that link will probably be broken later) in SQL Server 2018 Preview 5, also the options available in [DBAtools](https://dbatools.io/masking/).

The [Mockaroo](https://mockaroo.com/) tool for creating fake but realistic data and the [C# Bogus](https://github.com/bchavez/Bogus) separate tools were also mentioned.