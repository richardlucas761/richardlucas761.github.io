On 26 June I attended the **Building Scalable and Resilient Applications** Dot Net Notts event presented by Steve Spencer at the UNiDAYS offices in Nottingham.

>**Introduction to Azure Service Fabric**
>
>Azure Service Fabric is the Microsoft microservices framework and this talk explains how to build applications that can be deployed in Azure or on your own infrastructure.Service fabric lets you deploy your own existing services or build them using the service fabric framework to take advantage of the built-in microservices features that service fabric provides
>
>Steve is an experienced .NET Developer, Microsoft Azure MVP and a Senior Solution Architect at Liberis. Steve has spoken at previous DDD events covering Microsoft Azure, Gadgeteer, Service Bus and Azure Web jobs Steve has also recently appeared on channel9 also talking on Service Fabric - <https://channel9.msdn.com/Events/TechDaysOnline/UK-TechDays-Online-September-2016/Service-Fabric-for-the-Microservices-Win-baby>

This was the first time I had encountered Azure Service Fabric, one of the almost daily additions to Azure and not being from a deployment background it was interesting but difficult to see the benefit where I'm not experienced in container technologies.

I could understand the cool fail over features and "let Azure do the work of managing things in the cluster for you" but there wasn't a moment of thinking this would really help with something.

The information was presented well but like some of the earlier Azure SQL Data Warehousing and Data Lake events I didn't immediately think this was something I could make use of.

I could always experiment as the ability to run Service Fabric Clusters locally (with the same user interface as the cloud based version on Azure) was useful. Although I might need to learn Microsoft Hyper V as I've mostly been using VirtualBox for any VM experiments at home, perhaps that works just as well? On the reverse side being able to debug remote instances running in Azure from Visual Studio sounded very useful!

I've got experience of building Microservices but less experience of actually deploying them into production and maintaining them because of the size of the organisation I work for; we have whole departments of people to deploy and manage live software with specific DevOps people.

The talk either taught me or confirmed ideas about aspects of building scalable & resilient Microservices such as the idea that if some part of the system goes down the rest should still be available by using message queues to retain information.

If the web farm is down it should still be possible to continue processing orders which have already made it into the system so that customer orders aren't lost. Being able to do "as much as possible" when some part of the architecture was either broken or not behaving correctly was a useful thing to keep in mind. Scalability and scaling up (and out) was also discussed with the problems of legacy systems such as mainframe systems being a bottleneck in the architecture.

I hadn't previously encountered Reliable Collections, highly availability, replicated collections for the cloud, although this isn't something I need to work with at the moment, something to keep in mind for later.

**Links**

<http://blogs.recneps.net>

<https://twitter.com/sdspencer>

<https://azure.microsoft.com/en-gb/services/service-fabric/>

<https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-reliable-services-reliable-collections>

<https://www.virtualbox.org/>
