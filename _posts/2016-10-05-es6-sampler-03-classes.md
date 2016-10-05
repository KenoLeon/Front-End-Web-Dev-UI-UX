---
layout: post
title: 'ES6 Sampler #3 : Classes'
excerpt: Another look at what ES6 has to offer, this time let's look at classes.
permalink: /es6-classes
smlogo: Js.png
---

<div class="text-center"><img src={{ site.url }}"assets/images/JSLogo.jpg" alt="JavaScript"></div>

<h3 class="fancy">Preface</h3>

This is the third in a series of posts where I explore all the new stuff es6 has to offer, come along and learn about classes.

<div class="speechBubble"><b>Pssst...</b> You might also want to check the first 2 in the series:
</div>



- [ES6 Sampler #1: (Let & Const)]({{ site.baseurl }}/es6-let-const){:target="_blank"}
- [ES6 Sampler #2: (Fat Arrows)]({{ site.baseurl }}/es6-fat-arrows){:target="_blank"}

<div class="challenge"> <b>Note - Challenges: </b> I gave myself little challenges you are welcome to try if you want to recreate my own learning curve.</div>

<h3 class="fancy">Let's start:</h3>

ECMAScript 6 introduces the class syntax, I suppose the first thing we would need to figure out is what does it replace or it's equivalent in es5, so.

<div class="challenge"> <b>Challenge: </b>Find out what a class does and the equivalent in es5 </div>

<p data-height="980" data-theme-id="0" data-slug-hash="LRzJmj" data-default-tab="result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/LRzJmj/">ES6 Sampler- Classes pt1</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

In a nutshell, if you already know about prototypes you alaready know how a class works, it is basically  syntactical sugar (a more readable or convenient way) to deal with objects and inheritance.

<h3 class="fancy">How many ways ?</h3>

This being a programming language, there is nunance and variation when defining a class, so..

<div class="challenge"> <b>Challenge: </b>Figure out the different ways of defining a class in es6 </div>

<p data-height="860" data-theme-id="0" data-slug-hash="EgwONA" data-default-tab="result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/EgwONA/">ES6 Sampler- Classes pt2</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

<b class="fancy">Class Methods</b>

A lot of what makes an object useful is the internal machinery as I like to call it or Methods as most people do, let's figure out how to make some methods with es6 classes:

<div class="challenge"> <b>Challenge: </b>Find out how methods work with es6 classes</div>

  <p data-height="840" data-theme-id="0" data-slug-hash="ozozBB" data-default-tab="result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/ozozBB/">ES6 Sampler- Classes pt3</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

<b class="fancy">Extending Classes</b>

Another handy thing one can do with classes is extending them so they add or change behaviour from a base class (or prototype) , let's try that:

<div class="challenge"> <b>Challenge: </b>Find out how to extend a class in es6 </div>

<p data-height="640" data-theme-id="0" data-slug-hash="rrYymE" data-default-tab="result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/rrYymE/">ES6 Sampler- Classes pt4</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

<b class="fancy">Calling super</b>

One last things we must investigate, is how does one refer to the original class within an extended class?

<div class="challenge"> <b>Challenge: </b>Find out how to use super in es6</div>

<p data-height="960" data-theme-id="0" data-slug-hash="amVAjE" data-default-tab="result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/amVAjE/">ES6 Sampler- Classes pt5</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

And that's it, a quick overview of what classes bring to Javascript; One last thing I would like to start doing, is leaving a final challenge, one you might encounter on a coding test, so let's try that:

<div class="codingTest"> <b>Coding Test: </b>Create a class with at least 2 methods, extend it and use super to call one of the methods. <br/><br/>
<b>Extra Credit: </b> Create the same functionality in es5.</div>

<p data-height="1340" data-theme-id="0" data-slug-hash="xEpKrj" data-default-tab="result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/xEpKrj/">ES6 Sampler- Classes pt6</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

<h3 class="fancy">Conclusion</h3>

Classes in es6 while being syntactic sugar, are a welcome adition if you considered protoype chaining and inheritance a bit cumbersome, what's more, it aligns javascript with other languages that use classes.

<h3 class="fancy"> TL&#59;DR: </h3>

<b>Classes in es6 = delicious prototype/inheritance sugar </b>

Best,

Keno.
