# Stuart Moore - Connecting Business Apps with Azure Logic Apps & Service Bus

<https://www.meetup.com/dotnetnotts/events/262027858/>

> As more and more systems are split onto disparate systems connection them altogether has become a real head ache. Either suppliers want money to modify their systems or developer time has to be wasted writing bespoke code every time something new comes along. Using Azure Logic Apps and Service Buses we can quickly build scalable reliable connection between systems with the ability to scale on demand, pause data flow whilst still queuing it and replay for testing or fault finding.

Stuart outlined some of the reasons why service buses are useful as companies have too many systems to integrate and need flexibility to re-wire systems when making changes.

The example of university clearing was given as a busy situation where spikes in requests would be encountered and a queue of requests on a service bus is a way of dealing with these extra requests, non essential queue items can be parked until later to keep essential systems running.

## Logic Apps

Azure Logic Apps are serverless functions which have a low execution cost although they don't execute in realtime unless you spend more for premium services. The advantage of these being on the Azure platform is that Microsoft carry out the scaling of systems for you.

Logic apps trigger on a variety of events in applications, similar to IFTTT.

It's possible to talk to on-premise systems using the Integration Gateway system, to access the file system on a existing system for example.

## Azure Service Bus

Azure Service Bus is a pay-as-you-go enterprise service bus, I haven't worked with this myself but I have some brief experience with Tibco service buses a few years ago.

Azure Service Bus uses an open messaging format which has a few minor constraints on headers which need to be included but is otherwise free-form.

The recommendation is to not pass large files (images, binary objects) on a service bus but to dump these to storage and pass _references_ to these large objects on the service bus instead.

Queues and Topics are available to segment data, you subscribe to a topic which is a sub-set of the messages in a queue or all of them, depending on the filtering criteria defined.

Service Bus Explorer is a free desktop tool for accessing service bus queues.

## Links

<https://stuart-moore.com/>

<https://twitter.com/napalmgram>

<https://www.linkedin.com/in/stuart-moore/>