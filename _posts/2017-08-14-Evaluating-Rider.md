# Evaluating Rider, initial thoughts

I've been trying out the new Cross-platform .NET IDE from JetBrains and these are some initial thoughts and observations.

## Minor SVN issues (not Rider's fault!)

I had a minor issue with Subversion integration in Rider as I'm using Tortoise SVN and hadn't installed the SVN.EXE because I only ever use the GUI version.

It was simple to fix by downloading the installation package for Tortoise SVN and running a "Modify" installation to install the missing SVN.EXE; there is a StackOverflow article in the links section which helped me out.

## It's quite slow

It's a bit of a shame since I'm guessing most people will consider using it because Visual Studio is very resource hungry but Rider is noticeably slower than Visual Studio on starting up and when loading very large solutions, hopefully it will improve in later versions.

## It doesn't understand .RESX files

I have an application with a series of SQL scripts in a .RESX file and the file is just displayed as XML, maybe I just shouldn't be using .RESX files any more?

There is a small toolbar displayed to open the XML file in Chrome, Firefox, Safari, Opera or IE which is a little odd, I don't have two of those browsers installed so it seems strange to offer me the option to open the file in these browsers?

Admittedly, the Visual Studio RESX file editor is pretty crude but it's better than looking at raw XML.

## It works

Despite these minor issues it works fine with a fairly hefty solution, I'll see how it works out over the 30 days evaluation period.

**Links**

<https://www.jetbrains.com/rider/>

<https://stackoverflow.com/questions/2967176/where-is-svn-exe-in-my-machine>

<https://tortoisesvn.net/>
