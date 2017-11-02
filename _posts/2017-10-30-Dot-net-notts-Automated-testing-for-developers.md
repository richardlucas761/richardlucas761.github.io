# Dot Net Notts 30 Oct

## Automated testing for developers (using Selenium)

Alan Swan @ Tribal <http://www.tribalgroup.com/>

# Introduction

The intention is to create *repeatable* cross browser tests to give more confidence in produced code.

# Selenium IDE

<http://www.seleniumhq.org/projects/ide/>

Selenium IDE is a GUI to create testing scripts by carrying out actions on a web page which are then recorded.

The IDE has the option to export the testing steps as Selenium actions which can be used in the Selenium Web Driver.

The benefit of the IDE is that no programming experience is needed to create tests.

Unfortunately an update to Firefox has broken the IDE so usage has dropped.

# Sideex

<http://www.sideex.org/>

The Sideex website describes this as the "Starting point for developing the next generation of Selenium IDE".

Available for both Chrome and Firefox but not in the Firefox Add-Ons store yet for Firefox 55+ (<https://wiki.mozilla.org/Quantum>) so has to be installed and updated manually. An earlier version is available for older versions of Firefox.

# Selenium Web Driver

<http://www.seleniumhq.org/projects/webdriver/>

Selenium was used to create automation tests using a unit test project in Visual Studio as it's familiar. It doesn't actually matter where the Selenium Web Driver is run from.

Web Driver methods use Xpath or Attribute Decorators / Page Objects to find elements on the page to interact with.

The Selenium Web Driver is available on NuGet. <https://www.nuget.org/packages/Selenium.WebDriver>

# Selenium Standalone Server

<http://docs.seleniumhq.org/download/>

For remotely running the Selenium Web Driver

# Selenium Grid

<http://www.seleniumhq.org/projects/grid/>

Scaled up testing for multiple instances of the Selenium Standalone Server; makes load testing possible.

# Cucumber / Gherkin / SpecFlow

<https://cucumber.io/>

Touched on Behavioural Tests for describing features and work flow.

# VSTS

<https://www.visualstudio.com/team-services/>

c.f. Team City and Jenkins

Source control in Git

MS recommend using Git for new projects?

Simple to create new deployment actions using templates, moved the test assembly to after the build in this case because it was a post-build automation rather than unit tests.

Tests and Feedback extension looks useful for easily creating bugs with a screenshot and some context.

# Summary / Questions

Issues with running automation tests for every build due to time constraints, takes a long time to automate and wait for websites to respond.

Can alleviate speed problems with Selenium Grid or parallel tests.

Dev + Test collaboration, working together to create automated tests that cover requirements and that also make sense. Dev and Test different mind sets so work together.

Automation makes tedious regression testing which has to be repeated for every software release easier, just work on creating new tests for new requirements.

HTTP Mock, able to test the scaffolding of the website without having to actually spin up the full website.
