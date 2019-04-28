# Azure Global Bootcamp Nottingham 2019

On Saturday 27 Apr 2019 I attended the first Azure Global Bootcamp event in Nottingham at the Commify/Esendex offices.

These are my very rough notes from the sessions which were a mixture of presentations and practical sessions.

---

## Session 1 - SQL Server in Azure - Stuart

> Azure offers a range of SQL Server options from simple PAAS solutions up to as complex an infrastructure as you want using IAAS. With all these options there are benefits and downsides.

> But where are the sweet spots?

> In this session we’ll look at all he options, look at the pros and cons of each, and how to get the best of them. The guiding principle will be to look for the simplest solution to the problem, leaving you free to get on with the important stuff.

### SQL database (db not server) extended by elastic pooling

A SQL database on Azure is the simplest option, this is not a traditional SQL server but a single public (firewalled) database. Each database is attached to a server, you can re-use an existing server or create a new one.

Full backups are taken every 24 hours, log backups every 5 mins so it's possible to restore a database to a point in time.

For High Availability the Premium option has better failover. The Basic option cold starts on a new compute node and takes longer to spin up.

You can use Elastic Pool to share DTU/vCores across databases, can have 50 for all databases globablly, only need 50 at a time rather than buying 100 for two. Elastic DTUs are 1.5 the cost though. This could be an option if you have two systems which aren't being used at the same time.

You have to use elastic query to cross query databases, can create external data source and external table to work round this, probably one of the most obvious differences that although the databases are on the same server it isn't possible to directly access them from each other. The standard "use" statement doesn't work, you're only connected to one database and can't change.

Similarly no cross database transactions are possible. There are also no SQL Server Agent jobs, elastic jobs or azure functions are used instead.

### Azure SQL Managed Instances

99% of on premise features are present in a managed instance, effectively a private virtual SQL Cluster.

This version has a SQL Agent but has no SSIS, SSRS or SSAS -> Data Factory, Power BI, Azure Analysis Services are the replacements for these on Azure.

Private IP endpoints rather than public, can be routed to via ExpressRoute (On Prem to Azure VPN). Can also set up a public end point if you want.

Can upload database backups to Azure and restore them to a managed instance.

### Azure VMs with SQL Server

100% the same as an on premises instance but sat in Azure. More configuration needed.

### Chosing between these options

Features needed, do you have DBAs, costs?

The DBA role is still needed for setting up resilient services, disaster recovery planning, tuning -> same as development changes which reduce Azure spending.

### Azure data studio

This is a new tool which is like the Visual Studio Code equivalent of SQL Server Management Studio, it doesn't currently support traditional SQL Server things like SQL Server agents but is a lighter weight version of SSMS.

---

## Session 2 - Service Fabric Hands On - Simon Dale, BJSS

> Microservices, Orchestration, Deployment and Scale!

<https://github.com/simondale/>

Service fabric, c.f. Open Shift / Kubernetes.

---

## Session 3 - Azure IoT PaaS vs IoT Central SaaS - Julian Sharp

> This session will explore the differences between Azure IoT PaaS service (IoT Hub, Stream Analytics, TSI, DPS etc) and Azure IoT Central, a new IoT SaaS solution

### Azure IoT PaaS

The IoT Hub is used for comms between device and cloud. Hub Device Provisioning service is used for roll out.

IoT Edge moves processing to device rather than cloud, talk to cloud when needed, install machine learning or a container into device.

Stream analytics, monitoring data from devices, for insights and query data in motion, put machine learning into analytics.

Time Series insights, data prep and visual display, post data analysis.

Azure Device Explorer to see physical devices.

#### Azure IoT starter kits

MXChip, teXXMmo, Raspberry PI.

#### IoT Sphere

Dedicated hardware device and OS.

#### Azure IoT Workbench

Visual studio device simulators.

#### IoT Solution Accelerators

Template PaaS deployments, cover common business scenarios.

### Azure IoT Central SaaS solution

Free for first 5 devices with Azure subscription. No dev talent needed, easier to set up. Set up rules and actions which are triggered rather than having to hand roll steps yourself. Start with IoT Central and move to IoT hub later.

---

## Session 4 - Azure IoT Hubs with Raspberry PI and Node.js - Pete Gallagher

> This workshop based session takes attendees from start to finish through connecting a Raspberry Pi to Microsoft Azure IoT Hubs.

> I take the user through the basics of IoT, Microsoft’s Azure offering and basic electronics where we build a simple circuit with a couple of LEDs, a button and a Temperature Sensor.

> We cover everything from how to create a Basic IoT hub, connect a Raspberry Pi up to a circuit, add the parameters to the template code and see our first interaction between the Pi and the IoT hub.

> We’ll also walk through Device Twins and Azure Functions showing how to send a tweet when the room temperature drops below a certain level.

<https://github.com/PGallagher69/iothubs_with_raspberry_pi>

---

## Session 5 - PDFs at Scale in Azure - Daniel Edwards & Luke Billington

> A quick overview of how we tackled generating large amounts of PDFs in Azure

<https://github.com/dantheman999301/gabc-browserless>

Past PDF generating solutions usually expensive or painful.

HTML skills are known, don't need to learn a new formatting language.

Puppeteer node library for talking to headless chrome.

Browserless wrapper for Puppeteer, exposes functionality as set of end points.

Browserless runs in Docker (on Ubuntu only?)

Forked a version to refactor Browserless to suit their purposes, contributed to the open source tool to improve it.

Could either base64 encode the images or if the worker machines are going to stay alive and the images are constant could benefit from having the images cached.

### Azure setup

POST into service bus, pushed to internal service bus, internal service bus farms work out to chrome farm, write to blob storage.

GET end point to check whether the PDF is ready.

End points are Azure functions.

More RAM and CPU gives faster PDF generation

Horizontal scaling for concurrency can help, test and tweak.

Can use the chrome headless machines for Selenium testing when they are not generating PDFs, visual testing also perhaps?

### Others

AthenaPDF, not well supported? No CSS3 support?

JSReport, cheaper option for lighter workloads.

---

## Azure Bootcamp 2019 Science lab

<https://github.com/intelequia/GAB2019ScienceLab>

## Lab Key

GKM-DKT-NPO

## Lab Team

NottsBootCamp

---

## Links

<https://global.azurebootcamp.net/>

<http://www.nottsdevworkshop.co.uk/azurebootcamp/>