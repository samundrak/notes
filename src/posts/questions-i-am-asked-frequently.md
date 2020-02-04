---
layout: layouts/post.njk
title: Questions I am asked frequently
date: 2020-02-04T16:29:33.956Z
tags:
  - questions
  - ''
---
## Q1. What is the benefit of using a library like React/Vue/Angular vs using plain old JavaScript? What is your experience level with one of those frameworks?

If we see it from a business and personal perspective then using a library like React/Vue/Angularjs over JavaScript are :

Data over DOM: With a UI library like React or framework like Vue/Angular I don’t have to think of DOM and explicitly manipulate DOM or maintain a state to track changes of DOM, instead I will be seeing an application as state and develop a full application following it. A state of an application is a blueprint and we will be working on data over DOM which will be abstracted away from us by library/framework mentioned above.



** Productivity ** We don’t have to stuck on things which are already been solved with the best practice, fix bugs which already has been solved years ago, reinvent every chunk which has been already created, instead we can actually focus on application logic and deliver application faster.



**Performance**: Performance always matters in a competitive market, if we are delivering application faster but not with performance then it doesn’t add much value to our application because everyone hates slow application which directly or indirectly affects business. We can always write a performant library with our own plain old javascript only if the provided library doesn’t meet our requirement or have enough time to write else the widely used library is already battle tested on a big application on production.



** Community **: If a library has very less community support then it's good to use plain old javascript because we may reach to point where we are on dead end and there is no support for it. I would always go first for the power of library and the community it has so that in future I don’t have to regret selecting library. Working with the community will always help me become up to date with current trends, tech stacks, code convention, and quality.



I have worked with all three libraries mentioned above (React/Vue/Angular), I have listed below my experience with these libraries:

** Angular 1.x **: Started working with Angular 1.x from my first job, where I developed an application (CRM) where backend was on Nodejs and frontend AngularJS.It was a single page application.



** Vue **: Worked with Vue on my second job where I completely rewrote frontend of big CRM, where previously it was fully developed by jquery though less part was done on frontend most used to be handled by the backend (Laravel). I rewrote the whole application and converted it into a multi-single page application making it up to date with current trends and stacks maintaining company’s requirement. (agentcis.com)



** React **: I have worked with React for almost 2 years from pet project to professional project. Currently, I am working with React on 2 projects a plugin and realtime web app.





## Q2. When is CORS needed and how does it work in the browser?

We use CORS whenever we have to communicate from one origin to another origin.

Whenever we try to connect with any other host than we are served then browser first send a preflight request and check if the current requesting host is included in header tag \`Access-Control-Allow-Origin\` and if requesting host is mentioned or a wildcard(*) is in value then

A request is valid and it is dispatched to the target host.



## Q3. What is an XSS attack? Explain what can lead to one and how can it be prevented?

XSS attack is where a malicious user can run their malicious code and steal or access confidential data of the victim. On the Internet, we should never trust any input from a user which can lead us to XSS. If we don’t sanitize user input and

insert any raw input from the user into the output and if the input contains any scripts which can be executed on the user’s machine. So to prevent this we should always sanitize and escape

User input.



## Q4. Tell us about your latest "hard to debug" problem. How did you resolve it? Which tools did you use?

I have no latest “hard to debug” problem, maybe I haven't got a chance to work on that challenging project, but once I was in a situation when I was working on the module with multistep and I didn’t use state management well.

There I just distributed state on components and didn’t follow the single source of truth which took me in a very bad situation and caused a huge memory leak,

after a lot of debugging and breakpoints I came to know how badly I have structured my application state. After that, I understand the real world experience of following the single source of truth, (props down, events up). The stacks were Vue and later I added

Vuex for state management and re-architect my application to resolve it.



Recently I worked on an application (Frontend/Backend) where a user can transfer their web files to cloud storage(Google Drive), it can be multiple and while transferring file, the application need to show the progress of transfer, it can multiple so a page can have multiple progress of different file,

We get the progress of files from the server every second so if a user removes an item but the progress of that file is already dispatched and but when it goes for updating the item is already deleted which caused the massive error and sometimes it is used to display the progress of invalid file because of indexing.



## Q5. Tell us about your most advanced/exciting/mind-blowing JS/CSS implementation

I will say “domex”(https://github.com/samundrak/domex) its

a library where we can use the power of the routing feature of “ExpressJS”

On browser and have a route which we can call internally to make one-way data flow.

I extended it more and made “domex-redux” which help me work with redux

without writing actions/reducers instead I will just define a route where I will

hit whenever any event occurs in a page(click, hover’) with a

request body. (<https://github.com/samundrak/domex-redux>).

A full example of domex and domex-redux: https://github.com/samundrak/bhitte-patro
