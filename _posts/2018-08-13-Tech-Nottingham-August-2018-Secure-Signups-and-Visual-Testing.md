# [Tech Nottingham August 2018: Secure Signups and Visual Testing](https://www.meetup.com/Tech-Nottingham/events/253202050/)

## Security Sins Of The Sign-Up Process by James Barker

> The sign-up process is one of the earliest interactions a user will have with a website. There is a lot of pressure to increase the effectiveness of this process by requiring minimal clicks, the fewest key strokes and being as simplistic as possible.
>
> However usability and security often have conflicting requirements and leaning too far towards usability can lead to vulnerabilities...
>
> In this talk we will take a look at seven examples of what not to do during the user sign up process. Each example leads to a vulnerability that could be exploited later on and explores why it occurred and how it could have been avoided.
>
> This isn't a technical deep dive into the security aspects of software development. Instead it focuses on how the design stage can lead to vulnerabilities and aims to show where neglecting security over user experience or not fully understanding requirements is just as insecure as badly written software.

James' talk introduced seven security sins with examples, in no particular order!

1) Not verifying email addresses / giving too much information

An example was given of a security issue in the Netflix sign in process where it provides too much information to a potential attacker as it confirms whether an email address exists or not rather than failing with an "invalid username or password" message when attempting to sign in.

The problem was compounded by not having to sign into the password reset page, it was possible to exploit the feature of Gmail addresses which ignore full stop characters "someone@gmail.com" and "some.one@gmail.com" going to the former email inbox.

2) Password length limits

Restricting the length of a user's password causes issues if hashed passwords are leaked because it reduces the length of time it takes to brute force passwords against a common password dictionary, if the attacker knows the password can only be 1..8 characters they can reduce the number of combinations they need to attempt.

3) Trimming or weaking passwords

I hadn't heard of this issue before but some sites remove spaces from passwords and also remove injection characters, a password should never be displayed on screen so there is no need to remove injection characters and shorten (weaken) someone's password.

4) Generating passwords for the user

There are two issues here as people are generally lazy and won't change the password they are assigned. If the password is sent out to the user in an email it could either be read in transit if TLS isn't used or is vulnerable because it's stored in plain text in someone's mail box.

5) Revealing passwords a user has set

Similar to the previous point and I have seen this issue myself for some websites where they confirm the email address you have just used to sign up and also email the password you set.

6) Disable activation links

It might seem obvious but if a site has generated a link and sent it to someone to confirm their email address then this should only be used once, the risk is that the URL including the special activation code could be stored in the user's browser and used to bypass security and log in again.

7) 'Common' security questions

This seems to be an issue in banking or financial services where questions are asked where the information is in the public domain (or slightly less public on social media) like "What is your mother's maiden name?" or "What is your eldest child's middle name?". Some sites do allow the user to set their own questions but this may lead to the same common questions being used to allow someone access to an account with having to specify a username or password.

## Spot The Difference: Automating Visual Regression Testing by Viv Richards

> In this session we look at why we automate tests, the issue with just manually testing, common end to end automation pitfalls, a brief introduction to visual testing and finally a look at common issues with visual testing and ways to overcome them.
>
> Using interactive examples we will gain an understanding of why relying on just manual testing can become an issue and how too much end to end automation can have a negative impact. The audience will also learn what visual testing is, what tools are available, some of the common pitfalls of using visual testing as well as tips on ways to overcome them.

Viv's talk on an image comparison framework for automated testing included some interesting information and tips which I hadn't previously considered.

### Automated Testing

An important point was made that automated testing doesn't guarantee user friendliness or customer experience as it's difficult to create automation tests to check this. The length of time it takes a website to respond would be an exception.

UI tests running in an actual or simulated web browser take a long time to run (several hours for example) and to cope with this more unit tests can be written to compensate, shifting the problem to a different part of the technology stack.

Testers have more domain knowledge than devs _[citation needed!]_ so unit tests created by developers because they are quicker to run may not be as effective, this may vary depending on the size of the team I suppose but it's a valid point.

Viv outlined the large choice of automated testing tools and outlined why his company chose to use Selenium, which I've some limited experience with using myself.

He discussed how they had caused problems for themselves by maintaining too many Selenium helper functions to help out the testers, presumably as they had "traditional" testers who hadn't previously written C# code and needed some help in changing roles to "Developers in Test".

Automated testing might sounds great but some warnings were given that browser quirks where browsers render web pages slightly differently or take slightly different times to refresh can cause issues with Selenium tests. This can be worked round by having tolerances when running a test against a particular browser, but it means you aren't writing tests once and then running them on all browsers, you're having to maintain a set of tweaks for each browser.

Selenium or other automated tests aren't prefect and can still get caught out by CSS issues, an example was given where a "Submit" page on a page had disappeared but because it was just invisible to the user but still present the Selenium test didn't notice the difference and passed the test.

This leads into the use of *visual testing tools* to help cope with this issue.

### Visual Testing Tools

There are fewer visual testing tools avaiable compared to automated testing tools but still a reasonable selection and variety between paid and open source plus the programming languages you can use or the ease of creating tests.

Viv's company looked at the options in the marketplace but decided to create their own visual testing tool, a link is below to the GitHub page.

Visual testing tools take a screenshot of a web page and use this "baseline" to determine whether something has changed.

This can lead to false positives due to the browser rendering quirks as described above in the section on Automated Testing where an image is nearly the same or looks "near enough" to the human eye but an automated comparison can't make this distinction.

Failed tests get a visual representation of what the test thinks is the issue, the part of the screen which has changed is highlighted which is useful for debugging.

The visual testing tool developed included the ability to have a "amount of change" value to express as an integer for how different a part of a website is, this made it possible to tweak the comparison between a pixel perfect comparison or a "good enough" comparison to save time looking at false positives.

One of the downsides of having to record a base line image for each webpage means having to also store an image for each browser which increases the complexity by a factor of how many browsers you need to support.

Dynamic content (the number of people attending a Meetup) or animations or video can also cause problems but it is possible to "mask" sections of the website so these are ignored by the comparison so they don't get flagged every time the tests are run.

## Links

[Spot the difference - automating visual regression testing slides](https://www.slideshare.net/vivrichards/spot-the-difference-automating-visual-regression-testing-97864745)

[https://github.com/vivrichards600/AutomatedVisualTesting](https://github.com/vivrichards600/AutomatedVisualTesting)

[@Viv Richards](https://twitter.com/11vlr)

[http://vivrichards.co.uk/](http://vivrichards.co.uk/)
