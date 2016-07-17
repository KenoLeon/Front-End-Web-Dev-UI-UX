---
layout: post
title: More React.js Pens
excerpt: More beginner and not so beginner React.js code samples to continue learning.
---

<h2><b>Preface</b></h2>

This is an ongoing series on React, check out the first part here:

[Getting Started with ReactJs]({% post_url 2016-06-06-getting-started-with-reactJs %})

So let's get started where we left off, in this case we want to validate an input form before submitting the information upstate, a combination of state,form elements & bootstrap UI display takes care of the interaction, so in the end the component is fairly independent.

<h2><b>React Form Submit Validation</b></h2>

<p data-height="340" data-theme-id="0" data-slug-hash="KMdMpq" data-default-tab="js,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/KMdMpq/">React Form Submit Validation</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

Before going any further, we need to take a look at a components lifecycle, there are more stages in a component's life, but these few I think are enough to get the concept across ( open your console for this one) :

<h2><b>React Component lifecycle</b></h2>

<p data-height="340" data-theme-id="0" data-slug-hash="xOZGaP" data-default-tab="js,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/xOZGaP/">React Component Lifecycle</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>


<h2><b>Iterating over an array in React</b></h2>

Another common thing you might find yourself doing is Iterating and rendering the contents of an array, here's a simple one.

<p data-height="340" data-theme-id="0" data-slug-hash="YWwEWg" data-default-tab="js,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/YWwEWg/">React  Iterating over Array</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

<h2><b>Data flow in React</b></h2>

Now that we know how to iterate over an array, let's talk about data flow, specifically from child to parent, while a parent communicates through props to it's children, a child can communicate through a function passed as a prop as well:

<p data-height="340" data-theme-id="0" data-slug-hash="vKLvPm" data-default-tab="js,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/vKLvPm/">React  Data Flow</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>


<h2><b>Dynamic Components in React</b></h2>

But what if you want to create components on the fly, here's a simple way of creating components in a for loop that incorporates the previous data flow pattern.

<p data-height="340" data-theme-id="0" data-slug-hash="QENwbq" data-default-tab="js,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/QENwbq/">React  Dynamic Components</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>


<h2><b>Dynamic CSS styles in React</b></h2>

Another thing you might want to change on the fly is css styles, in this case with a custom component method.

<p data-height="340" data-theme-id="0" data-slug-hash="gMrKbX" data-default-tab="js,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/gMrKbX/">React  Dynamic CSS Styles</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>


<h2><b>Css Transitions in React</b></h2>

This one took me a little longer to figure out, but basically you can incorporate Css transitions into your components life cycle, check it.

<p data-height="340" data-theme-id="0" data-slug-hash="vKKJmY" data-default-tab="js,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/vKKJmY/">React  CSS Transitions</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>


<h2><b>Ajax Call in React</b></h2>

Getting close to a good basic understanding of React, here is the all too popular Ajax call which happens inside a component, which in turn could call other components to display and format it.

<p data-height="340" data-theme-id="0" data-slug-hash="bewEpE" data-default-tab="js,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/bewEpE/">React Ajax Call</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>


<h2><b>Using Bind in React, more data flow</b></h2>

I wanted to revisit the data flow example,now with communications from a child to a parent and child to a parent's parent, also using bind as an alternative way of passing a function as a prop.

<p data-height="340" data-theme-id="0" data-slug-hash="NrRpJg" data-default-tab="js,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/NrRpJg/">React Bind</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

Best,

Keno
