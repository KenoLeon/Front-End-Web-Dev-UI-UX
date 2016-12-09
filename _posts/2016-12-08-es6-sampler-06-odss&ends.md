---
layout: post
title: 'ES6 Sampler #6 : Odds & Ends '
excerpt: Final part of a series on the new features of Javascript's ES6 Some odds & ends.
permalink: /es6-promises
smlogo: Js.png
---

<div class="text-center"><img src="assets/images/JSLogo.jpg" alt="JavaScript"></div>

<h3 class="fancy">Preface</h3>

There is a huge list of new stuff ES6 brings to the table, I've tried to cover a few of the most relevant things, but there are a <a href="http://es6-features.org/#Constants" target="_blank">ton of other new things</a>, we'll try covering a few more, the odds and ends in this final installment.


<div class="speechBubble"><b>Pssst...</b> Previous ES6 Samplers
</div>

- [ES6 Sampler #1: (Let & Const)]({{ site.baseurl }}/es6-let-const){:target="_blank"}
- [ES6 Sampler #2: (Fat Arrows)]({{ site.baseurl }}/es6-fat-arrows){:target="_blank"}
- [ES6 Sampler #3: (Classes)]({{ site.baseurl }}/es6-classes){:target="_blank"}
- [ES6 Sampler #4: (Spread)]({{ site.baseurl }}/es6-spread){:target="_blank"}
- [ES6 Sampler #5: (Promises)]({{ site.baseurl }}/es6-promises){:target="_blank"}


<b>Default Values</b>

<div class="challenge"> <b>Challenge: </b>Find out what default values are and how to use them, what is their equivalent in es5 ?</div>

<p data-height="600" data-theme-id="0" data-slug-hash="xRWjOZ" data-default-tab="result" data-user="k3no" data-embed-version="2" data-pen-title="ES6 Sampler #6 Odd & Ends - Default values" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/xRWjOZ/">ES6 Sampler #6 Odd & Ends - Default values</a> by Eugenio  Keno   Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

<b>Object.assign</b>

<div class="challenge"> <b>Challenge: </b>Find out what object.assign does to an object, what does it replace in es5?</div>

<p data-height="600" data-theme-id="0" data-slug-hash="ENLNQw" data-default-tab="result" data-user="k3no" data-embed-version="2" data-pen-title="ES6 Sampler #6 Odd & Ends - Object.assign()" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/ENLNQw/">ES6 Sampler #6 Odd & Ends - Object.assign()</a> by Eugenio  Keno   Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

<div class="note"> <b>Note: </b> There are caveats and special cases when cloning/merging some objects, check this page for further Reading:
<a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/assign" target="_blank">Object.assign() MDN...</a>
As for es5, there are multiple ways of cloning and merging objects depending on what it is you are trying to achieve, check this 2 excellent posts for more:
<ul>
<li><a href="http://stackoverflow.com/questions/728360/how-do-i-correctly-clone-a-javascript-object" target="_blank">How to correctly clone a javascript object</a></li>
<li><a href="http://stackoverflow.com/questions/171251/how-can-i-merge-properties-of-two-javascript-objects-dynamically" target="_blank">How can I merge properties of two javascript objects.</a></li>
</ul></div>

<b>Object Method & Properties Shorthands</b>

<div class="challenge"> <b>Challenge: </b>Find out the new shorthands for defining Object Properties in es6 and it's equivalent in es5</div>

<p data-height="900" data-theme-id="0" data-slug-hash="VmdZJV" data-default-tab="result" data-user="k3no" data-embed-version="2" data-pen-title="ES6 Sampler #6 Odd & Ends - Object  Properties shorthand" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/VmdZJV/">ES6 Sampler #6 Odd & Ends - Object  Properties shorthand</a> by Eugenio  Keno   Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

<div class="challenge"> <b>Challenge: </b>Find out the new shorthands for defining Object Methods in es6 and it's equivalent in es5</div>

<p data-height="600" data-theme-id="0" data-slug-hash="ObEJmy" data-default-tab="result" data-user="k3no" data-embed-version="2" data-pen-title="ES6 Sampler #6 Odd & Ends - Object  Methods shorthand" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/ObEJmy/">ES6 Sampler #6 Odd & Ends - Object  Methods shorthand</a> by Eugenio  Keno   Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

<b>Array find</b>

<div class="challenge"> <b>Challenge: </b>Find out how to use the array find & findIndex methods in es6 and their equivalents in es5</div>

<p data-height="700" data-theme-id="0" data-slug-hash="rWKOOG" data-default-tab="result" data-user="k3no" data-embed-version="2" data-pen-title="ES6 Sampler #6 Odd & Ends - Array Find method" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/rWKOOG/">ES6 Sampler #6 Odd & Ends - Array Find method</a> by Eugenio  Keno   Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

<b>String Methods</b>

<div class="challenge"> <b>Challenge: </b>Find out how to use the new es6 string methods</div>

<p data-height="420" data-theme-id="0" data-slug-hash="VmdExQ" data-default-tab="result" data-user="k3no" data-embed-version="2" data-pen-title="ES6 Sampler #6 Odd & Ends -String methods" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/VmdExQ/">ES6 Sampler #6 Odd & Ends -String methods</a> by Eugenio  Keno   Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

And that's it, a final sampler of some of the new things ES6 has to offer, now to start writing with them : )

Best,

Keno.
