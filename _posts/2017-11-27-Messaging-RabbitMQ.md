[Dot Net Notts 27 Nov](https://www.meetup.com/dotnetnotts/events/242325991/)

# Automated testing for developers (using Selenium)

John Staveley [@johnstaveley](https://twitter.com/johnstaveley)

> Message queuing is becoming an essential part of modern architectures and essential for asynchronous architectures and microservices. In this session will be described the benefits of messaging systems, the software solutions that are available and typical messaging architectures. Examples will be made using Azure Storage Queues, Azure Service Bus and RabbitMQ. This talk is primarily about messaging, however as this session is for tech hipsters, the demos will be done giving an extensive introduction to Azure functions, Azure Resource Manager Templates, .Net Core and Docker.

John's presentation was introducing Rabbit MQ, messaging and distributed work loads. In the context of work I've previously done message queues can help with threading microservices together.

The code for the presentation is here on GitHub [johnstaveley/MessagingPresentation](https://github.com/johnstaveley/MessagingPresentation).

The [slides](https://www.slideshare.net/johnstaveley/messaging-rabbitmq-azure-service-bus-docker-and-azure-functions) are here.

## Azure Storage Queues

(See also AWS Lambda's)

Azure Storage Queues are functions as a service, serverless bits of code with an event / trigger and some code to execute in the event of the trigger firing, with bindings to data.

There is a limit of 5 mins processing time so they might not work in all cases.

## Azure queue options

There are several Azure options for queues in increasing order of complexity

* Azure Queues
* Azure Storage Queues
* Service Bus Queues
* Event Hubs

## RabbitMQ, Docker, .NET Core & Kitematic demonstration

RabbitMQ implements the standard [AMQP](https://www.amqp.org/). The demonstration was using the [EasyNetQ](http://easynetq.com/) wrapper to make it easier to work with in C#.

## Docker Build Container

Building the Docker image for the RabbitMQ queue applications using a specific version of .NET Core Build to stop "works on my machine" issues.
