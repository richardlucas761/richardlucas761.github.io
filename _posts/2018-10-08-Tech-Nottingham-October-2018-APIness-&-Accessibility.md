# [Tech Nottingham October 2018: APIness & Accessibility](https://www.meetup.com/Tech-Nottingham/events/254754472/)

## 

## Life, Liberty And The Pursuit Of APIness: The Secret To Happy Code by Dylan Beattie

> We spend our lives working with systems created by other people. From the UI on our phones to the cloud infrastructure that runs so much of the modern internet, these interactions are fundamental to our experience of technology - as engineers, as developers, as users - and user experiences are viral. Great user experiences lead to happy, productive people; bad experiences lead to frustration, inefficiency and misery.

> Whether we realise it or not, when we create software, we are creating user experiences. People are going to interact with our code. Maybe those people are end users; maybe they're the other developers on your team. Maybe they're the mobile app team who are working with your API, or the engineers who are on call the night something goes wrong. These may be radically different use cases, but there's one powerful principle that works across all these scenarios and more - and it's called discoverability.

> In this talk, we'll draw on ideas and insight from user experience, API design, psychology and education to show how you can incorporate discoverability into every layer of your application. We'll look at some real-world systems, and we'll discuss how how discoverability works with different interaction paradigms. Because, whether you're building databases, class libraries, hypermedia APIs or mobile apps, sooner or later somebody else is going to work with your code - and when they do, wouldn't it be great if they went away afterwards with a smile on their face?

Dylan's talk was about Happy versus Sad Code and having systems which are "Discoverable" (capable of being explored to learn how they work) and learning curves for new software. The example of learning ASP.Net Web Forms and finding out the web doesn't work that way was given where you learn a certain amount and then have to go back to the beginning again.

The error messages given by Castle Windsor where common errors describing what the user can do to fix them were a good example. A comparison was made between the DOS prompt (not discoverable, RTFM) and the Mac OS Gui (discoverable).

The concept of **Information Radiators** was presented (I've written a few of these myself) which can help with the business perception of the current state of supported systems by having a small number of indicators displayed on a screen in a communal area.

Tracing, metrics and logging are important and need to be built into a system from the ground up, not added later as an afterthought. The ability to turn on tracing in a production **Nancy** website was presented, impressive that this could be configured through the GUI for troubleshooting production issues.

## Accessibility Is More Than Supporting Screenreaders by Seren Davies

> All too often we think about accessibility as just meeting the needs of those who rely on screenreaders, but it's a far wider issue than that. In this talk, Seren will explore how people with cognitive, physical, hearing and sight difficulties experience the web, and how the decisions we make affect their experience.

Seren's talk was about changing the web to make it accessible (as it was originally intended) and presented different types of disabilities (permanent, temporary or situational) which had been presented in an earlier Tech Nottingham talk [Helen Joy, The Dangers of Digital Exclusion](https://noti.st/helen/4UsZ6K/the-dangers-of-digital-exclusion).

10% of the UK population suffer from some form of **Dyslexia** and this makes it hard to read text which is ALL CAPS (ironically the British Dyslexia Association website was doing this) as it's harder to see where each of the letters begin and end if they are all the same height.

1% of the population have some form of **Epilepsy** and there were problems with the London Olympics logo and a flashing animation which was triggering photo sensitive epilepsy. (Slow) animations and hover text are useful but the advice was not to overuse them. Similarly don't use scrolling marquee text as this can cause problems for people with **ADHD** who are constantly distracted by it.

**Tipsy or Drunk** users were discussed and the lack of colour contrast in the Untappd app was given as an example of a poor UI design when users are likely to be drunk! The "City Mapper" has a better UI where the "Get Me Home" button increases in size later in the evening as it's the most likely option users will want to choose.

**Touch or Movement impairment** causes an issue with very long websites or single page websites with very long scrolling, also a lack of "Back to Top" links to save having to scroll back to the top of websites. Having very small areas where you have to click *exactly* on a word to access a link is an issue, particularly on mobile devices where a finger is being used instead of a more precise mouse cursor.

**Deafness** affects 1 in 6 people in the UK so it's important to have annotations for non-audio situations such as on video, also useful if you don't have headphones in an open plan office. The [British Deaf Association](https://bda.org.uk/) have a style guide on their website.

To test for accessibility there are resources from Microsoft, those from the W3C consortium or the Lighthouse feature in the Google Chrome browser.

## Links

[British Deaf Association](https://bda.org.uk/)

<http://www.dylanbeattie.net/>

<https://twitter.com/JSOxford>