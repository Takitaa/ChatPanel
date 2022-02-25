# chatchallenge

## The Beginning

### Challenged to create a chat-sidepanel with the following aspects:

1. Please create a new VueJS (1.x latest) project as repo on github.
   a. use typescript! for the project!!
   b. add "itsatony" as a collaborator to the project.
   c. create a USEFUL README please. explain what you did. what was problematic
   and why. how you approached the tasks and solved them.
   d. ideally, commit whenever it seems reasonable to you - imagine you're working in
   a team of 4+ developers on this project.

2. The application should show a video-player + chat-sidepanel layout. The chat-sidepanel
   should be aligned right in a container with a max width of 350px and a min-width of
   300px. Take inspiration from this: <a href="https://webclient.spect8.me/demo.html" target="_blank">https://webclient.spect8.me/demo.html!</a>

3. Add a video-player to the main container (play any public video - you can re-use the one
   we use).

4. Add a button for "theatre-mode" where the video + chat-sidepanel go into fullscreen
   mode.

5. Add a slide-in + slide-out button to the chat-sidepanel. This should work (animated) both
   in full-screen mode and normal mode.The video-size should adapt according to the
   sidepanel status (out/in/sliding animation).

6. add an input field to the bottom of the chat-sidepanel with a submit button and a
   emoji-selector (use any available plugin you like).

7. entering a message and submitting (either pressing return or clicking/activating the
   submit button) should MOCK/SIMULATE an async call to a backend and then reception of the message (independently asnyc) from a eventsource connection. upon receiving the message from the mocked backend, add the message to the "message-list" above the input field.
   DO NOT WRITE A BACKEND HERE! Find a smart way to mock/simulate the backend calls/push messages in the frontend. Try to make sure the mocked code can very easily be replaced with a real backend.
   EXPLAIN your approach and execution in the README!

8. the "message-list" field should show avatar,username and the message content.

9. each first load of the page should create a random username + select a random
   user-avatar (where to get those is up to you). store these in localStorage so that a reload
   will give the same username+avatar.

10. add a button to "shuffle new user" which will randomly select another username and
    another avatar.

11. add the custom emoji to the emoji-selector and make sure they are rendered correctly in the input field AND in the message-list.

12. Finally - do something COOL in this project. Surprise us, WHOW us, if you can. Show us what you can do! All up to you :)

## DAY 1 - Personal approach:

> Visiting [https://webclient.spect8.me/demo.html](https://webclient.spect8.me/demo.html) in Chrome

> Opening Dev Tools - Inspect

> View Source code for an overall idea - I feel better looking directly to the code as it is, plain and simple, no tricks or hidden folders

    - happy to see the video source already

> Dev Tools / Sources

-   Reacted folders in VS
-   Opening .htlm with VS Live Server and noticing that JS does not seems to be part of it. [Oh no](https://www.youtube.com/watch?t=12&v=fXLicO0CRvk&feature=youtu.be)

### Felling it in my guts

> That I will need VUE CLI and Components more than I could have imagined at the beginning of my VUE learning both lessons not yet reached in my one and only VUE contact/learning approach at Udemy [Vue - The Complete Guide (incl. Router & Composition API)](https://www.udemy.com/course/vuejs-2-the-complete-guide/). However, as I like to look around the lessons to spot important/crucial learning modules, these two caught my eyes.

Plan for day 1 : Learn Vue CLI and get a hand of Components.

> Update: WHY Learning approaches often teaches you the simplest way to implement a framework only to destroy all your knowlege by showing completely different and more efficient ways of doing it in advanced lessons?!? - this happened to me with Phaser 3 too.

If they would have a minimum humanized approach, they would know that, specially visual learners - as I am - print every image to their souls being much harder to start from kind of zero again, even more when we have nearly zero time to learn this new technology as time urge to put it to practice.

### Kind of panicking but searching for hope/resources around (online) #pleaseGoogleHelpMe

> Learning way too fast that there are not really many resources - at least not as I expected.
> Checking around my Udemy lessons for anything seemenly close to what I need aka a more ready solution = NOPE
> Searching among the other VUE courses I have [The Complete Vue JS Developer Course – inc. Vue JS 2!](https://www.udemy.com/course/vue-js-2-the-full-guide-by-real-apps-vuex-router-node/) - great, how old is this?!? / and [Vue JS 2: From Beginner to Professional (includes Vuex)](https://www.udemy.com/course/vuejs-from-beginner-to-professional/l), this second one quite helpful - me jumping to the module Animations & Transitions Hello <templates><templates> and <script></script>

## Reimagination of the wheel!

This itched my creativity :sparkles:

## DAY 2 - Project setup

### Updating node - aware of the recent security issues in node_modules

```
npm update npm -g
```

```
npm -v
V16.14.0
```

### Typescript version

```
tsc -v
 not found
```

I remember doing thins not -g but in local folders so time to correct that

```
npm install typescript -g
Tsc -v

4.5.5
```

### Installing Vue CLI

```
npm install -g @vue/cli
```

```
Vue --version
@vue/cli 5.0.1
```

### Creating Project folder - Vue App

```
vue create  vchallenge
```

> UPDATE 1: later I created a new project folder as for this first one I chose default settings and was not asked to choose features such as Typescript.

    In doubt of having it or not and noticing there was no .ts file among the project I added

    ````
    vue add typescript
    ````

    But I messed up ignoring the suggestion for not compiling JS files, which result in my project not working on the browser - because compiler could not find main.js that by now was changed to main.ts. I then ran vue add again, this time saying no to compliting JS files and everything was running again, however with many merge issues.

    I was wasting more time with Git-Github than with anything else so I created everything from zero, this time with create vue manually - typescript was there.

    I will make some progress using the setup as it is - not .ts file at least to put the video on and add a toggle sidepanel/container with the requested measures, after that I will populate the chat and/or work on the toggle button + Submit button.

    After the progress, I will time to add Typescript and see if things jump to TS magically.

> Update 2: I could not ignore the TS - first item of my challenge list, so I started from there, found out about Vue UI and add TS successfully - same could have hapenned by using VUE CLI I as I just messed up with the activation options.

### Compiles and hot-reloads for development

```
npm run serve
```

### (by default readme) Compiles and minifies for production

```
npm run build
```

### (by default readme) Lints and fixes files

```
npm run lint
```

## DAY 3 - Hands On!

> Before start attacking the tasks, I checked my git/github sync situation. Not having used them as part of a team, I lack of some command habits, often confusing pull and push (this happens because I'm always in a worry digging around these tools for life saving measures only).

I took the time and clarified that push was what I needed (sync my remote to the changes from my local) and pull... what a surprise! a Pull Request is an opportunity to have my code revised etc, loved it - a hello world moment.

I've seen this pull request button in VS and all I knew was: I don't need it.

Reading the [GIT guide](https://github.com/git-guides/git-pull) helped me out.

### Challenge new approach

> Better informed about Vue projects, I analysed the Inspiration code again. And realised I have two options: create mine from zero OR modernize demo.html to a Vue app, getting rid of those getElementById, adding the css to style etc.

I've been preparing myself to do it from zero, will give some time to this and then possibly do the second option which I believe would be more clever and would definitely show my Vue capabilities.

My dilemma is: in which way would I have this solution up an running faster?

### Customize configuration

See [Configuration Reference](https://cli.vuejs.org/config/).
