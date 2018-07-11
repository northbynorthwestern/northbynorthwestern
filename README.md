# northbynorthwestern.com

[northbynorthwestern.com](http://www.northbynorthwestern.com/) was created in 2011(?! fact! check! this!) by our forefolks of yore. Since then, the Internet has changed :scream:. People [use](https://medium.com/front-end-hacking/how-it-feels-to-learn-javascript-in-2017-a934b801fbe) and  _love_ JavaScript! News is read on phones! Social media _is_ the place for news?!?!

Okay, but really. The old website has served its purpose. We are *SO* proud to be one of the only student publications that has created and maintained its very own website and we are *SO* grateful for people who started that legacy by making the site in the first place! We want to continue this work by making the site better for our reporters, editors, readers, and developers!

The website right now is like...

![gif](https://i.imgur.com/WWsGOwu.gif)

We want the website to be like...

![gif](https://i.imgur.com/cJERtAb.gif)

So here's how we're going to do it!

## The plan

### Frontend
We're planning to use [React](https://reactjs.org/) to implement the reader-facing side of our site. We'll use the [comprehensive style guide](https://docs.google.com/document/d/1UdR9JsL967WbApox2wR-cGt__vxxAkGObsi0iIJxf-c/edit?usp=sharing) and visual mockups (below) NBN's designers created to design the site.

* Front page (above the fold) ![Front page above](http://media.northbynorthwestern.com.s3.amazonaws.com/uploads/2018/07/03/Homepage_above_the_fold.png)

* Front page (below the fold) ![Front page below](http://media.northbynorthwestern.com.s3.amazonaws.com/uploads/2018/07/03/Homepage_below_the_fold.png)

* Article page ![Article page](http://media.northbynorthwestern.com.s3.amazonaws.com/uploads/2018/07/03/Redesign_Idea.png)

* Staff page:
![Staff page](http://media.northbynorthwestern.com.s3.amazonaws.com/uploads/2018/07/03/Author_page.png)

### Backend
We want the reporter-facing side of the site to gel with the natural workflow of our staff. The editorial team uses Google docs to write and collaborate on stories, so we want to build a backend that works seamlessly with the team's current processes.

In order to do this, we need systematically formatted Google docs so we can identify different assets/information in a story and reliably create article pages from that format. To make this easier for the editorial staff, we are creating a [Google add-on](https://developers.google.com/apps-script/add-ons/) where a writer can select a formatted block from a sidebar to put their content inside. A formatted block for an article header might look like:
```
Headline: ''
Subhead: ''
Author: ''
```
Where an author would fill in the values to the right of the colons. A formatted block for an image would be:
```
[.photo]
link:
caption:
credit:
[]
```
Here's one high-level idea of how our technology can work with our staff's workflow:
* There will be article skeletons with basic formatting pre-made for each section. Reporters can make a copy of that skeleton and write their story just like normal.
* If the writer or their editor wants to add any special assets -- images, pull quotes, etc. -- they can use the Google add-on to find the formatting block for that component.
* Editors and writers can comment and make changes just like normal.
* When an article is complete, the editor/reporter should double-check the Google doc's formatting just like they might double-check spelling or a source's information.



We'll use the [Google Drive API](https://developers.google.com/drive/) (along with tools like [ArchieML](http://archieml.org/), [Amazon S3](https://aws.amazon.com/s3/), [Browserify](http://browserify.org/), [Gulp](https://gulpjs.com/), etc.) to pull articles directly from writers' docs to the site. Here's one high-level idea of how our technology can work with our staff's workflow:

* A reporter will write their story in a Google doc just like normal. The only difference will be some light formatting: [light formatting example](http://media.northbynorthwestern.com.s3.amazonaws.com/uploads/2018/07/03/Web_Redesign_Style_Guide.pdf)
In this doc, writers and reporters can add images, create pull quotes, and more just by adding a few formatted lines! We'll have a document with all the Google doc shortcuts so any staff member can add features beyond just the article itself.
* Editors and writers can comment and make changes just like normal.
* When an article is complete, the editor/reporter should double-check the Google doc's formatting just like they might double-check spelling or a source's information.
* There will be a folder in the North by Northwestern Google drive titled "Published" (or anything that indicates a piece is complete). Each section will have a folder within that "Published" folder. The doc containing the completed article will be dragged into the corresponding section folder.
* The story will automatically publish to a page!
* If a story needs to be updated or deleted for some reason, there will be an app under the "Add-ons" dropdown menu that will have buttons to allow these actions.

We are still figuring out how to let reporters and editors preview an article before it publishes, but as we dig deeper into the technology behind publishing process, we'll hopefully get a better idea.

## Process
To keep ourselves accountable, we'll be tweeting and  updating docs -- on GitHub and maybe even on Medium -- noting our progress, challenges, and technical decisions.

We'll use GitHub issues, branches, pull requests, and project boards to organize our work and make sure our `master` branch has the most stable, functioning (when applicable :joy:) code on it. We'll also use make another markdown file with setup instructions for any developers who want to jump in and try out what we're working on.

Our entire project will be open-source, meaning anyone can see our code. Ideologically, we believe in open-source as a way to promote information accessibility and accountability. Practically, it makes sense because it allows for feedback and contribution from other developers.

We plan to document the technical aspects of our work along with the process in order to make passing down maintenance of the site a smoother process.

## Contributors / Maintainers
Reach out to [@adebruine](https://github.com/adebruine) or [@maxine](https://github.com/maxine) with questions, comments, concerns, or encouragement for the project!
![Jack Black saluting](http://gifimage.net/wp-content/uploads/2017/11/godspeed-gif-3.gif)
