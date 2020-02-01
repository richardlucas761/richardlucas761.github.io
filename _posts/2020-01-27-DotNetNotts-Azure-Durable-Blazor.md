# Dot Net Notts January 2020

<https://www.meetup.com/dotnetnotts/events/267036938/>

## Oliver Tomlinson - Azure Durable Functions

> Durable Functions is an extension of Azure Functions that lets you write stateful functions in C# or JavaScript in a serverless compute environment.

> Having developed and maintained software that utilises Durable Functions in production for almost a year at Esendex and Commify, I will reflect on this journey and provide some insight into what worked well, what didn't, and what challenges one might face when adopting Durable Functions.

Azure Durable Functions build on Azure Functions to provide tolerance for failure by design whilst working with a volatile cloud platform.

Azure Functions can be used to achieve:

1. Function chaining using durable orchestration.
2. Fan out / fan in (think Map Reduce) and the same durable orchestration concept across multiple instances.
3. Long running process pattern (async HTTP) where it's possible to check the status of a task and return a response payload when completed.
4. _I think I missed number four!_
5. Human Interaction Pattern where we are waiting for external events which take a longer time to complete, manual processes.

All of these take advantage of the abstraction provided by durable functions, less implementation needed.

Durable functions are scalable but only if you follow the coding and design rules. Make processes deterministic, don't perfom any I/O, no resource intensive processes, no I/O bindings and make processes idempotent.

Durable functions can be run in a container on AWS and etc. but you still need an Azure storage account and need to invest in Kubernetes for scaling.

Oliver mentioned v2 of Durable Functions but didn't consider this ready for production at the time of writing.

## Chris Sainty - Blazor

> Blazor lets you build interactive web UIs using C# instead of JavaScript. Blazor apps are composed of reusable web UI components implemented using C#, HTML, and CSS. Both client and server code is written in C#, allowing you to share code and libraries.

> Blazor is a feature of ASP.NET, the popular web development framework that extends the .NET developer platform with tools and libraries for building web apps.

<https://github.com/chrissainty/Talks-BuildingNextGenAppsWithBlazor>

Most of Chris' talk was live coding examples but he described Blazor as a component based framework for building UIs although Server, Web Assembly and even Desktop and Mobile (building on Xamarin Forms) flavours of Blazor are coming soon.

Chris used the same "feature folders" set up for his solution as seen in a previous DotNetNotts talk where all of the classes for a single business feature were together rather than being grouped by their purpose.

Blazor was described as not opinionated and with hot swappable modules.

Chris described how Blazor could be used to wrap existing JS libraries and then interact with those libraries using C#.

## Links

<https://twitter.com/dotDestroyer>

<https://twitter.com/chris_sainty>