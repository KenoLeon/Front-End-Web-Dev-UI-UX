---
layout: post
title: Getting Started with React.js
excerpt: Follow me as I learn React.js with a series of live code examples.
permalink: /Getting-Started-With-ReactJs
---

<h2><b>Preface </b></h2>

<p>Getting Started in <strong>React.js</strong>, or any other javascript library or framework usually takes me a few hours or days of configuring my environment (downloading/updating node,npm,webpack,etc,etc) , while it is eventually necessary to build apps for deployment , I usually get a better feel and experience through writing code and seeing what happens, consulting the documentation and the occasional youtube tutorial along the way. </p>


<p>Thanks to CodePen, you can start right away learning in small bites and at least postpone setting up your environment while you figure out if this is something you want to get into, here are a few pens I made with a bit of commentary that helped me get my noodle wrapped around React.js. </p>  

 <h2><b>CodePen Setup: </b></h2>

 Setting up React was a breeze, from the JS Settings:

 * Babel as the Script Preprocessor (JSX to JS)
 * Quick add React & ReactDom

 I also added a Scss (Sass) preprocessor, but that's just in case I need to write some variables or what not in CSS.

 <h2><b>Hello World: </b></h2>

 So the idea behind React is firstly to mix JS and HTML and chuck them into a JS file ( or files) , all the Html you will need will be injected into a lonely HTML element, through the ReactDOM.render method which basically says this goes here.

 <br />

 <p data-height="340" data-theme-id="0" data-slug-hash="YWXqNd" data-default-tab="js,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/YWXqNd/">React Hello World No Component</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
 <script async src="//assets.codepen.io/assets/embed/ei.js"></script>

<h2><b>Hello World From a component: </b></h2>

All right, lets move hello world to a component, the building blocks of the React world :

<br />

<p data-height="340" data-theme-id="0" data-slug-hash="EyjKXQ" data-default-tab="js,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/EyjKXQ/">React Hello World Component</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>


<p>Now let's nest another component and style them both:</p>

<h2><b>Hello World from a styled Component</b></h2>

<p data-height="340" data-theme-id="0" data-slug-hash="EyjKwE" data-default-tab="js,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/EyjKwE/">React HW Nested Component</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

<p>Props are the next concept that is important to learn, a prop is basically an attribute of a component:</p>

<h2><b>Props:</b></h2>

<p data-height="340" data-theme-id="0" data-slug-hash="oLXxMm" data-default-tab="js,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/oLXxMm/">React HW Props</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

You can has default props:

<h2><b>Default Props:</b></h2>

<p data-height="340" data-theme-id="0" data-slug-hash="ezNEjJ" data-default-tab="js,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/ezNEjJ/">React HW Default Props</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

<h2><b>Prop Types:</b></h2>

Props can be defined within a component both for readability and validation, notice we are also using inline styles.

<p data-height="340" data-theme-id="0" data-slug-hash="gMpEZW" data-default-tab="js,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/gMpEZW/">React HW PropTypes</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

<h2><b>Passing Props:</b></h2>

Props can be passed from parent to child, this can come in handy when making complex components.

<p data-height="340" data-theme-id="0" data-slug-hash="VjLEbE" data-default-tab="js,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/VjLEbE/">React HW Transfer Props</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

<h2><b>Handling Events: </b></h2>

Before digging into State, let's figure out user interaction, a humble button and a click Handler that logs to the console for now.( also added Bootstrap to refine the presentation )

<p data-height="340" data-theme-id="0" data-slug-hash="EyjzEo" data-default-tab="js,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/EyjzEo/">React User Interaction</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

<h2><b>Almighty State: </b></h2>

What better way to demonstrate state than with a toggle button, notice that the state has no properties, it is just a bit of private logic within the component.

<p data-height="340" data-theme-id="0" data-slug-hash="vKOoXm" data-default-tab="js,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/vKOoXm/">React State</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

<h2><b>User Input: </b></h2>

A slightly more complex use of state with user input, in this case state does contain the input values.

<p data-height="340" data-theme-id="0" data-slug-hash="ZOGdEv" data-default-tab="js,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/ZOGdEv/">React Input</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

And that's it for now, hope this helps you get started.
<br />
<br />
Best,
<br />
<br />
Keno
