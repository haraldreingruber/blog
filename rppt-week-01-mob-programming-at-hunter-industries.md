**- Week 1 of my Remote Pair-Programming Tour -**

My [Pair-Programming Tour][remote-pair-programming-tour] on the US West Coast ended right before it even began. The [COVID-19][covid-19-wiki] pandemic forced me to return to Austria, a couple of days after I arrived in San Diego (California), where my tour would have started at [Hunter Industries][hunter-web].

[covid-19-wiki]: https://en.wikipedia.org/wiki/Coronavirus_disease_2019
[hunter-web]: https://www.hunterindustries.com
[remote-pair-programming-tour]: https://dev.to/harald3dcv/pair-programming-tour-invite-me-for-free-sessions-sf-bay-area-5eci

## From On-site to a Remote Pair-Programming Tour
Thankfully all my 3 confirmed tour stops agreed that we can do the planned pair-programmed sessions also online. While I am very happy that I didn't have to cancel my tour completely, I am a bit sad that the opportunity of meeting very interesting developers, companies and humans in person. Also, the 9-hour time zone difference adds another challenge, which means we only can collaborate for half-day sessions in the pacific-time morning (evening in Austria).

## Mob-Programming Invitation
[Austin Chadwick][mob-mentality-twitter] of the Mob Mentality Show pod-/videocast crew invited me to join the mob-programming sessions after I saw a tweet about their show from [Amitai Schleier][amitai-twitter] and I reached out to them. 

My only mob-programming experience before was a one-hour session at a [code retreat][code-retreat-about] organized by the [Softwerkskammer Vienna][softwerkskammer-wien] group. Back then, I liked the idea but didn't pay more attention to it as in my experience it was already difficult to convince teams/employers of the advantage of pair-programming, so I assumed it would be even worse for mob-programming. 

My favorite quote from the Mob Mentality Show:
> Solo development feels like sitting at home watching Netflix. 
> Mob Programming feels like going out to a movie with friends. 
> Pair Programming feels like going on a date.
> -- *[unknown][financial-benefits]*

Watching the [videocast][mob-mentality-youtube] of [Austin][mob-mentality-twitter] and [Chris Lucian][chris-twitter] was really an eye-opener to me and was very curious about joining their mob-programming sessions.

[amitai-twitter]: https://twitter.com/schmonz
[chris-twitter]: https://twitter.com/ChristophLucian
[code-retreat-about]: https://www.coderetreat.org/pages/about/
[financial-benefits]: https://www.chrislucian.com/2019/09/mob-programming-financial-benefits.html
[mob-mentality-twitter]: https://twitter.com/mob__mentality
[mob-mentality-youtube]: https://www.youtube.com/channel/UCgt1lVMrdwlZKBaerxxp2iQ
[softwerkskammer-wien]: https://www.softwerkskammer.org/groups/wien

## Mob-Programming at Hunter Industries
![Austin, Kirjsten and Matt during our group learning session.][mob-programming-picture]<figcaption>Mob-programming with at Hunter Industries.</figcaption>

Last week my tour finally started and I joined the mob of Alex, Matt, and Austin   from remote from Austria. Because of COVID-19 they had to switch to working from home the week before as well. They were using Microsoft Teams for the online collaboration and accessing their on-site mob station via Anydesk. All of us were quite surprised that the oversea video-connection between us didn't cause a noticeable delay. They said they sometimes have more trouble talking to people (online) who are close by.

[mob-programming-picture]: https://raw.githubusercontent.com/haraldreingruber/blog/master/imgs/rpp-tour-week1/hunter-mob-programming-merged.png

## Dealing with Email in a Mob
They had one mailbox for the mob, where all the development related Emails were sent to. Every morning after the daily meeting with the Product Owner (PO), they were dealing with the mails, in a mob-programming style (with Driver/Navigator roles). It took usually around 5-15 minutes, and that was it regarding mail for that day, no further interruptions for checking mailboxes. 

