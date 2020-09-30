---
id: "devto"
title: Remote Pair- and Mob-Programming Tour Spring 2020 - Stories yet to be told
---
@import "dev-to-style.less"

## Week 1: 
See []()

## Week 2: 
See []()

## Week 3: Learning Flutter with Adrian
Adrian had already a project idea for collaboration in his mind. He implemented a website for hiking routes about 15 years ago, and he suggested to create a mobile app for that.

I liked the idea, and I always wanted to give Flutter and Dart a try, so we agreed to use that technology. The language was new for both of us, plus Adrian never worked on a mobile app before. It was a learning experience for both of us.

### Flutter and Dart
We were surprised how easy and frictionless the setup of the project went. I have worked with React Native before and I was a bit overwhelmed with the amount of libraries and frameworks I saw in project templates.

In less than 2 hours we had a base application working on both of our computers.

Dart is nice as a language, it kind of combines the simplicity and expressiveness of JavaScript (less boilerplate code) with the advantages of typed languages. Compared to TypeScript it seems to be easier as types are a first class citizen in dart, and also it doesn't need complicated languages features which TypeScript needs in order to be able to establish compatibility with untyped code.

Also, when we got stuck we were able to quickly fix the issues.


### Floobits for remote pairing

As we both were familiar with JetBrains IDEs, we decided to use Floobits for remote collaboration. Compared to VSCode LiveShare, it has the advantage of syncing the whole project, so the other person was also able to run the App in an emulator (**TODO:** to be checked). But there were also sync issues from time to time, and it seems to have problems with syncing newly created files. Usually, re-connecting to Floobits solved the issues.

### Flexible pairing style

We were using a flexible pairing style, usually whoever had an idea took over the keyboard, the other one was following and it worked well for us. 

We assumed that if both are experienced in pair-programming and have a similar level of programming experience it doesn't matter that much which paring-style you are using. If you discover any communication or collaboration difficulties you should experiment with other styles and see if they help. Sometimes it is difficult to think, type and explain at the same time. Then strong-style pairing might be helpful. Maybe it worked well be cause our project had an exploratory goal. I could imagine if it is already clear what to do, and the driver just quickly executes one step after the other, the pairing-experience suffers big time.

### Migrating MSSQL DB from 2004

We decided to put all the data inside the app, as implementing a REST backend as well would have exceeded the scope and could be done later also.

We wanted to reuse the database Adrian used for the web app he developed years ago, which was running on MSSQL. I don't know how the MSSQL experience is today, but only installing took almost 2 hours (the version he used in 2004). After all, we were able to migrate the DB to SQLLite after half a day and were able to integrate it into our Flutter application in the following session.

### Test-driven Development with Flutter

We started the project with TDD practices. Flutter has a nice way of testing UI components and screens without requiring to render it. The execute very fast, don't need to be executed in the emulator and therefore have less disadvantages as UI tests usually have.

We continued our sessions on a weekly base after the official week part of my pair-programming tour. After a while we drifted away from sticking to TDD and focused more on feature development, which also was okay because our focus was learning and not so much about testing. But I wouldn't recommend this for apps that will be used in production.


## Week 4: Improving RegEx Performance at Glitch
**TODO:** almost finished.

## Week 5: Mob-Programming at Emmersion Learning

Emmersion Learning is developing a web-platform for language tests using speech recognition. Mike Clement reached out to me, that they have 2 teams in their company doing full-time mob-programming and I can join one of them.

### Mob-programming over multiple time-zones

One of their mobs is spanned over many time-zones. Mountain Time, Eastern Time and the Philippines. Eric and Charles usually start in the morning of the Eastern time zone (which is already late afternoon for Charles in the Philippines). Neil, Jon and Kevin join two hours later in the morning of the Mountain Time. 

## Week 6: Exploring TDD with Unity3D with Peter "CodeCop" Kofler

## Week 7: Hacking Mozilla Hubs with Fabien Benetou

## Week 8: Improve coding-sustainability for Streetmix3D with Kieran Farr

## Week 9: Test-drive Electric Boots with Ted M. Young 

## Week 10: Indy Game-Development using Unity3D with Max

