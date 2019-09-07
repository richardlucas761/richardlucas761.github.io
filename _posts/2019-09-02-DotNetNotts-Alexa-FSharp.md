# Alexa.Net with Steve Pears + Writing Business Apps in F# with Ian Russell

<https://www.meetup.com/dotnetnotts/events/263866046/>

## Alexa.net - More than just voice:

> When developers think of using Alexa, they typically think of a device on a shelf being spoken to. They're right - that is the functionality all skills have to have. But what if you already have a great conversation? What else can you offer your users? In this talk we start with an Alexa Skill, a dice roller written in .NET, that already ticks that conversation box and look at enhancing it to offer much more than just speech.

Steve described the wide range of devices with Alexa functionality, from small voice only devices to larger devices with a variety of screen sizes (and shapes). He also described the Alexa.NET NuGet package.

Request flows were outlined and the ability to send progressive responses to let the user know that processing is taking place because delays of even a few seconds become annoying.

By requesting information from the user's profile responses can be personalised. Permissions need to be granted for Alexa skills and the fact a user has *not* given permission for something also needs to be coped with.

Reminders which can be absolute (at 12:00) or relative (in 1 hour's time) can be set up but still need to be confirmed by the user. The Alexa skill won't be certified if you don't handle user confirmation for the setting up of reminders and other things.

Pro-active notifications in response to a fixed list of events can be set up (such as a weather alert).

Push notifications can be sent to a mobile device which is signed into Alexa.

Issues with different screen sizes of devices were described and this is made easier by a new set of responsive controls which deal with this.

Upselling of paid features "you can view the last 10 dice rolls on the dice rolling app for £x" was described although the pricing model meant the actual cost couldn't be included as Amazon guarantee a fixed percentage to the app developer but can discount the price (check this as I might have misheard, it seemed an odd way of charging!)

## Writing Business Apps in F#:

> As you may have heard, F# is great for specialist areas such as finance, scientific research or data analysis but it is also an excellent choice for writing the boring Line of Business apps we work on every day. If you write cloud-ready web apps or cross-platform/mobile apps, then the F# story is very compelling. In this session I will show you how functional programming in F# could help you write apps designed for the rapidly evolving world we live in.

F# has always been a cross platform programming language, for example it's always been possible to run it on Linux using Mono.

For tooling Visual Studio Code or full Visual Studio can be used, JetBrains Rider also has F# support.

C# libraries (such as NUnit) can be used from F# using wrappers, if an existing library exists there is no sense in re-inventing it for F#. It's also possible to write tests for C# code using F# to take advantage of the better named tests using English strings rather than *CustomerBuysSomething* style naming.

Domain modelling of a set of BDD / Specflow requirements using F# was described, showing the parity with C# and other languages.

F# has a data load function to import CSV files and work out the types of the data elements on the fly, which seemed pretty impressive.

.NET Core makes it easier to write web apps and web APIs using F#, also using tools and wrappers like the Giraffe wrapper and Saturn MVC framework.

<https://github.com/giraffe-fsharp/Giraffe>

<https://saturnframework.org/>

Also the Paket tool but probably more reading needed as I don't understand how this provides more functionality than standard NuGet?

<https://github.com/fsprojects/Paket>

Other tools were discussed including the Fable F# compiler:

<https://fable.io/>

The Elmish library which works like React:

<https://github.com/elmish/elmish>

The following project on GitHub gives an introductory dojo on developing full stack web applications using F#.

<https://github.com/CompositionalIT/SAFE-Dojo>

Also the Fabulous system which can be used with Xamarin Forms:

<https://fsprojects.github.io/Fabulous/>

## Links

<https://twitter.com/StevenPears>

<https://twitter.com/ijrussell>