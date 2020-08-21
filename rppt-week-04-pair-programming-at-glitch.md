---
id: "devto"
---
@import "dev-to-style.less"

**- Week 4 of my Remote Pair-Programming Tour -**

[Johnicolas][johnicolas] invited me to pair with him after reaching out to developers in the `#PairWithMe` channel on the [Software Crafters Slack][software-crafters-slack-web] workspace.
He works in the infrastructure team at [Glitch][glitch-web] and is an enthusiastic software crafter and [Test-driven development (TDD)][tdd-wiki] practitioner.

[Glitch][glitch-web] is the name and a product of former Fog Creek Software, who invented [Trello][trello-web] and co-created [Stack Overflow][stack-overflow-web], tools which every developer know and probably use every day. You can imagine it as a Google Docs for developers, or as [JSFiddle][jsfiddle-web] for (also) back-end ([Node.js][node-web]) code. The live-editing and auto-deployment features are remarkable, and for getting started you don't even need an account for getting started. Just play around and carry-on your projects later if you like it. 


[glitch-web]: https://glitch.com
[johnicolas]: https://twitter.com/Johnicholas
[jsfiddle-web]: https://jsfiddle.net/
[node-web]: https://nodejs.org
[software-crafters-slack-web]: http://slack.softwarecraftsmanship.org
[stack-overflow-web]: https://stackoverflow.com/
[tdd-wiki]: https://en.wikipedia.org/wiki/Test-driven_development
[trello-web]: https://trello.com

## Test-driven-development with Glitch
{% glitch game-of-life-kata app %}

For getting to know each other and Glitch better we decided to do a code kata as an exercise. [Code katas][code-kata-web] follow the idea of [delibarte practice][deliberate-practice-definition], meaning to do a simple exercise over and over again in order to be able to pay attention to a specific technique and focus rather on the process than the actual result.

The integrated editor of Glitch doesn't have built-in support for running tests, which is why Johnicolas suggested using [Intern][intern-web] which runs the tests in the browser and displays a nice user interface with the result. Combined with the auto-refresh on every keystroke feature of Glitch it provides a nice development experience for test-driven development. The result can be shown in a side-panel to the right, so you have immediate feedback while typing your code.

Here is a template if you want to try out testing with Intern yourself: https://glitch.com/~intern-test-template

[intern-web]: https://theintern.io/
[code-kata-web]: http://codekata.com/
[deliberate-practice-definition]: https://blog.cyber-dojo.org/2015/05/do-more-deliberate-practice.html

## Pair-Programming using Glitch
The Google Docs-like collaboration experience of Glitch makes it a very interesting choice for Pair-Programming as well. You can get started quickly, start from scratch, or remix an existing project.

Practicing JavaScript-based code katas is also very easy, as you don't need to set up any development environment. Just start hacking.

## Pair-Programming with VSCode Live Share
For the actual task we wanted to collaborate on this week, we decided to work with VSCode. VSCode provides the Live Share feature, which works really well for remote pair-programming. Compared to other alternatives, it doesn't require to sync the whole project. Instead, it just opens the requested files from the hosts PC via SSH. The disadvantage is that it seems the code can not be accessed with external tools outside VSCode, which is probably not a problem for many projects. 

Live Share also offers a Shared Terminal window for running tools (e.g. npm scripts) on the remote host in a collaborative way, and even server ports can be shared by the host. What we didn't try was co-debugging, which might be handy as well, although if you are doing TDD a debugger should rarely be necessary :smile:.


## Merging multiple RegEx Tests into One
One of the tasks Johnicolas was suggesting we could collaborate on was refactoring a TypeScript class called BadRexer responsible for detecting malicious patterns in the project files of Glitch users. The current architecture was to test each file for multiple [RegEx][regex-wiki] patterns and suspend the project if one of the patterns was found.

The current approach was working good enough for most of the projects, but can cause some issues for bigger projects as each file has to be re-scanned for each pattern, which means in the worst case N files have to be scanned M times if the project doesn't contain any malicious pattern (which should be the normal/majority case).

Johnicolas already had an idea how this can be improved, and the idea is as elegant as simple: Merge each RegEx pattern into a single pattern by logically "or"-combining them. This of course only works if you don't need to know which test failed, which was the case in our scenario.



[regex-wiki]: https://en.wikipedia.org/wiki/Regular_expression

## Some Regex Features may cause exponential worst-case runtime complexity 
https://github.com/uhop/node-re2/#why-use-node-re2

## Heavy clean-up of test code

## Let it crash 