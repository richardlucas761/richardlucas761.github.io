# [Nottingham PowerShell Meeting - June 2018](https://www.meetup.com/Nottingham-PowerShell-UserGroup/events/250934743/)

## Building Better Bricks: Module design and development best practice by Chris Gardner

> There are a number of ways to design and develop a PowerShell module but each has its pro's and con's. This talk will look at the main approaches that are used, common pitfalls, and some of the best practices that should be used to make developing the module as low effort as possible, with a look at how this can then be extended to make publishing the module easier.

Chris's talk made some interesting points about PowerShell script design and further to the previous session all of the ideas of writing Pester tests first and structuring scripts so they are maintainable was very familiar to me as a C# developer.

I wasn't previously aware of the ability to combine scripts into a single file for deployment or tools like PSDepend to package PowerShell dependencies for deployment to machines without internet access.

The VSTS build actions demonstrated with code coverage (_script_ coverage?) metrics piped into SonarQube were also interesting, a set of graphs to hopefully see code coverage increase over time.

## Introduction to PowerShell testing and Pester by Stuart Moore

> How do you make sure that scripts keep doing things correctly when you add new features? Or even that they really do what you set out to do?

> The answer is testing!

> Pester is a PowerShell testing framework written in PowerShell. In this session we'll take a look at how to test your scripts, why putting the effort in early pays dividends later on, what you should be testing and how the way you design and write functions can help (or hinder!) easy development.

As mentioned earlier it was good to hear it was possible to carry out script development using TDD and Stuart demonstrated creating failing unit tests which checked whether the script existed at all. Building on this with checking for whether the expected function existed in the file to more comprehensive tests checking both the parameters into and the expected output from the function under test.

I didn't know that Pester had the ability to Mock objects to make it possible to test scripts with dependencies (where the intention is the dependencies should not be checked themselves) and use canned data, this again is familiar from writing C# unit tests.

## Links

[Stuart Moore](https://twitter.com/napalmgram)

[Chris Gardner](https://twitter.com/HalbaradKenafin)
