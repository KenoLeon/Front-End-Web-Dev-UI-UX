---
layout: post
title: 'Getting started with Firebase Part 2. Real Time Database.'
excerpt: One of the coolest things Firebase does, is provide you with access to a real time database for your projects, let's take a look.
permalink: /firebase-realtime-database
smlogo: FirebaseSm.png
---
<div class="text-center"><img src="assets/images/firebase.png" alt="firebase"></div>


<div class="speechBubble"><b>Pssst...</b> Previous posts on this series:
</div>

- [Getting started with Firebase Part 1. Setting up.]({{ site.baseurl }}/firebase-settingup){:target="_blank"}

<h3 class="fancy">Preface</h3>

Perhaps the most important feature ( along with authentication) that firebase provides is a real time database, let's check out what it is and how to use it:

<div class="challenge"> <b>Challenge: </b> Find out how to use Firebase Real Time Database </div>

Setting up the database is fairly straightforward, you will first need to configure your app to point to your own Firebase account:

![Firebase Setup 001](https://firebasestorage.googleapis.com/v0/b/codepen-b4abb.appspot.com/o/images%2Ffirebase001.jpg?alt=media&token=2fd83a0f-e40b-4c38-9ef1-745ca62480ae)

After that, you need to modify your access rules, while it is a bad idea to let anyone read and specially write to your database, while developing ( we don't have any users yet) it makes things easier:

<img src="https://kenoleon.github.io/Front-End-Web-Dev-UI-UX/assets/images/postImages/Firebase/Database01.jpg" alt="Firebase">

<b> Writing Data: </b>

<p data-height="600" data-theme-id="0" data-slug-hash="gLmBBy" data-default-tab="result,js" data-user="k3no" data-embed-version="2" data-pen-title="Firebase  Database pt 1. " class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/gLmBBy/">Firebase  Database pt 1. </a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

The above code writes a random number to the database, you can see it change live from your firebase console once you connect it to your account:

<img src="https://kenoleon.github.io/Front-End-Web-Dev-UI-UX/assets/images/postImages/Firebase/Database02.jpg" alt="Firebase">

Further examples and reference from the Docs:
<a href="https://firebase.google.com/docs/reference/js/firebase.database.DataSnapshot" target="_blank"><b>firebase.database.DataSnapshot</b></a>




<b> More Security: </b>

At this point it is good practice to rework our database rules, so only numbers can be written, there is an [extensive section on
<a href="https://firebase.google.com/docs/reference/security/database/#validate" target="_blank"><b>validating</b></a> in the Firebase Docs and even a simulator in your console,so you can test rules, this is one of the simplest validations you can make and it will only accept numbers for our specific case.

<img src="https://kenoleon.github.io/Front-End-Web-Dev-UI-UX/assets/images/postImages/Firebase/Database03.jpg" alt="Firebase">

<b> Reading Data: </b>

The magic of Firebase Real Time database will hopefully be illustrated by the following sample, instead of reading data on demand, Firebase can be configured to subscribe to updates, (<a href="https://firebase.google.com/docs/database/web/read-and-write" target="_blank"><b>you can still read on demand from the database if you wish</b></a>, so if someone else modifies the database your app will be notified and can update it's own state, if you click the button on this app, the number will change and any other pages running it will be updated automagically !


<p data-height="600" data-theme-id="0" data-slug-hash="qqVGmw" data-default-tab="js,result" data-user="k3no" data-embed-version="2" data-pen-title="Firebase  Database pt 2. " class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/qqVGmw/">Firebase  Database pt 2. </a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

Here's what that would look like when you connect it to your account:

<img src="https://kenoleon.github.io/Front-End-Web-Dev-UI-UX/assets/images/postImages/Firebase/Database04.jpg" alt="Firebase">

<b>Working with more Data</b>

Unlike traditional relational databases (mysql,SQL) Firebase stores the schema, rules and data as a JSON object, a full overview is beyond this short introduction, but you can check their documentation for more:
<a href="https://firebase.google.com/docs/database/android/structure-data" target="_blank"><b>Structure your Database</b></a>


What we want to do now, is create a click counter and update it at the same time we write our number, here is the result:

<p data-height="600" data-theme-id="0" data-slug-hash="qqpYqP" data-default-tab="js,result" data-user="k3no" data-embed-version="2" data-pen-title="Firebase  Database pt. 3 " class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/qqpYqP/">Firebase  Database pt. 3 </a> by Eugenio  Keno   Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

Here's what that would look like along with the new database scheme:

<img src="https://kenoleon.github.io/Front-End-Web-Dev-UI-UX/assets/images/postImages/Firebase/Database05.jpg" alt="Firebase">

With a new database scheme, we also now need to validate our new clicks field, enter new validation rules:

<img src="https://kenoleon.github.io/Front-End-Web-Dev-UI-UX/assets/images/postImages/Firebase/Database06.jpg" alt="Firebase">

Notice how we have changed the validation rules based on our new database schema.


<b>And finally a live example !</b>

<p data-height="600" data-theme-id="0" data-slug-hash="BQYrGY" data-default-tab="result" data-user="k3no" data-embed-version="2" data-pen-title="Firebase  Database pt. 4 " class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/BQYrGY/">Firebase  Database pt. 4 </a> by Eugenio  Keno   Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>


<h3 class="fancy">Conclusion</h3>

Firebases realtime database is both awesome and a little tricky to get at first, while I used very simple but hopefully expandable code samples, you will most likely use it in conjunction with User Authentication or more meaningful data schemas,so this brief review only covered the bare basics, still I came away impressed by how simple it is in the end, and the wow factor of real time updates.

Best,


Keno