## Test-driving a small improvement
The team is working on a mobile app of Hunter Industries Internet of Things (IoT) system. One of the first tasks was to add an "in-progress" feedback when fetching data, which could take a couple of seconds. From a user perspective, this improvement is actually not small at all, as it might avoid confusion when the app doesn't seem responsive. It was really nice to see how the development in the mob was working out very fluently. We were using the [Mobster][mobster-website] pair-/mob-programming timer, switching Driver/Navigator roles every 6? minutes.
First, we wrote a failing test, then the production code was moved forward. When the new test was succeeding it was time for refactoring, where we also watched out if the [Scout Rule][boy-scout-vs-scout] can or should be applied.

[boy-scout-vs-scout]: https://dev.to/ben/the-boy-scout-rule-is-now-the-scout-rule-420g
[mobster-website]: http://mobster.cc/

## Mob-programming allows fast onboarding and contributing quickly
It was interesting to see, that the mob was not slowing down much while I was learning and getting to know the project and the processes. In contrast to switching from solo-development to pair-programming, joining a mob is definitely less disruptive, which is probably not really surprising. Another interesting aspect was, that I was able to contribute ideas and solutions within the first couple of hours, even though I never worked with that specific platform-independent mobile app development framework before. As there were 3 other developers knowing the details and concepts of the framework it didn't really slow us down because I didn't know them. I have experience with similar frameworks and many concepts in programming are similar in many programming languages, so for many discussions I was still able to contribute valuable input. This was really motivating and quite a different experience compared to the usually very dense and at least perceived slow onboarding when you are working alone or with an expert developer of the new team, for example when starting working at a new company.

## New (non-trivial) feature development felt a bit sluggish?

In the middle of the week, we started to work on a feature that was new and more difficult. The feature was required in order to further improve the performance and responsiveness of the app.

When we started, there were many questions and unknowns. How to test this? Which parts do we have to mock in order to be able to write tests and isolate the test units from each other? Do we start with the small technical details (bottom-up/Detroid School TDD) or with the top-level requirements (top-down/London School TDD)? As often the answers are to some extend also a matter of taste and the arguments for one or the other are not really known in the beginning the direction in which we were going was depending a lot on the current navigator. As the navigator role was switched, sometimes it was leading to a change of direction as the picture on which path was better was not yet developed and/or was perceived differently within the team.

We talked about this later in the retrospective, that this was a bit of a surprise to me. It was probably also the case that in a mob, a process feels sluggish much earlier when 4 people are working on one task, compared to if a developer is struggling with starting a new feature for hours. Another difference is that when working alone, you sooner take one direction and continue as you don't have to justify or discuss the idea with others (ideally you had a discussion with the team before starting to work on the feature). This way, the development is perceived faster, but in some cases, you might have to invest more time in refactoring or changing the initial idea later (maybe already during the review). My mob was not surprised about my observation about this exploratory task and saying that this is quite certainly outweighed by the improved outcome and the much faster development time in other phases (bug fixing, refactoring, etc.).

I really like this quote about mob-programming:
>  In practice it feels more like a bulldozer than a race-car - unstoppable and thorough.
> *--unknown*

## Splinter Group Pattern

On Thursday, the mob had to prepare for the monthly department-wide status meeting, where the top-level management of Hunter Industries informed themselves about the current state of the developments. We still wanted to move the code forward, so we decided to create a [splinter group][splinter-group-pattern]. Alex and me continued test-driving the new caching feature, while Austin and Matt were working on preparing the slides and reports for the meeting in the afternoon. After lunch, we joined the mob again and discussed the results of both teams.

[splinter-group-pattern]: https://github.com/michaelkeeling/mob-programming-patterns

## Group learning session

On Friday, we reserved 2 hours for a group learning session, which was announced department-wide and everybody who was interested was able to join. I shared my experience and the ideas of [Git-bisect][git-bisect-article], the idea of my Pair-Programming Tour and asked several questions about mob-programming.

![Austin, Kirjsten and Matt during our group learning session.][group-learning-picture]<figcaption>Austin, Kirjsten and Matt during our group learning session.</figcaption>

