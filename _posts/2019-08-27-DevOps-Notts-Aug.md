# DevOps Notts August

<https://www.meetup.com/DevOps-Notts/events/262473868/>

## William Ellwood - Site Reliability Engineer, GoDaddy

> Test Driven Infrastructure using Molecule and Ansible.

Will described three different scenarios in the situation where a disaster had happened and a data centre needed to be rebuilt.

1. No scripting at all, everything needs to be rebuilt and then tested manually.
2. Scripted deployment where servers are built automatically but not automatically tested.
3. Scripted deployment with scripted tests to ensure what has been built is in fact what was expected.

The tools used to carry out the scripting of both build and test aren't important but the main ones are Ansible, Puppet or Chef. Each of these tools have a testing suite which is appropriate to that platform.

Testing scripts are important because they capture intent and form documentation of a system, how a system should be set up. These scripts can be thought of as a testable hypothesis for server configuration.

## Tom Hoyland - Agile Delivery Lead from Sky Betting and Gaming

> Building and growing an Agile team with DevOps mindset and a clear purpose to create a squad with an infectious, high performing culture.

Tom described his experiences of setting up a login and registration team at Sky Betting loosely following the Spotify model.

A set of metrics were collected but the details of these were hidden from the team as they were trying to avoid the observer effect and hopefully prevent the distortion of good behaviours.

They worked on their backlog at first and understood where new features were coming from (some of them seemingly appearing out of nowhere!)

They realised they have multiple backlogs and multiple entry points into their own backlog, this was simplified into a single larger backlog which helped them have better conversations about priorities and business value for features.

The team was built up of people who had different experiences of Agile so they took a back to basics approach to create their own version of Agile, carrying out bootcamp training sessions to create a culture which would enable growth.

They also kept teams together as having people hopping between teams made it difficult to estimate, specific smaller teams which worked together better and produced more predictable results.

Using Scrum they stripped out job titles to encourage co-creation and give a sense of shared responsibility. Anyone working in a heavily regulated industry might take exception to this as testers need special training so a tester is always a tester, it depends on the industry.

Like most firms they realised they were working in an Agile -> Waterfall environment when it came to putting systems into production, they discovered they had new work which hadn't already been included into their backlog and started having conversations with potential blockers earlier.

They concentrated on automating the boring parts of the process and building up the team rather than the tooling.

## Links

<http://www.devopsnotts.co.uk/>

Tom Hoyland <https://twitter.com/thatagile>