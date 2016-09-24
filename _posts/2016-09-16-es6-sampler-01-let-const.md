---
layout: post
title: 'ES6 Sampler #1 (let & const).'
excerpt: Let's sample what es6 has to offer with code samples and comparisons to es5, don't be shy, take a bite !
permalink: /es6-let-const
smlogo: Js.png
---

<div class="text-center"><img src={{ site.url }}"assets/images/JSLogo.jpg" alt="JavaScript"></div>

<h3>Preface</h3>

I've been using es6 more and more these days, I am also about to jump into typescript, while it is an interesting time to be a developer, it is also a little challenging to be juggling 3 (4 if you include Jquery) syntaxes for javascript, so in an effort to cement the knowledge I would like to do a few es5 to es6 code snippets before moving on.

<div class="Note"><b>Note: </b>Are you confused by the terminology ? I sure was, check out this post that explains it all: </div>

&bull;&nbsp;[ES5, ES6, ES2016, ES.Next: What's going on with JavaScript versioning?](http://benmccormick.org/2015/09/14/es5-es6-es2016-es-next-whats-going-on-with-javascript-versioning/){:target="_blank"}


<b>TL;DR: &nbsp;&nbsp; es5</b> = The Past/Present &nbsp;&nbsp;<b>es6 === es2015 </b> = The Bleeding Edge/Future


<div class="challenge"> <b>Challenges: </b> I gave myself little challenges you are welcome to try if you want to recreate my own learning curve.</div>

<h3>Variables (Let & Constant) </h3>

<div class="Note"><b>Note:</b> Technically, the following are statements and declarations, but you'd be surprised how many people (including myself) call them variables or variable types from time to time</div>

I guess the first thing to look into is variables, what kind of new magic variables does es6 add and when to use them ?

<div class="challenge"> <b>Challenge: </b>Learn and use the new es6 statement <b>let</b></div>


<p data-height="560" data-theme-id="0" data-slug-hash="NRNVwG" data-default-tab="result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/NRNVwG/">ES6 Sampler - let</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

As I understand it, <b>let</b> brings block scoping to Javascript, or in other words makes variable declaration less loosey goosey since now ( if you use let), you can make sure variables stay within your functions.

<h3>Constants</h3>

Another type of variable or declaration new to Javascript, is the Constant, let's try using it:

<div class="challenge"> <b>Challenge: </b>Learn and use the new es6 declaration <b>constant</b>&nbsp;&nbsp; ...<b>extra challenge:</b> Equivalent in es5 ?</div>


<p data-height="540" data-theme-id="0" data-slug-hash="GjqRJp" data-default-tab="result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/GjqRJp/">ES6 Sampler - const</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

<h3>TL;DR: let is the new var; there are now constants in Javascript</h3>


<div class="challenge"> <b>Extra Credits: </b>What is block scoping and variable hoisting ?...How do they work with let and Const ? </div>



Of course there is more nuance to using let and const,([Check the docs if you get stuck](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/let#Scoping_rules_2){:target="_blank"}), but this being a sampler, I hope at least you consider starting to use let and const ( with babel for now : mid-late 2016) in your projects.

Best,

Keno
