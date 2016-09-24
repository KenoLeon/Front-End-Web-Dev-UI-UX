---
layout: post
title: Getting started with Redux
excerpt: I investigate what Redux is with a series of easily digested code samples come along...
permalink: /getting-started-with-redux
smlogo: Redux.png
---

<h2><b>What is Redux ?</b></h2>

Good question, the plan is to figure out what Redux is and how it works through a series of pens that follow my learning; before each one I gave myself a little challenge which you can use to learn on your own, so come along.

Before we get started, I should mention that Redux seems to work with frameworks other than React, but I am learning it along React. If you are just getting started check out my other posts on React.js:


* [Getting Started with React.JS]({{ site.baseurl }}/Getting-Started-With-ReactJs)

* [More React.js pens]({{ site.baseurl }}/More-ReactJs-Pens)

* [Getting started with React-Router]({{ site.baseurl }}/getting-started-with-react-router)


<h2><b>The General Idea with Redux</b></h2>

**React.js** helps you make efficient applications with components, but as they tell you mostly serves as the View, *the presentation layer*, then along came [FLUX](https://facebook.github.io/flux/) a pattern for dealing with state, *The logic Layer* and then [REDUX](https://github.com/reactjs/redux) [a simplificatin of Flux](http://redux.js.org/docs/recipes/ReducingBoilerplate.html), so let's see how Redux fits in with React with a pen:

> *My/Your challenge: Import Redux and display a React component using redux... Hint: you will need a store.*

<h2><b>Redux Store</b></h2>

<p data-height="340" data-theme-id="0" data-slug-hash="pbwmdg" data-default-tab="js,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/pbwmdg/">React Redux Store</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

After a little head scratching, I think I got a very basic example of a redux implementation, or at least a **Store** which contains the state ( a function), I also figured out how to get the current state with **getState()** which in turn can be passed to a React component,so things look promising. According to the documentation, you need [Actions](http://redux.js.org/docs/basics/Actions.html) to send information and   change State, so let's figure out those next.

> *My/Your challenge: Figure out what is an action and use it to change the state.*

<h2><b>Redux Actions</b></h2>

<p data-height="340" data-theme-id="0" data-slug-hash="grxgbV" data-default-tab="js,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/grxgbV/">React Redux Actions</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

Well that was interesting, some initial setup needs to happen to change and read state, so let's see, the store can now change state based on actions,in order to change state, an action is dispatched (from a button component in this case) , the hardest part was syncing the main component to changes in the store, this is done by subscribing to the store and forcing a re render, but I believe I got what an action is, let's check out reducers next.

>*My/Your Challenge,Figure out what a reducer is and use it.*

<h2><b>Redux Reducers</b></h2>

<p data-height="340" data-theme-id="0" data-slug-hash="YWxJoJ" data-default-tab="js,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/YWxJoJ/">React Redux Reducer</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

A **[Reducer](http://redux.js.org/docs/basics/Reducers.html)** turns out is simply a way of getting state out of actions by  applying some logic, while at it's basic this logic can be dealt with an else if statement, there is a bit more nuance to it, namely a set of rules for reducers like immutability and a more complex state (dealt with objects), let's dig into those next.

>*My/Your Challenge: Figure out what is immutability and create a reducer for complex state that doesn't mutate... Yawzhaa!*

<h2><b>Immutability in Redux</b></h2>

<p data-height="340" data-theme-id="0" data-slug-hash="wWAzQy" data-default-tab="js,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/wWAzQy/">React Redux Immutable Reducer</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

Couple of things going on in the last pen, we upgraded the reducer to work with objects so more complex state can be represented, we also changed the Reducer to a switch statement with an initial object value, and to comply with **immutability,** we are cloning the state object. In the end we return a new object (*After every single click*)thus not changing the existing state. Why ? it just keeps you honest by a) not allowing any other part of your script to modify your state directly thus making your code consistent and easier to debug, and b) allows for easier tracking of changes.

Moving on, since we are working along React, let's figure out how to convert state changes to props


<h2><b>React-Redux:</b></h2>

> My/Your Challenge: Figure out how to convert state changes to props using React-Redux, connect() and container & presentational components... oh my, this is a little too much to eat in one sitting, so let's break it down:

<h2><b>Container & Presentational components:</b></h2>

> Sub Challenge:  Create a Container Component and a Presentational Component in React

<p data-height="340" data-theme-id="0" data-slug-hash="JKAAQA" data-default-tab="js,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/JKAAQA/">React Redux: Presentational &  Container Components</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

The above pen is a minimal example of React-Redux, instead of manually subscribing to the store's state with a Container Component, connect produces a component with props generated from state that is also subscribed to the store, a Presentational Component, let's expand on this subject by mapping to specific props just a part of state:

> Sub Sub Challenge : connect parts of state to specific props

<p data-height="340" data-theme-id="0" data-slug-hash="rLYVbV" data-default-tab="js,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/rLYVbV/">React -Redux: mapStateToProps</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

Through changes in the mapStateToProps function, we now only pass down the props we need our presentational component to be aware off, neat. We still need to deal with the other half of the interaction, dispatching actions through React-Redux, let's investigate:

> New Challenge : Dispatch Actions and change state through React-Redux

Let's start by Manually dispatching and only connecting mapStateToProps...

<p data-height="340" data-theme-id="0" data-slug-hash="VjAZWw" data-default-tab="js,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/VjAZWw/">React -Redux: MapDispatchToProps pt. A</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

And using React-Redux

<p data-height="340" data-theme-id="0" data-slug-hash="RRjABR" data-default-tab="js,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/RRjABR/">React -Redux: MapDispatchToProps pt. B</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

The same Dispatch is now handled by mapDispatchToProps, and the presentational component can call a prop on click events, double neat : )

<h2><b>Bringing it Home</b></h2>

With this new understanding, let's try a more complex app with a complex state tree, and multiple action dispatches.

> Final Challenge : Create a more complex app using Redux and Redux-React

<p data-height="340" data-theme-id="0" data-slug-hash="NAwNPr" data-default-tab="js,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/NAwNPr/">React  + Redux + React-Redux</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

This last pen was probably the hardest, I started with a more ambitious app, but I pared it down (reduced ?) since I started having issues creating and accessing a bigger State Tree, in order to advance in the Redux world, I believe an intermediate understanding of React/ Redux is needed ( along with good ES6/JSON chops) and a few other things. For now, I am happy where this post has taken my understanding of Redux, I hope this helps you as well.

Till Next Time.

Best,

Keno
