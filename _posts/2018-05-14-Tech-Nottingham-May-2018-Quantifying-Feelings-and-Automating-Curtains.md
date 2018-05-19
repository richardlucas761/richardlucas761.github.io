# [Tech Nottingham May 2018: Quantifying Feelings and Automating Curtains](https://www.meetup.com/Tech-Nottingham/events/250061017/)

## How I Ended Up Automating My Curtains And Shouting At My Laptop by Luke Bonaccorsi

> A few years ago Luke Bonaccorsi set about building a simple JavaScript chatbot that then quickly grew into a chat based automation system that he uses every day. The experience was, and still is, a fantastic learning opportunity and in this talk he’ll share his progress, his reasons for doing it and what he'd like to do in the future whilst also hoping to inspire you to build something weird.

Luke's talk provided details on the bot uprising and services like the visitor wrangling system where visitors sign into a tablet device at reception which I'd seen previously at Unidays. Most people are probably familiar with virtual assistant devices like Google Home and Alexa where there is an AI backend to a device in your home.

Luke described creating his own home automation system called Woodhouse which is a Node based modular system. He has a set of simple on/off remotely controllable plug sockets which are running OpenWRT which Woodhouse can control to turn lights on and off. He also described creating a 3D printed device used to control a thermostat using a remotely controlled servo.

It was interesting to hear how he'd learnt about the devices and their APIs he was interacting with, I haven't done much work with Node but it was interesting to hear about the possibilities.

## Feelings Quantified – Ranking Football Clubs By Supporter Sentiment by Matt Gordon

> Regardless of what football league you follow, some years the title chase can be quite boring. A football podcast in the US (Men in Blazers) came up with an interesting idea - what if we ranked the Premier League by the Twitter sentiment of the supporters at the end of the match?

> Matt Gordon heard that episode and created the Premier League Mood Table for them to discuss on the podcast. While the premise of a mood table might be quite silly, the underlying concepts and technology are relevant to any company with a social media sales presence. Join Matt as he walks us through using Azure Logic Apps, Cognitive Services, and Azure SQL Database to store and analyse Twitter sentiment that can impact your company's bottom line - and potentially yours as well!

Matt talked about sentiment analysis using Twitter to determine whether tweets were positive, neutral or negative using the Azure Cognitive Services API.

Social media and how companies deal with negative comments on social media is becoming more important with news cycles in media changing from days to hours.

Matt talked about creating a mood table for a football podcast where the sentiment amongst fans up to 10 minutes after the match had finished and whether this was positive or negative.

It was interesting to hear about how data mining tweets and feeding them through an API could be used to determine feelings although storing personal data becomes more of an issue with forthcoming GDPR legislation.

## Links

[Luke Bonaccorsi](https://twitter.com/LukeB_UK)

[Matt Gordon](https://twitter.com/sqlatspeed)
