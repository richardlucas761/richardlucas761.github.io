# [Nottingham PowerShell user group October Meeting](https://www.meetup.com/Nottingham-PowerShell-UserGroup/events/254881983/)

## Serverless by Jaap Brasser

> A practical session on how we can move our existing code to the Cloud. What can be re-used? Which code should we leave in our existing silos?

> These questions will be answered in this session focussed on what Serverless means for our PowerShell code. The approach we will take is as follows: we will take our existing code and transfer into Serverless code using Azure Functions; we evaluate changes or optimizations to take into account and how can we maximize the benefits of using Serverless.

Jaap presented information on [Azure Automation](https://azure.microsoft.com/en-us/services/automation/) and [Microsoft Flow](https://flow.microsoft.com/en-us/) which has a set of connectors, plug-ins, approval flows and event triggers so similar to other work flows like [Zapier](https://zapier.com/) or [ifttt](https://ifttt.com/).

Also [Azure Functions](https://azure.microsoft.com/en-us/services/functions/) for Severless computing and [Azure Web Apps](https://azure.microsoft.com/en-us/services/app-service/web/) to have an abstract infrastructure.

As this was a PowerShell meetup the emphasis was on creating new Azure Functions and being able to re-use existing skills and existing code, have faster deployments with less maintenance.

Version 2 of Azure Functions doesn't support PowerShell yet but it's possible to enable _experimental languages_ to use PowerShell.

You can specify Environment Variables for functions which seemed odd because the functions aren't running on a server?

Jaap made the point that efficient functions are key here due to the charging model based on time of execution; we want functions that run as quickly as possible. It's possible to upload your own functions to Azure via FTP.

## Azure DevOps - What is it? What can I do with it? Where Do I Start? How can I use it in PowerShell Scripting by Ryan Yates

> In this session I will cover features and functionality of Azure DevOps (formally Visual Studio Team Services) and how these components can help you in both IT Pro & Developer workloads.

> Whilst this is more an introductory session however I will demo out some personal workloads that I have using the Azure DevOps Platform with integration with Github and how this as a platform can accelerate your own personal PowerShell development

[Azure DevOps](https://azure.microsoft.com/en-us/solutions/devops/) is the new name for VSTS, not a DevOps tool but it can be used to automate many things.

Ryan described DevOps as a mixture of tools and processes, a way of life rather than a specific tool or tools with the benefit of faster releases of software to customers (internal or external).

Parts of the process are CI (Continuous Integration), CD (Continuous Deployment) and Learning and Monitoring tools.

[Azure Boards](https://azure.microsoft.com/en-us/services/devops/boards/) were mentioned to help manage work, I haven't used Azure Boards but I have used [JIRA](https://www.atlassian.com/software/jira) and the tool formerly known as [Rally](https://www.ca.com/us/products/ca-agile-central.html) for planning and tracking work of Agile teams.

[Azure Pipelines](https://azure.microsoft.com/en-us/services/devops/pipelines/) is the equivalent of CI/CD tools I've used before like [Jenkins](https://jenkins.io/) or [Team City](https://www.jetbrains.com/teamcity/features/) and I was impressed by the ability to write pipeline steps in a variety of languages (not just Groovy) and define scripts in YAML.

[Azure Repositories](https://azure.microsoft.com/en-us/services/devops/repos/) were mentioned, a private Git repository with the ability to carry out a semantic search of code in the repository, also web hooks to call Azure Functions to automatically post information to Slack for example.

## Links

### General

[Azure Automation](https://azure.microsoft.com/en-us/services/automation/)

[Azure Boards](https://azure.microsoft.com/en-us/services/devops/boards/)

[Azure DevOps](https://azure.microsoft.com/en-us/solutions/devops/)

[Azure Functions](https://azure.microsoft.com/en-us/services/functions/)

[Azure Pipelines](https://azure.microsoft.com/en-us/services/devops/pipelines/)

[Azure Repositories](https://azure.microsoft.com/en-us/services/devops/repos/)

[Azure Web Apps](https://azure.microsoft.com/en-us/services/app-service/web/)

[ifttt](https://ifttt.com/)

[Jenkins](https://jenkins.io/)

[Microsoft Flow](https://flow.microsoft.com/en-us/)

[Rally](https://www.ca.com/us/products/ca-agile-central.html)

[Team City](https://www.jetbrains.com/teamcity/features/)

[Zapier](https://zapier.com/)

### Jaap Brasser

<https://www.jaapbrasser.com/>

<https://twitter.com/jaap_brasser>

### Ryan Yates

<https://blog.kilasuit.org/>

<https://twitter.com/ryanyates1990>