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
   300px. Take inspiration from this: [https://webclient.spect8.me/demo.html](https://webclient.spect8.me/demo.html)

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

## 0 Personal approach:

> Visiting [https://webclient.spect8.me/demo.html](https://webclient.spect8.me/demo.html) in Chrome

> Opening Dev Tools - Inspect

> View Source code for an overall idea - I feel better looking directly to the code as it is, plain and simple, no tricks or hidden folders

    - happy to see the video source already

> Dev Tools / Sources

-   Reacted folders in VS
-   Opening .htlm with VS Live Server and noticing that JS does not seems to be part of it. [Oh no](https://www.youtube.com/watch?t=12&v=fXLicO0CRvk&feature=youtu.be)

### Felling it in my guts

> That I will need VUE CLI and Components more than I could have imagined at the beginning of my VUE learning both lessons not yet reached in my one and only VUE contact/learning approach at Udemy [Vue - The Complete Guide (incl. Router & Composition API)](https://www.udemy.com/course/vuejs-2-the-complete-guide/). However, as I like to look around the lessons to spot important/crucial learning modules, these two caught my eyes.

Plan for today: Learn Vue CLI and get a hand of Components.

> Update: WHY Learning approaches often teaches you the simplest way to implement a framework only to destroy all your knowlege by showing completely different and more efficient ways of doing it in advanced lessons?!? - this happened to me with Phaser 3 too.

If they would have a minimum humanized approach, they would know that, specially visual learners - as I am - print every image to their souls being much harder to start from kind of zero again, even more when we have nearly zero time to learn this new technology as time urge to put it to practice.

### Kind of panicking but searching for hope/resources around (online) #pleaseGoogleHelpMe

> Learning way too fast that there are not really many resources - at least not as I expected.
> Checking around my Udemy lessons for anything seemenly close to what I need aka a more ready solution = NOPE
> Searching among the other VUE courses I have [The Complete Vue JS Developer Course – inc. Vue JS 2!](https://www.udemy.com/course/vue-js-2-the-full-guide-by-real-apps-vuex-router-node/) - great, how old is this?!? / and [Vue JS 2: From Beginner to Professional (includes Vuex)](https://www.udemy.com/course/vuejs-from-beginner-to-professional/l), this second one quite helpful - me jumping to the module Animations & Transitions Hello <templates></templates> and <script></script>

## 1 - Project setup

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
npm install
```

### Compiles and hot-reloads for development

```
npm run serve
```

### Compiles and minifies for production

```
npm run build
```

### Lints and fixes files

```
npm run lint
```

### Customize configuration

See [Configuration Reference](https://cli.vuejs.org/config/).
