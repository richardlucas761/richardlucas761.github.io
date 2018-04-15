# [Nottingham PowerShell user group April 2018](https://www.meetup.com/Nottingham-PowerShell-UserGroup/events/247733243/)

This month's meetup was two sessions with Rob Sewell talking about both Pester tests in PowerShell and Continuous Delivery using VSTS.

As an aside there were some technical problems with a broken screen so everyone was introduced to the new screen sharing feature in Windows 10 so we could still see the presentation through a second laptop screen.

We also discussed the issues of setting up a new workstation and being able to restore existing settings (along the lines of the Vagrant tool) using this tool [https://chocolatey.org/](https://chocolatey.org/).

## Session 1: Introduction to Pester

> Start from nothing and use Test Driven Development to write a PowerShell function that uses the Microsoft Cognitive Services API to analyse pictures. I will take you on a journey from nothing to a complete function, making sure that all of the code works as expected, is written according to PowerShell best practices and has a complete help system. You will leave this session with a good understanding of what Pester can do and a methodology to develop your own PowerShell function

Pester is a unit testing framework for PowerShell, the first thing that struck me is how familiar all of the features were given my mostly C# background:

* Creating mocks in your tests
* Outputting test results into NUnit format to be consumed by a further tool
* Using TDD principles to write your tests first before you've written any PowerShell

A related tool of having a PowerShell [script analyser](https://www.powershellgallery.com/packages/PSScriptAnalyzer/1.16.1) (see also lint tools) also feels familiar and is embeddable into Pester to ensure PowerShell code is "good" script. This also reminded me of a previous session on Sonar Qube.

## Session 2: Continuous Delivery for your Module - Put your PowerShell modules in the gallery with just a commit.

> An introduction session to show you how YOU can deploy your PowerShell module to a PowerShell Gallery (public or private) automatically.

> In this fast paced demo heavy session we will

> - Use Plaster to create our module framework
> - Use GitHub for Version Control
> - Use Pester to develop our module with TDD
> - Use VSTS to Build, Test (with Pester) and Release our changes to the PowerShell Gallery

> Within 45 minutes you will have the tools that you require to continuously deliver changes safely to your published PowerShell module for the consumption of others

I've used TFS but I've never used VSTS (I've used Jenkins and Team City in the past) for Continuous Integration or Continuous Deployment so this was a useful introduction.

We were introduced to the **Plaster** templating tool to make it easier to submit new modules to the PowerShell gallery which felt very similar to NuGet.

The workflow we were shown was running Pester tests, creating XML output of running the tests which were then parsed by VSTS to give stats on the number of tests failing and etc.

During the presentation we were given a live demonstration of fixing a bug in the DBA Checks PowerShell module and deploying a new fix to the PowerShell gallery.

# Links

[Rob Sewell on Twitter](https://twitter.com/sqldbawithbeard)

[Rob Sewell website](https://sqldbawithabeard.com/)

[Powershell script analyser](https://www.powershellgallery.com/packages/PSScriptAnalyzer/1.16.1)

[https://chocolatey.org/](https://chocolatey.org/)