[group-learning-screenshot-url]: https://github.com/haraldreingruber/blog/raw/master/imgs/rpp-tour-week1/hunter-group-learning-screenshot.png
[group-learning-picture]: https://raw.githubusercontent.com/haraldreingruber/blog/master/imgs/rpp-tour-week1/hunter-group-learning.jpg

When I asked my mob-programming questions in the end, it led to a lively discussion which was very insightful and I'd like to share my takeaways from it:

### 1. Why is Hunter Industries cool with often having guests joining the mob-programming sessions?
When I reached out to Austin during the preparation of my tour, he said that they have guests joining their mobs regularly, so the process would be simple for me as well. I asked them if it was difficult to get support from their managers, or which value they saw in having guests joining. The response was that there were 2 advantages they saw in frequently hosting guests. The obvious one is that next to sharing their knowledge and mob-programming experience their teams also often get very good input from their guests and different perspectives. The other advantage was that it is good PR for their recruitment efforts. Hunter Industries is known in the development and agile world as the inventor of what we today call mob-programming, and they are doing it already for almost 10 years. The guests who visit them talk and write about it, which in turn will raise the interest of developers sharing the same or similar values.

### 2. Would you say mob-programming might become the future for every developer?
This was more a provocative question, which I told them, and I explained that I was more interested in their thoughts than the actual answer.
I think there was a wide agreement that, similar to pair-programming also mob-programming is definitely not optimal for every developer, and that every team and every developer has to figure out themselves what works well and what doesn't work well for them.

![Fred Zuill and Austin Chadwick on a screenshot during our group learning session.][group-learning-screenshot-url]<figcaption>Fred Zuill and Austin Chadwick on a screenshot during our group learning session.</figcaption>

I like how Fred Zuill, who also joined the group learning, explained his thoughts, saying that there is this thing called mob-programming today, which might develop into something that we will call differently tomorrow. One thing that will for sure spread to a big part of the industry is the need for faster innovation and that the close collaboration improves learning and leads to better results. How that collaboration will look like might vary and change.

### 3. Do you know small companies practicing mob-programming?
The idea behind this question was that for small companies having the trust that forming a mob of 3-4 people, maybe having only a single mob working on the tasks for creating and improving their software seems to me to be more challenging than for a larger company, already having established a constant cash-flow.
There were not really clear answers, there were one or two start-ups mentioned doing full-time mob-programming. Still, there was a general tone that even though the pressure for small companies might sometimes be higher, there are small companies doing mob-programming. Small companies often need to innovate faster, where mob-programming might come in handy.
Chris Lucian, the director of software development at Hunter Industries, shared a link to his blog where he compiled a [list of companies doing mob-programming][companies-doing-mob-programming].

### 4. What would you recommend for introducing mob-programming to a team that never did it before?
Austin shared a nice website about mob-programming patterns with me, which also has a pattern describing [beginning mob-programming][beginning-mob-programming].

[beginning-mob-programming]: https://jay.bazuzi.com/Mobbing-Pattern-Language/metapatterns/Beginning%20Mobbing.html
[companies-doing-mob-programming]: https://www.chrislucian.com/p/companies-that-are-mob-programming.html
[git-bisect-article]: https://dev.to/svettwer/automated-debugging-with-git-2pod


## Impression and conclusions of my first week

I really enjoyed my coding tour start with the team of Hunter Industries. Thanks Alex, Austin and Matt for inviting me to join their mob. Thanks Hunter Industries for having a guest-friendly mobbing policy, and being open to continue my visit from remote during the chaotic time of the COVID-19 crisis.

I have heard about the high-bandwidth learning during mob-programming before and liked it a lot experiencing it with the mob at Hunter Industries. Also, I think that mob-programming created a very mindful company culture at Hunter Industries, or was it the other way around? What I already realized that I like about going on a coding tour is, the experience while working on real-world tasks. I think that practicing certain techniques and experimenting with coding katas, for example at coding dojos or code retreats is really important and helpful, it's still often difficult to apply certain ideas on the task in the every-day job.

Looking forward to the impressions, conclusions and insights of the next week of my Remote Pair Programming Tour while working on projects using three.js with [Theo Armour][theo-armour-twitter].

[theo-armour-twitter]: https://twitter.com/ta
