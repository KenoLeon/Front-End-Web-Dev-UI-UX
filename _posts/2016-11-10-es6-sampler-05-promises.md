---
layout: post
title: 'ES6 Sampler #5 : Promises ( were made ) '
excerpt: More samples of new Javascript's ES6 features, this time we look at promises, come along and see how they work.
permalink: /es6-promises
smlogo: Js.png
---

<div class="text-center"><img src="assets/images/JSLogo.jpg" alt="JavaScript"></div>

<h3 class="fancy">Preface</h3>

ES6 brings a new way of handling event flow with the new promise object, this seems to be a huge addition to Javascript since it involves new ways of doing asynchronous computations, but what are asynchronous computations ? what are synchronous, and how do promises work, what do they do ? Come along and let's figure it out.



<div class="speechBubble"><b>Pssst...</b> Previous ES6 Samplers
</div>

- [ES6 Sampler #1: (Let & Const)]({{ site.baseurl }}/es6-let-const){:target="_blank"}
- [ES6 Sampler #2: (Fat Arrows)]({{ site.baseurl }}/es6-fat-arrows){:target="_blank"}
- [ES6 Sampler #3: (Classes)]({{ site.baseurl }}/es6-classes){:target="_blank"}
- [ES6 Sampler #4: (Spread)]({{ site.baseurl }}/es6-spread){:target="_blank"}


<div class="challenge"> <b>Note - Challenges: </b> I gave myself little challenges you are welcome to try if you want to recreate my own learning curve.</div>

<h3 class="fancy">Let's start:</h3>

<div class="challenge"> <b>Challenge: </b> Find out what synchronous and asynchronous computations are. </div>

<p data-height="1000" data-theme-id="0" data-slug-hash="JbPLMj" data-default-tab="result" data-user="k3no" data-embed-version="2" data-pen-title="ES6 Sampler - Promises Pt. 1" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/JbPLMj/">ES6 Sampler - Promises Pt. 1</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

Great, so sequential operations are analogous to synchronous computations, that is things that happen one step at a time in order, asynchronous computations, on the other hand can happen independently from one another, in this case via a timeout function. So, I guess the next thing we might need to figure out, is why we need promises, I mean the previous example worked fine, why add new objects if they don't serve a purpose.

<div class="challenge"> <b>Challenge: </b>Find out why are promises needed, what problem they solve ?</div>

<p data-height="1200" data-theme-id="0" data-slug-hash="oYNBzK" data-default-tab="result" data-user="k3no" data-embed-version="2" data-pen-title="ES6 Sampler - Promises Pt. 2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/oYNBzK/">ES6 Sampler - Promises Pt. 2</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

So it seems that promises were introduced to deal with the above 2 problems, callback Hell.- where it is easy to loose track of what happens where and the Pyramid of Doom which is just hard to write and maintain, so what do promises offer, how do they work ?


<div class="challenge"> <b>Challenge: </b>Create a basic promise</div>

<div class="note"> <b>From the docs - </b>
<i> new Promise( /* executor */ function(resolve, reject) { ... } );</i>
</div>

<p data-height="1300" data-theme-id="0" data-slug-hash="KNKYJO" data-default-tab="result" data-user="k3no" data-embed-version="2" data-pen-title="ES6 Sampler - Promises Pt. 3" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/KNKYJO/">ES6 Sampler - Promises Pt. 3</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

Ahhh, so after a bit of trial an error, I think I got a handle on the basics of promises, you define them with reject (In case of errors) and resolve (in case everything went well) clauses, and then call them and use whatever they produce to control the flow of your program down stream, it seems a little like overkill, the syntax definitely gets some time to get used to, so let's revisit our original premise and find out how to rewrite things with promises...

<div class="challenge"> <b>Challenge: </b> Solve the callback hell and pyramid of doom problems with promises</div>

<p data-height="500" data-theme-id="0" data-slug-hash="VmYxdp" data-default-tab="result" data-user="k3no" data-embed-version="2" data-pen-title="ES6 Sampler - Promises Pt. 4" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/VmYxdp/">ES6 Sampler - Promises Pt. 4</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

The above mini sample hopefully exemplifies how promises make things a little more readable.

And how about Async computations ? surely this is where promises will be of use the most.

<div class="challenge"> <b>Challenge: </b> Do some Async computations with promises</div>

<p data-height="600" data-theme-id="0" data-slug-hash="JbovwR" data-default-tab="result" data-user="k3no" data-embed-version="2" data-pen-title="ES6 Sampler - Promises Pt. 5" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/JbovwR/">ES6 Sampler - Promises Pt. 5</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

So after all this preamble, the last thing I would like to do is figure out some real world examples:

<div class="challenge"> <b>Challenge: </b> Find Real world uses of promises</div>

<p data-height="900" data-theme-id="0" data-slug-hash="yVNMwr" data-default-tab="result" data-user="k3no" data-embed-version="2" data-pen-title="ES6 Sampler - Promises Pt. 6" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/yVNMwr/">ES6 Sampler - Promises Pt. 6</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

It takes a little getting used to, but anything that returns something after some time can probably be rewritten using promises, as to whether or not you want to, that is entirely up to you, but as other programmers take a liking to promises, you will encounter them in the wild, so it's better to know how to spot them.

<h3 class="fancy">Conclusion</h3>

Promises seem to be a more robust and complex alternative to using callbacks to control the flow of your program,they take some getting used to, but are somehow clearer at displaying and managing complex asynchronous operations.


<h3 class="fancy"> TL&#59;DR: </h3>

<b>Promises are a sophisticated way of handling async & sync computations and the flow of operations within your program.</b>

Best,

Keno.
