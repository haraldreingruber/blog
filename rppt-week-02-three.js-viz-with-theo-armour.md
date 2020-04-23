---
id: "devto"
---
@import "dev-to-style.less"

**- Week 2 of my Remote Pair-Programming Tour -**

[Theo][theo-armour-twitter] found out about my tour from my [outreach email campaign][tour-article] and liked the idea from the beginning. He even offered to cover my accommodation costs in San Francisco, but due to [COVID-19][covid-19-wiki] I had to return to Austria before I was able to start my tour. Thankfully, Theo was still interested in continuing the collaboration and knowledge exchange online and I was happy to find out how he was using [three.js][threejs-web] for the [COVID-19 visualization](#covid19-viz3d) and his various other projects.


[covid-19-wiki]: https://en.wikipedia.org/wiki/Coronavirus_disease_2019
[theo-armour-twitter]: https://twitter.com/ta
[tour-article]: https://dev.to/harald3dcv/pair-programming-tour-invite-me-for-free-sessions-sf-bay-area-5eci

## Shared passion for 3D visualization and three.js
Theo is working on some really interesting projects, all [FOSS][foss-wiki] and based on [three.js][threejs-web].

He is really passionate about how "easy" and fast you are able to visualize 3D content in the browser using [three.js][threejs-web], and his excitement is justified and very contagious. Collaborating on [three.js][threejs-web] projects was an awesome tour stop offer for me, and I enjoyed a lot figuring out how I can support Theo on his tasks and brainstorm with him about his future visions.

[foss-wiki]: https://en.wikipedia.org/wiki/Free_and_open-source_software
[threejs-web]: https://threejs.org/

## Interesting projects Theo is working on
Theo likes to create web apps with plain vanilla JavaScript and [three.js][threejs-web]. He has an uncountable number of projects and repositories on Github, which he created while experimenting with the reimagination of visualizing things (objects or information) in 3D.

### COVID-19 Viz3D
![COVID-19 Statistics 3D Visualization][spider-covid-19-viz-img]
A couple of weeks ago, with the start of the [COVID-19][covid-19-wiki] pandemic, Theo started a project to visualize the global statistics on a 3D globe in the browser, fetching data from the John Hopkins University and Wikipedia. Here is the [COVID-19 Viz3D][spider-covid-19-viz], which is also static HTML with plain vanilla JavaScript, only depending on [three.js][threejs-web] and fully running in the browser for desktop and mobile devices.

### Spider gbXML Viewer
![Spider gbXML Viewer][spider-gbxml-viewer-img]
One very remarkable project is the [gbXML][gbxml-web] viewer, which allows to view building data stored in Building Information Models (BIM). Check out this online demo of the [Spider gbXML Viewer][spider-gbxml-viewer], I especially like the exploded view and the possibility to toggle the view between interior/exterior surfaces which can be found in the popup menu on the right.

### three.js cookbooks
There are hundreds of HTML and JavaScript snippets, which Theo published in his "[cookbooks][cookbook-wiki]", like [this one][jaanga-threejs-cookbook]. The idea is to have browser-ready online demos, where also people new to JavaScript and programming in general are able to copy, paste and adapt the code snippets from the [github repository][jaanga-threejs-cookbook].

[cookbook-wiki]: https://en.wikipedia.org/wiki/Cookbook#Usage_outside_the_world_of_food
[gbxml-web]: https://www.gbxml.org/About_GreenBuildingXML_gbXML
[spider-gbxml-viewer]: https://www.ladybug.tools/spider-gbxml-tools/spider-gbxml-viewer/
[spider-gbxml-viewer-img]: https://github.com/haraldreingruber/blog/raw/master/imgs/rpp-tour-week2-theo/gbxml-viewer_small.png
[spider-covid-19-viz]: https://www.ladybug.tools/spider-covid-19-viz-3d/
[spider-covid-19-viz-archive]: https://www.ladybug.tools/spider-covid-19-viz-3d/dev/covid-19-viz-3d-archive/
[spider-covid-19-viz-img]: https://github.com/haraldreingruber/blog/raw/master/imgs/rpp-tour-week2-theo/covid-19-viz_small.png
[jaanga-threejs-cookbook]: http://jaanga.github.io/index.html#cookbook-threejs/index.html

## Time zone difference and common working hours
Theo usually works in the afternoon and evening. Combined with the nine hour time zone difference between Pacific and Central European time, it was not so easy for us to find time slots which was working well for both of us.

In the beginning we tried to do two 2-hour slots in the morning and evening, but we soon realized it is better to have only one session per day instead of switching back and forth. After several sessions, we decided that doing 2-hour sessions twice a week works best for us. I've kept "week 2" in the title of this article, which is the week of my tour where we started collaborating. We continued collaborating in the weeks after at a lower pace. 

## Topics Theo and I were collaborating on
After Theo showed me what he was working on, we figured out which topics might be interesting to start working on and kicked off our collaboration.

### three.js performance profiling and improvement
* Loading large amounts of data
* Creating many 3D objects
* Enabling user interaction with hundreds of obects
* Keeps the Globe spining without too much jitter]
* Maintain a high rate of framers per second - 60 gps being ideal
* Make it all happn on computer, tablet or phone

### Calendar versioning and automated deployment
Theo uses a [calendar versioning][calver-web] approach, which allowed him to run different versions (by date) directly in the browser from Github Pages. He tried to create a new feature for the [COVID-19 Viz3D][spider-covid-19-viz] every day, and a [menu linking to all daily versions][spider-covid-19-viz-archive] clearly shows the impressive progress the project had during a couple of weeks.

#### Separation of concerns
While working with him, I noticed that because of creating copies of the source folders, Git can not be used to it's full extent as it looses the connection between the different versions. Still, the advantages of having all versions online in parallel is evident. My gut feeling was if the concern of versioning are separated from the concern of deployment, Theo could benefit from having all previous versions online while being able to use the full power of Git versioning.

#### Continuous deployment of tags/branches
We made a plan, to experiment with a couple of workflow changes:
- Configure Github Pages to use a separate gh-pages brach, instead of master, which contains the sub-folder with all relevant source files
- Create a branch or tag for each version
- The development branch will only contain the current version
- A deployment script will update the gh-pages branch and copy the current version to a sibling folder named after the branch name
- The script will be executed on every new commit pushed to Github, by a continuous integration service like Github Actions, Travis CI, Circle CI, Gitlab CI, etc.

[calver-web]: https://calver.org/

### ESlint
Theo knew already that there is value in using tools for auto-formatting your code and static code analysis, but ESLint has a high learning curve if you are not very familiar with the Node.js ecosystem and NPM.

I know how much you can learn from the suggestions of static code analysis, and how much more readable code with consistent styling is. Our eyes and brain unconsciously detects even slight differences, which consumes cognitive energy you might want to reserve for the actual task you are working on. But you don't want to spend the cognitive energy on sticking to strict coding styles either, which is why tools doing that for you are very helpful.

Helping Theo with a initial setup of ESlint and simple NPM scripts for linting and fixing the JavaScript files, allows him to step-by-step get used to the workflow and adjust the ESLint rules to his preferences. Later he will be able to copy the settings to other projects as well.

[eslint-web]: https://eslint.org/

## Conclusion
