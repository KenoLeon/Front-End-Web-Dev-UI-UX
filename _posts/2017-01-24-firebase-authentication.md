---
layout: post
title: 'Getting started with Firebase Part 3. User authentication.'
excerpt: Firebase Offers multiple options for authenticating and tracking users through their API, join me in finding out more.
permalink: /firebase-user-authentication
smlogo: FirebaseSm.png
---
<div class="text-center"><img src="assets/images/firebase.png" alt="firebase"></div>


<div class="speechBubble"><b>Pssst...</b> Previous posts on this series:
</div>

- [Getting started with Firebase Part 1. Setting up.]({{ site.baseurl }}/firebase-settingup){:target="_blank"}
- [Getting started with Firebase Part 2. Real Time Database.]({{ site.baseurl }}/firebase-realtime-database){:target="_blank"}


<h3 class="fancy">Preface</h3>

User authentication is one of those web things that always gets me, I have probably written and used tens of libraries, some custom and some of the shelf, I am very curious to see how firebase deals with this subject of login,validating and keeping track of users, so let's check it out!

<div class="challenge"> <b>Challenge: </b> Find out how to use Firebase User Authentication </div>

The first thing to do, is to go to your trusty Firebase console and enable your preferred methods of authentication:

<img src="https://kenoleon.github.io/Front-End-Web-Dev-UI-UX/assets/images/postImages/Firebase/Firebase07.jpg" alt="Firebase">

Once that is done, you have 2 options; you can use their recommended prepackaged or Drop-in system (<a href="https://github.com/firebase/FirebaseUI-Web" target="_blank">Firebase UI</a>) or you can go custom and use the SDK, you can read more about these options here: <a href="https://firebase.google.com/docs/auth/web/password-auth#before_you_begin" target="_blank">API Reference</a>.

<div class="step"> <b>Option 1: </b> Authenticate with Firebases SDK </div>

I opted to start with creating an user with a very simple email password combination to start:

<p data-height="600" data-theme-id="27284" data-slug-hash="bgqXdz" data-default-tab="js,result" data-user="k3no" data-embed-version="2" data-pen-title="Firebase  Authentication  pt. 1 " class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/bgqXdz/">Firebase  Authentication  pt. 1 </a> by Eugenio  Keno   Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

It is of course not a production or complete alternative, but it is relatively easy to expand if you wish to go custom, let's now check the prepackaged option.

<div class="step"> <b>Option 2: </b> Authenticate with Firebase UI </div>

<p data-height="600" data-theme-id="27284" data-slug-hash="vgmmrY" data-default-tab="js,result" data-user="k3no" data-embed-version="2" data-pen-title="Firebase  Authentication  pt. 2  Firebase UI" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/vgmmrY/">Firebase  Authentication  pt. 2  Firebase UI</a> by Eugenio  Keno   Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

<div class="note"> <b>Note:</b> Firebase doesn't seem to like more than 1 instance on the same page, so you will need to provide your own credentials or un-comment mine on the pen, this is what it looks like:

<img src="https://kenoleon.github.io/Front-End-Web-Dev-UI-UX/assets/images/postImages/Firebase/Firebase08.jpg" alt="FirebaseUi Authentication">

</div>


The Drop-In alternative seems to work fairly well with the expected  caveat that you are somehow stuck with Material Design for the UI and their choice of authentication flow. You can change and tweak both by modifying options and the library, but at that point you might as well go with the sdk, all in all minor complaints.



<div class = "note"><b>Note:</b> Unfortunately only the email sign-up option works within codepen, for the rest to work you would need to request api keys and authorization from the providers , additionally, some do not allow iframes and have cors security issues, all I am saying is that these problems are due to me just making an example inside a web editor and not a real App, so it shouldn't be an issue for you.</div>

<h4 class="fancy">Tracking users: </h4>

<p data-height="600" data-theme-id="27284" data-slug-hash="GrmwwM" data-default-tab="js,result" data-user="k3no" data-embed-version="2" data-pen-title="Firebase  Authentication - Tracking Users" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/GrmwwM/">Firebase  Authentication - Tracking Users</a> by Eugenio  Keno   Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

<div class="note"> <b>Note:</b> As mentioned before, You will need to run the pen  and un comment my  Firebase Credentials or replace them with yours for the code sample to properly run</div>

The above code should render the following authentication flow:

<img src="https://kenoleon.github.io/Front-End-Web-Dev-UI-UX/assets/images/postImages/Firebase/Firebase09.jpg" alt="FirebaseUi Authentication Flow">

Tracking the user is then a matter of keeping a reference to the **userId or token** made available by other authorization providers (facebook, google,etc) and listening for changes with :
<code>firebase.auth().onAuthStateChanged</code>.

<div class="note"> <b>Note:</b>Upon creating a user with Firebase UI email & password, a First & last name is requested, and stored as part of the user object, this object and it's properties change based on the provider, if you need to store specific information then you will have to store it on your firebase database read more about this here : <a href="https://firebase.google.com/docs/auth/users" target="_blank"><b>Users in Firebase Projects</b></a></div>

<h4 class="fancy">Conclusion: </h4>

Firebase Authentication is a mixed bag of awesome,compromises and plenty of options, I barely scratched the surface of the complexity that the API and SDK provide,as such it is still a bit on the complex side,Authentication is still not easy :( on the other hand, if you want to add authentication to your project in a few hours, you can easily do it by using the drop-in option provided you are ok with their flow and UI, as I mentioned something of a compromise, but hard to find an alternative.


Best,

Keno
