---
layout: post
title: 'ES6 Sampler #2 : Fat Arrows '
excerpt: Another look at es6, this time we check out arrow functions ( or fat arrows) and how to use them.
permalink: /es6-fat-arrows
smlogo: Js.png
---

<div class="text-center"><img src={{ site.url }}"assets/images/JSLogo.jpg" alt="JavaScript"></div>

<h3 class="fancy">Preface</h3>

This is the second in a series of posts where I explore all the new stuff es6 has to offer, come along and learn vicariously!

<div class="speechBubble"><b>Pssst...</b> You might also want to check the first one in the series:
</div>

[ES6 Sampler #1: (Let & Const)]({{ site.baseurl }}/es6-let-const){:target="_blank"}


<div class="challenge"> <b>Note - Challenges: </b> I gave myself little challenges you are welcome to try if you want to recreate my own learning curve.</div>

<h3 class="fancy">Let's start:</h3>

If you've used any recent js library or framework you might have stumbled upon fat arrows ( or arrow functions) that use the following syntax <b> => </b>

<div class="challenge"> <b>Challenge </b>Find out what an arrow function is and the equivalent in es5 </div>

<p data-height="680" data-theme-id="0" data-slug-hash="zKkLKK" data-default-tab="result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/zKkLKK/">ES6 Sampler - Fat Arrow pt1</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

Well ok then arrows seem to replace the function syntax , but how is that an improvement ?

<div class="challenge"> <b>Challenge </b>Find out why are arrow functions are an improvement...</div>

<div class="note"> <b>Note: </b>

There are a couple ways of using arrow functions :

<ul>

<li><b>(param1, param2, …, paramN) => expression </b> Single line, implicit return of expression  </li>
<li><b>(param1, param2, …, paramN) => { statements } </b> Multi Line, does not implicitly return anything, (ie you would need to return something)  </li>

</ul>

</div>

<b>Compact Syntax in anonymous functions</b>

<p data-height="470" data-theme-id="0" data-slug-hash="gwmjjq" data-default-tab="result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/gwmjjq/">ES6 Sampler - Fat Arrows pt2</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

<div class="note"> <b>Note: </b>Parentheses are optional when there's only one parameter:
 <ul>
<li><b>(singleParam) => { statements }</b></li>
<li><b>singleParam => { statements }</b></li>
</ul>
</div>

Anonymous functions (nameless functions for instance) are everywhere in javascript, with the arrow syntax you can ommit the word function.

<p data-height="560" data-theme-id="0" data-slug-hash="EgWzAj" data-default-tab="result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/EgWzAj/">ES6 Sampler - Fat Arrows pt3</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

Another very common instance, is the use of functions as arguments for other functions, with arrow functions the syntax can become somehow clearer.

<b>.this and scope with arrow functions</b>

Have you ever lost track of your global variables or wanted to use a local variable but couldn't figure out which <b>this</b> to use ? , arrow functions help by making things a little more concise, consider the following cases:

<p data-height="1000" data-theme-id="0" data-slug-hash="EgWqPQ" data-default-tab="result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/EgWqPQ/">ES6 Sampler - Fat Arrows pt4</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

<h3 class="fancy">Other uses</h3>

I personally believe in a verbose syntax when writing javascript to make things easy to a wider audience,but as more and more developers and libraries use newer features, it is important to at least know how to recognize what's being written, so I would like to finish this very small introduction to arrow functions with other cases one might encounter:

<div class="challenge"> <b>Challenge </b>Find other uses of arrow functions in the wild</div>

<b>Javascript methods with callbacks :</b>

<p data-height="500" data-theme-id="0" data-slug-hash="mAmqJq" data-default-tab="result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/mAmqJq/">ES6 Sampler - Fat Arrows pt5</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

<b>JQuery: </b>

<p data-height="620" data-theme-id="0" data-slug-hash="ALRarQ" data-default-tab="result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/ALRarQ/">ES6 Sampler - Fat Arrows pt6</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

<h3 class ="fancy">Conclusion:</h3>

The new es6 arrow syntax brings a more compact/clear way of writting functions, It also helps with scope in some cases, while using them is up to you, recognizing them is no longer optional, so it pays to learn them.

<h3 class="fancy"> TL&#59;DR: </h3>

<b>() => </b> You will learn to love me.


Best,

Keno
