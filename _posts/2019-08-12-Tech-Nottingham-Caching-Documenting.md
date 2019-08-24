# Tech Nottingham August 2019: Caching And Documenting

<https://www.meetup.com/Tech-Nottingham/events/263561311/>

## Data Caching: Keeping It Hot by Samathy Barratt

> Every year technological advances come up with faster ways to get data flowing between storage and screen. However, while modern storage is fast, we must always trade off between Performance, Capacity and Persistence.  To keep speed up, we use tiers of storage with increasing performance, but decreasing capacity, shifting data upwards and back down as it is used. This is caching. This talk discusses the need for caching with a detailed look at the algorithms used to decide what data to keep in fast cache, and what to kick out. We specifically explore 'page caching' - a particular flavour of caching used in databases, operating systems and computer hardware itself. You will leave the room with the knowledge you need to "Keep it Hot". Audience participation may be required!

The "data caching pyramid" was described with the top of the pyramid being CPU / memory (fastest but smallest amount) and the bottom the large capacity HDD (slow but more of it available).

Something can be considered to be "hot" if it's in the cache at the top of the pyramid in the fastest storage possible but it's also impossible to cache everything.

Page caches used by databases and operating systems were described where each page is the same size, holds the same amount of information.

An optimal algorithm could predict the future and predict what needs to be kept in the cache to keep everything "hot" but practically this is impossible.

Various caching methods were discussed (see link below for slides) with a live demonstration.

## You Are Not A Precious Snowflake: Document Your Work by Kate Bolin

> Yeah, yeah, you're so important to the team. You're completely irreplaceable. Your work is the greatest work ever. Your memory is razor sharp and ready for anything. You have so much knowledge and experience that the gods themselves come to you for their programming issues. You are amazing, you are wonderful, you are obviously a genius and you're going to live forever. But you're not. You're replaceable. You're mortal. And you're not really that great at remembering what you put live six weeks ago, let alone a year ago, are you? Kate is going to get into all the reasons documentation is incredibly important, and how to make it easy and effective - not just for the people who'll be reading it after you get hit by a speeding Red Arrow on Parliament Street, but also for you on that early Monday morning before that first cup of coffee.

Documentation can be created whilst you work, after you finish something as long as it gets created. The process of creating documentation can be used as a "Rubber Duck" as if you can't document something the chances are you probably don't understand it well enough, find out what's missing and add it to the documentation to make it complete.

Include information about what exists but also the interactions between different systems which can help with future understanding or diagnosing issues.

## Links

<https://twitter.com/katemonkey>

<https://twitter.com/Samathy_Barratt>

### Documenting

<https://docs.google.com/presentation/d/1qQcFo0Eon_GscGqYmhHhOJWtFJr6v7qKpQwsSAeHOR4/edit#slide=id.g5f6b93f01f_0_769>

### Caching

<https://docs.google.com/presentation/d/1fUDNP9RPgMDlTeUFV7XAy3oZWhqobf9OgL7_B2FUgxg/edit?usp=drivesdk>