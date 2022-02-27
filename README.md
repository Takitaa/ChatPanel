
## Practical Info

> Branches
- main : JS env original (general readme)
- dev : dev environemnt for main
<br>
 
- devTS dev environement TS and currently working branch⚠ (dedicated readme)
- devTSprod : "main" of devTS where app will be deployed
<br>

> Emojis

📌 pain points<br>
🍀 hope / luck
<br>
<br>

## The Beginning


### Challenged to create a chat-sidepanel with the following aspects:

> 1. Please create a new VueJS (1.x latest) project as repo on github.
  - a. DONE use typescript! for the project!!
<br>

## Project setup

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
```
Not found
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

### Added Typescript plugin using Vue UI
### VS Vetur extension
<br>

  -  b. DONE add "itsatony" as a collaborator to the project.<br>
      Adding was easy but quite a lot of time refreshing Git/Github skills and seting up Git-Github pushs and best pull practices due to lack of experience working with the tool and in a team that relies on it. 📌

  -  c. DOING create a USEFUL README please. explain what you did. what was problematic and why. how you approached the tasks and solved them.<br>
      I first opted for a descriptive README - the human touch however, having the feeling that the essential info was getting lost, I decided to keep my verbose in the dev branch - where out of the box thinking (aka craziness) is allowed, right?
   
  -  d. DOING ideally, commit whenever it seems reasonable to you - imagine you're working in a team of 4+ developers on this project. 📌
  <br>

> 2. The application should show a video-player + chat-sidepanel layout. 
   The chat-sidepanel should be aligned right in a container with a max width of 350px and a min-width of
   300px. Take inspiration from this: [https://webclient.spect8.me/demo.html] (https://webclient.spect8.me/demo.html)   
> 3. Add a video-player to the main container (play any public video - you can re-use the one
   we use).

   As my VUE knowledge was not completed (lack of Components/Props), I searched to progress with my first and only Vue contact and [video course](https://www.udemy.com/course/vuejs-2-the-complete-guide/) in order to cover missing points. 
   <br>
   
   Theoretically everything seems doable, hands-on not quite to the point I forgot how to do stuff and the meaning of simple things. I got trapped in a rabbit hole, finding many sources for the questions that would pop up, I decided to jump to what I thought I knew: the toggle button (item 5).
   <br>
   
   French would say, too much information, kills the information and I agree.
   <br>
   
   On the top of the challenge, there is a layer of I must learn fast combined with what I need to learn (information, information, information + time to digest the information, as in practice and settle it in my mind) and this refrains my progress📌
   <br>
   
   Same happened to me when dealing with Javascript  and coincidentaly enough, as it happened back then, searching for a way to <ins>consolidate</ins> my knowledge and make sense of the pieces of information I have, I found a French 🇫🇷 [step-by-step didactical tutor] (https://www.udemy.com/course/vuejs-tutorial/) who give proper names (easy digestable) to things - also he allows PrintScreens of his code: as a visual person and normally watching courses on my phone (because of the practicity of taking printscreens for example and how easy it is to go through the images as I code along on my desktop), this helps a lot!
   <br>
   
   There is hope! 🍀
<br>
   UPDATE from <ins>DAY 5</ins> Progress has been made as I realised the VueJS  version asked for the app was <ins>1.x</ins>!! 🥴🥴🥴🥴🥴 (walking backwards from the future gave me an advantage though as I could understand the progress implemented to version 1.0.
<br>

   I wanted to mention before about documentation and versions having found little for Vue 3 and much for Vue 2 📌  A new world and challenge was presented by having to work with Vue 1 but now I understand extremely better the Async call and backend Mock - were you meaning tests with this? Yes or Not, I learned about Jest against Karma-Mocha (choice for Vue projects at this point - it seems).
<br>

  A brand new enviroment was deployed, I was creating a new branch to upload it when I realised the Vue 3 environemnt would be there, so I found out about submodules and will deploy it to GitHub tomorrow (Monday 27 feb).
  
  <br>
  
  I'm getting more hand of the enviroment as I'm having to do things again and again 🤗
  
  <br>
  
  For the records, I can create a user input with a submit button .- at least in Vue 3 😅 And I'm noticing difficulty - now that I'm working with just one file (App.vue) and the need for Component - to link/register one thing to the other, so still working on one file and not finding it so straight forward as I know it can be.🤓
  
  <br>
  
  Lastly, I will also get in touch with the team tomorrow, I didn't before because my issues were due to lack of knowledge so questions would be more on a how to basis which I don't believe would answer the purpose of the challenge.

> 4. Add a button for "theatre-mode" where the video + chat-sidepanel go into fullscreen
   mode.<br>
   
   <ins>DAY 5</ins> The video has a fullscreen, I would say 40% done for this task 4.
   <br>
   <br>
   
   
> 5. Add a slide-in + slide-out button to the chat-sidepanel. This should work (animated) both
   in full-screen mode and normal mode.The video-size should adapt according to the
   sidepanel status (out/in/sliding animation).
   
   I decided to start here and my world crumbled as my perfect button done with vue-toggle does not seems to be so stratight forward or even working. 📌
   So I tried task 2. and 3.
   <br>
   <ins>DAY 5</ins> I added a button that would have come with a sidepanel but the style were in sass and with the Vue 1 version I could not pass the issue with Vue Ui as the system is older than required for such a fancy UI.
   <br>
   <br>

6. add an input field to the bottom of the chat-sidepanel with a submit button and a
   emoji-selector (use any available plugin you like).
   <br>
   

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



### Customize configuration

See [Configuration Reference](https://cli.vuejs.org/config/).
