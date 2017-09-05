[TECH NOTTINGHAM SEPTEMBER 2017: DEVEL-OPS: BRINGING DEV PRACTICES TO OPS TASKS](https://www.meetup.com/Tech-Nottingham/events/242558043/)
*by [Jonathan Relf](https://twitter.com/jbjon)*

> The platform you choose to run your software on is a key part of how secure your solution is.
> During the first half of the evening Jonathan will discuss how "infrastructure as code" can help you build secure, up to date environments consciously & collaboratively. You will be introduced to some of the methods and tools he has used to automate and test building virtual machines and the benefits he's learned through the process.
> The second half of the evening will see a practical session where you can have a go at creating your own virtual machine build pipeline, putting into practice what we learned in the first half.

This was a very busy session and a great introduction to concepts such as *Infrastructure As Code* and *Agile Engineering*.

*Agile Engineering* was described as a more collaborative way of working with less of a defined split between the *Development* and *Operations* sides of Dev Ops but still leaving room for specialisation.

Background was given to the problem which scripted deployments were going to help solve, the fact that manual server setups usually result in slight variations; no two installations of IIS on a server are ever completely alike, perhaps a different set of firewall ports have been left open or there is a slightly different patch level for some important software service or package.

Further background described how "server rooms" have progressed in some organisations from *Physical* hardware to *Virtual* machines possibly still running on that old physical hardware to *Cloud* based servers which are no longer on premise. This can be thought of as reliable software running on unreliable hardware. The real world example of Netflix killing deployed instances which didn't meet performance criteria (remember that it's someone else's computer) was a good example.

*Infrastructure as code* was described as necessary in the Cloud environment due to:

* regulatory issues which weren't as much of a problem when the servers were owned by the company
* issues with third party images used for server installations or software installations, just *which* version of PHP was being used as the default installation by your cloud provider?
* this also gives the opportunity to 'harden' deployments by mandating *exactly* what gets installed onto the server: a specific version of Ruby with specific additional packages, a specific set of firewall ports.
* also the issue of vendor lock in, if your cloud provider decide to increase their charges do you have any choice but to just accept this, or could you move to a different provider?

This also gives the opportunity to treat deployed servers and the things running on them as cattle rather than pets; don't get overly attached to deployed instances and consider any of them as something which could be terminated at very short notice.

Having a scripted and *repeatable* deployment process leaves people free to concentrate on valuable tasks rather than carrying out boring repetitive tasks.

A set of deployment scripts in *source control* also become valuable living documentation which both describe the current state of the deployed system but also giving a version history of changes which were applied. This also helps with issues of decaying knowledge with very complex systems and issues because X is on holiday and X is the only person who knows how system Y is put together on the live server. Even if this is just a batch file or a shell script this is a step in the right direction towards having a documented and repeatable process.

The ability to carry out *automated tests* to ensure what was built was what we were expecting was very interesting. Being able to check the correct version (and patch level) of Windows Server was installed, IIS was set up as expected and the necessary firewall ports were opened would be very useful and prevent even more tedious GUI clicking to find out whether a deployment was as expected.

**Links**

[Jonathan Relf](https://twitter.com/jbjon)

[Infrastructure as Code - Managing Servers in the Cloud](http://shop.oreilly.com/product/0636920039297.do)
