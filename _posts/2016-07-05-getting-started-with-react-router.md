---
layout: post
title: Getting started with React Router
excerpt: Come along and learn React Router with simple code examples.
permalink: /getting-started-with-react-router
---

<h2><b>Preface</b></h2>

You want to learn React Router ?, I am learning React Router, come learn along :)

I recently had an epiphany : You can read the manuals or docs, or dive into some tutorial project code in hopes something might stick, but getting your hands dirty in small,incremental steps is more rewarding,even fun, and codepen is an ideal place to do so.

These pens are small code nuggets that follow my own learning, before each one I'll tell you what I set out to learn, the challenge I gave myself along with my learning experience, I believe by redoing my own challenges you too can learn, and if you get stuck you can always consult my own.

*Note: This is some intermediate React Stuff, check out my previous posts if you are just starting out:*


[Getting Started with React.JS]({{ site.baseurl }}/Getting-Started-With-ReactJs)

[More React.js pens]({{ site.baseurl }}/More-ReactJs-Pens)


<h2><b>What is React Router ?</b></h2>

I am not sure at this point, something to do with sending folks to different pages depending on where they click and using React Components along the way, that sounds about right.

<h2><b>React Router Home Route</b></h2>

First let's try setting up a home page, where a simple component will be displayed through react router:



>My/Your Challenge: Import react router and display a HomeComponent

<p data-height="340" data-theme-id="0" data-slug-hash="RRVEBr" data-default-tab="js,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/RRVEBr/">React Router Home Route</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

<h2><b>React Router Links</b></h2>

Well now let's see how we can send folks to different routes, or in this case different components and return them safely to the main page.

>My/Your Challenge: Create a home page with links to other pages/components and use the router to navigate to them and back

<p data-height="265" data-theme-id="0" data-slug-hash="bZRbWG" data-default-tab="js,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/bZRbWG/">React Router Links</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

<h2><b>Nesting Routes</b></h2>

But how would we reuse say a navigation bar ? is there a react-router way ?, let's find out:

>My/Your Challenge: Create a navigation bar with links to other components/pages with React Router

<p data-height="265" data-theme-id="0" data-slug-hash="BzkKrN" data-default-tab="js,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/BzkKrN/">React Router Nav</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

Ahhhh, so rendering Router allows you to treat it as a component and thus be able to nest children like any other component, it sounds a little confusing, but if you write the example above it becomes clearer how useful it can be.

<h2><b>Active Links</b></h2>

And how would one let know the components where they are ? let's investigate active links:

>My/Your Challenge: Create a navigation bar with active links

<p data-height="265" data-theme-id="0" data-slug-hash="OXgXOb" data-default-tab="js,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/OXgXOb/">React Router Active Links</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

React-router provides a handy active class or style flag to allow for active styles, neat.

<h2><b>Url params</b></h2>

As the name implies, urls can have specific params associated with them, so an user or section name could be used to inform the component by passing a param. it all sounds a little confusing, so let's try an example:

>My/Your Challenge: Create a navigation bar with links that include params and are used by a component

<p data-height="265" data-theme-id="0" data-slug-hash="RRgxoV" data-default-tab="js,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/RRgxoV/">React Router Params</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

The text style in the above example is set by the name param which is created in the fly in the navigation bar.

Like many things in the programming world, it makes more sense if you follow the param or variable around an look at how the system is set up, check the source, but it's utility should become apparent.

<h2><b>IndexRoute & IndexLinks</b></h2>

One issue you might have noticed, is that a navigation component can't call a Home or Index Route upon being loaded, an Index Route, and a corresponding IndexLink help to this purpose, to see the difference, you can add some text to our third example ( nesting routes) in the navigation component, it will repeat in each section, not something we want,so:


>My/Your Challenge: Create a navigation bar component, and both a home or index section and a couple of other sections and link them using the IndexRoute and Active Links

<p data-height="265" data-theme-id="0" data-slug-hash="rLwpoB" data-default-tab="js,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/rLwpoB/">React Router IndexRoute</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

So as you can see we now have the behavior most web pages with a menu structure require via components and routes, and more importantly a fairly good understanding of what React-Router does and how to get started using it.

There is of course more complexity and features to React-Router, but this being an introduction, I hope you at least get the gist of it.

I would recommend consulting the project page for more:

[React-Router on Github ](https://github.com/reactjs/react-router)

Best,

Keno.
