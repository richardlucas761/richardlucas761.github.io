# Jonathan Relf - Devel-ops: Bringing development practices to operations tasks

<https://www.meetup.com/dotnetnotts/events/263058071/>

> DevOps starts to deliver more value when it moves beyond breaking down team communication walls and the sharing of best practice starts to happen from all sides.

> In this talk, Jonathan Relf discusses how "infrastructure as code" can help you build secure, up to date environments consciously & collaboratively. You will be introduced to some of the methods and tools he has used to automate and test building virtual machines. He illustrates this with his own career journey from a Developer moving into Operations and the benefits these approaches have brought.

Jonathan described how changes in computing have decoupled software development and operations from the physical hardware, from a "data centre" in the corner of an office to cloud based solutions.

In smaller organisations or startup companies each person will be doing all of the development and operations work but as a company grows this develops into separate roles with a wall between them or both develop into silos which don't communicate.

The intention of Agile Engineering is breaking down the wall between the departments or silos. This greater collaboration fits in with Agile generally by involving the people who may block you earlier in the process by making them aware of what you are going to need in advance.

To make it easier to work with larger systems and more importantly create documentation which exists in source control *infrastructure as code* tools can be used to describe and deploy software and systems.

These scripts can be version controlled, form a single point of truth describing a system and could be considered living documentation or "requirements as code".

This can also be needed for regulatory requirements, 3rd party solution uncertainty (other software or systems not under your control), hardening application hosting (limitations on shipping data outside of a country) and avoiding vendor or cloud lock in.

There is a minor caveat for the cloud lock in as each cloud platform usually has it's own unique features and it might be difficult to move everything to a new hosting provider, but made easier by having scripted deployments.

IAC can help build confidence in a Disaster Recovery plan, how difficult will it be to build a system from scratch in the event of a catastrophic failure?

IAC enables change as changes can be routine with less drama and less stress, carried out during agreed scheduled downtime periods.

Staff can spend their time doing *valuable* things rather than repetitive things where minor variations can creep into the system (ask three people to build a new IIS server and there will be minor variations in all three).

Changes defined in code can be carried out unattended but can still be subject to sign off before going into user acceptance or production environments.

## Links

<https://twitter.com/jbjon>