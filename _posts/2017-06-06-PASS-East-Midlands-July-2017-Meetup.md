On 6 June 2017 I attended the **PASS East Midlands July 2017 Meetup** event presented by Paul Andrew and Alex Whittles of Purple Frog at the Capital One offices in Nottingham.

There were two talks presented this evening:

>**Building an End to End IoT Solution Using Raspberry Pi Sensors & Azure**
>
>The Internet of Things is the new kid on the block offering a wealth of possibilities for data streaming and rich analytics. Using a Raspberry Pi 3 we will take an end to end look at how to interact with the physical world collecting sensor values and feeding that data in real-time into cloud services for manipulation and consumption. This will be a heavily demonstrated session looking at how such an environment can be setup using Microsoft offerings, including; Windows 10 IoT Core, a C# Universal Windows Platform application, an Azure IoT Event Hub, Azure Stream Analytics, Azure SQL DB and Power BI. This is an overview of what’s possible, but showing exactly how to build such a simplified solution with a session which will be 90% demonstrations. This will hopefully add that level excitement to real-time data with plenty of hardware out there showing what it can do when setup with Microsoft software.

The introduction to Paul's talk described a processing model where there was a constant stream of push notifications from multiple different data sources rather than a more traditional model with static flat files to process. This introduced me to the concept of Lambda architecture.

Paul demonstrated a Raspberry Pi 3 with a Fez Hat from GHI Electronics add-on providing temperature and light sensors (amongst others). A simple way to attach multiple sensors to a Raspberry Pi.

The Pi was demonstrating a simple architecture where the Pi was connected to an Azure IoT Hub and from there into Stream Analytics which provided outputs into both an Azure SQL DB and Power BI. The IoT Hub can be run for free on Azure although it has a limit of 8000 messages per day.

The Pi itself was running the Windows IoT Core operating system and I was impressed at how simple it looked to both install the operating system onto the Pi and interact with it from Windows 10 from both a device explorer and RDP-esque interface into the Pi.

The demonstration showed how simple it could be to hook up a physical device both to an Azure cloud processor and data storage. It was also nice to see some C# code in the application which read data from the Fez Hat sensors and pushed it into Azure.

I've worked on a system which was similar at PAREXEL recently called ClinPhone Active Tracking which tracks both the temperature and location of temperature sensors inside consignments of medication. In that case the sensors were pushing data into a private cloud but the concept was similar.

And the second talk:

> **Introduction to U-SQL and Data Lake**
>
>U-SQL is the new kid on the SQL language block, and Data Lake is the big data buzzword. In this session we'll look at the what, where, why and how of U-SQL. Is it a query language? Is it a data transformation or an analytics language? How does it fit into Azure Data Lake? And what even is Data Lake?

I'd attended a hands-on session given by both Paul and Alex in May at a Notts Dev Workshop (previous blog post) so I'd heard most of the information presented but with it being a presentation rather than a hands on session it was still interesting the second time.

What I took away from the second hearing was Azure Data Lake was like "Map Reduce 2.0 but without retraining" (for those of us from a mostly Microsoft database background) and Data Lake was the "T" in an ETL solution.

I don't think we had covered the post run diagnostics for Data Lake jobs in the previous session which like the query analysis tools in SSMS for SQL Server showed where you were using too many Azure processing units (and therefore could save some money!)

It was interesting to hear that the interfaces into these cloud services from Visual Studio were still a bit buggy as this was one of the problems I found during the previous hands on session. In that session I had to give up on trying to use Visual Studio 2017 and go back to Visual Studio 2015 (with it's installed rather than built-in extensions) as this seemed more stable.

**Links**

<https://www.purplefrogsystems.com/paul/wp-content/uploads/2016/05/PASS_EastMids_IoTTalk.pdf>

<https://www.purplefrogsystems.com/>

<https://en.wikipedia.org/wiki/Lambda_architecture>

<https://www.parexel.com/solutions/informatics/randomization-and-trial-supply-management/active-tracking>

<https://www.ghielectronics.com/catalog/product/500>
