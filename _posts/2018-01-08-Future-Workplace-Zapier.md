# [Tech Nottingham 8 Jan 2017](https://www.technottingham.com/events/tech-nottingham-january-2018)

## Workplace Of The Future by Mark Phelps

> "In this talk Mark discusses how more collaborative and mobile working is changing the face of the physical workspace and the effect it is having on human interactions."

Mark's talk was about the future of the workplace; describing the evolution of IT organisations from single developers working in closed environments to more collaborative, Agile teams with greater mobility and flexibility. Modern IT firms are Agile rather than monolithic and not afraid to fail.

An interesting and perhaps controversial comment was that _automation_ has provided all of the benefit it can. The key now is _collaboration_.

Before collaboration can be achieved there are issues with communication tools as the current tools are both complicated and fragmented.

Mark estimated there were 50+ methods of contacting him so which one should someone use?

According to statistics presented most employees aren't using the majority of corporate communications or are working round them which might cause a problem with upcoming GDPR regulations.

This also poses a problem for companies trying to support communication methods customers or partners want to use where there is a rapid pace of change in tools or perhaps conversely a slow development process! Consider also new tools like bots, AI, IoT, Mobile first websites or Virtual Reality.

## Prometheus: Automated Outage Detection At Zapier by Rob Golding

> "Zapier makes hundreds of millions of outbound API requests every day. When a service starts to fail, we need to know about it quickly so we can prevent our infrastructure from crawling to a halt. This talk explores the development of Prometheus, the tool we use to detect API issues at scale."

Rob's talk was about an internal tool developed at Zapier called Prometheus (written in Python). I hadn't heard of Zapier before but their workflow automation platform reminded me of [IFTTT](https://ifttt.com/).

Zapier interface with ~1000 different APIs and have a scheduler which puts jobs onto a Rabbit MQ queue to be processed (_see also my previous blog post about Rabbit MQ_). Each of these jobs having an interaction with one of the ~1000 APIs which Zapier supports.

Their issue was with these APIs being broken, running slowly or being intentionally offline for maintenance and how they cope with this with as little impact on customers as possible.

Before each of the queued jobs executes their internal tool Prometheus is called to check whether the targetted API is functioning normally based on simple average response time criteria. If the API is considered to be down request polling is reduced to 10% and any writes to APIs are delayed. Any responses from push type web hooks are also queued to be processed when the API is working again.

To prevent Prometheus from being a single point of failure its considered to be a non-critical system with very low timeout values, if a response isn't received from Prometheus polling just continues normally. Prometheus is monitored by [Data Dog](https://www.datadoghq.com/).

When the API is responding normally again polling goes back to 100% although Rob pointed out the limitation of using HTTP requests here to indicate the service is back to normal when a response isn't required. They would like to replace this with a _fire and forget_ UDP call perhaps.

As a side benefit of collecting this response time data Zapier are able to display public metrics or warn customers when a specific API may be having issues when they are attempting to create a new workflow, also displaying information on their [Status Page](https://www.statuspage.io/).

## Links

[Rob Golding](http://twitter.com/robgolding63)

[Zapier.com](https://zapier.com/)

[Status Page](https://www.statuspage.io/)

[Data Dog](https://www.datadoghq.com/)

[IFTTT](https://ifttt.com/)

[Mark Phelps](http://twitter.com/markp894)

[Node4](https://www.node4.co.uk/)
