---
layout: post
title: 'ES6 Sampler #4 : Spread ... '
excerpt: Following up on a series of ES6 code samples, let's check what the spread syntax ( ... ) does!
permalink: /es6-spread
smlogo: Js.png
---

<div class="text-center"><img src="assets/images/JSLogo.jpg" alt="JavaScript"></div>

<h3 class="fancy">Preface</h3>

<div class="speechBubble"><b>Pssst...</b> Previous ES6 Samplers
</div>

- [ES6 Sampler #1: (Let & Const)]({{ site.baseurl }}/es6-let-const){:target="_blank"}
- [ES6 Sampler #2: (Fat Arrows)]({{ site.baseurl }}/es6-fat-arrows){:target="_blank"}
- [ES6 Sampler #3: (Classes)]({{ site.baseurl }}/es6-classes){:target="_blank"}


<div class="challenge"> <b>Note - Challenges: </b> I gave myself little challenges you are welcome to try if you want to recreate my own learning curve.</div>

<h3 class="fancy">Let's start:</h3>

I've been bitting my nails for this one, The spread syntax  <b>...</b> is all kinds of awesome, but what is it and what does it replace ?

<div class="challenge"> <b>Challenge: </b> Find out what the spread syntax does and what it replaces</div>

<div class="note"> <i>From the docs - </i>
 Syntax for function Calls:  <br/>
 <b> myFunction(...iterableObj);</b>
</div>

<p data-height="900" data-theme-id="0" data-slug-hash="dpqoEo" data-default-tab="result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/dpqoEo/">ES6 Sampler - Spread Operator Pt1.</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>


More than anything, the spread syntax brings clarity and a cool way of using enumerable arguments in a function call.
There seems to be more, you can also use them in array literals, but what does that entail...

<div class="challenge"> <b>Challenge: </b> Find out how to use the spread syntax in a Array Literal and it's counterpart in es5</div>


<div class="note"> <i>From the docs - </i>
 Syntax for array literals:  <br/>
 <b> [...iterableObj, 4, 5, 6]</b>
</div>

<p data-height="1300" data-theme-id="0" data-slug-hash="ORoxyP" data-default-tab="result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/ORoxyP/">ES6 Sampler - Spread Operator Pt2.</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

Notice that depending how you use those 3 dots it is either a spread ( wave your hand like you are spreading something on bread), or Rest ( as in the rest of), Operator.


<div class="challenge"> <b>Challenge: </b> Find out other uses of the spread syntax</div>

<p data-height="1100" data-theme-id="0" data-slug-hash="zKmGrJ" data-default-tab="result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/zKmGrJ/">ES6 Sampler - Spread Operator Pt3.</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

One of the coolest things you can do with the dots, are Rest Parameters, so you can  define a function with an unlimited/unknown  number of parameters.

<h3 class="fancy">All together now: </h3>

<div class="codingTest"> <b>Coding Test: </b> Use the spread syntax in a function call,array literal and with function parameters <br/>
</div>

<p data-height="600" data-theme-id="0" data-slug-hash="BLqbNQ" data-default-tab="result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/BLqbNQ/">ES6 Sampler - Spread Operator Pt4</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

<h3 class="fancy">Conclusion</h3>

You can use the spread syntax to simplify your javascript in a lot of places and cases, each one has it's nuances, but overall make writing clear JS easier.

<h3 class="fancy"> TL&#59;DR: </h3>

<b>Spread Syntax has many faces all of them are useful</b>

Best,

Keno.
