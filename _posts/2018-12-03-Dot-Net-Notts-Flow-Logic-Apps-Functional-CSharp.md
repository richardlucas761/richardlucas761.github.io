# Dot-Net-Notts-Flow-Logic-Apps-Functional-C#

[Flow & Logic Apps - Steve Spencer / Functional C# - Simon Painter](https://www.meetup.com/dotnetnotts/events/255664276/)

## Easy integration with Flow and Logic Apps - Steve Spencer

> Historically integrating different systems has been challenging and you have needed experts to help you build even the simplest integration. Microsoft has introduced its Azure based offerings to help take some of the complexity out of integrating to allow you to build your own personal workflows. This talk will introduce both Flow and Logic apps, show you where to use each and how you can migrate from Flow to Logic Apps.

Some of the benefits of using Flow and Logic Apps are having a centralised system which can be used by semi-technical people and integrating into an existing CI/CD pipeline.

Flow and Logic Apps have a drag-and-drop design similar to other technologies such as [ifttt](https://ifttt.com/) with a selection of pre-built connectors for applications like Slack, also the ability to add new connectors for integrating into other systems. It's also possible to integrate with on premise systems through connectors or custom HTTP end points for talking to web services.

These are examples of serverless computing with no specific server or operating system to manage. Flow is part of Office365 and conceptually sits on top of Logic Apps. Flow is aimed at business users with Logic Apps for Enterprise.

Like most automation systems there are various Triggers (on receiving an email) and Actions which take place when the trigger is activated such as saving a file attachment from an email into a OneDrive location.

Steve gave examples of integrations they had created to turn Excel documents into CSV, import CSV documents into a SQL Server database table or generate Open Banking URLs. He also demonstrated how it was possible to integrate with the public food standard scoring API for restaurants, consuming the JSON returned from an external API in response to a call from within a Flow using a custom connector.

A suggested work flow was to create a Flow system as a proof of concept and then export this into a Logic App, pushing it to an existing CI/CD system and being subject to source control. It seemed a little manual but definitely better than having an undocumented and uncontrolled Excel spreadsheet which carries out an integration on a server the IT department only find out about when someone goes on holiday and it breaks.

## Functional C# - Simon Painter

> So you want to get started, putting together Functional code, but you don't have time for the learning curve that comes with F# or Haskell? Or maybe you're fine with them, but the rest of the team isn't ready to follow yet. Whatever the case may be, it's perfectly possible to implement a lot of the amazing features of Functional programming in C#, without the need for any new dependencies, or even any especially complicated code.

> We'll be looking at:
> • What is Functional Programming?
> • What are the benefits?
> • Higher-Order functions - Chaining & Currying
> • Functional program structure
> • Coming features in C#8 - Pattern Matching

I haven't done much Functional Programming (FP) since Formal Methods with Z as part of my undergraduate degree course so it was interesting to hear about Functional Programming in the context of C#. I suppose I have done a little LISP but even that was several years ago.

FP is useful for concurrent and highly critical systems. It's not useful in unpredictable situations. FP is concise, readable, extremely testable, concurrent and robust.

Simon's presentation slides are available on his DropBox <https://twitter.com/madSimonJ/status/1072395611037675520> and he recommended the "F# for fun and profit" website as a good resource.

## Links

### Steve Spencer

<http://blogs.recneps.org/>

<https://twitter.com/sdspencer/>

### Simon Painter

<https://www.linkedin.com/in/simon-painter-45a05217/>

<https://twitter.com/madSimonJ/>

<https://fsharpforfunandprofit.com/>