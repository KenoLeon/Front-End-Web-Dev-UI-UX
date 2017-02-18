---
layout: post
title: 'Getting to know Typescript Part 2.'
excerpt: A second look at typescript to further a simple overview of it's features with some code samples.
permalink: /TypescriptPt2
smlogo: TS.png
---
![javascript](https://kenoleon.github.io/Front-End-Web-Dev-UI-UX/assets/images/TSLogo.jpg)

<h3 class="fancy">Preface</h3>

Let's check out more Typescript ! These will still be very beginner friendly Typescript code samples, but hopefully we will end up with a general overview of what typescript brings to the table.

<div class="speechBubble">Check out the first post on this series,a good place to start if you have no idea what Typescript is:
</div>


- [Getting to know Typescript Part 1.]({{ site.baseurl }}/TypescriptPt1){:target="_blank"}

<h3 class="fancy">Functions</h3>

<div class="step"> <b>Step 1: </b>Figure out function types</div>

<p data-height="420" data-theme-id="27284" data-slug-hash="wgOKqR" data-default-tab="result" data-user="k3no" data-embed-version="2" data-pen-title="TypeScript - Function Types" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/wgOKqR/">TypeScript - Function Types</a> by Eugenio  Keno   Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

Not much to it, we can now add types to our functions by adding a type declaration to the function...

<div class="note"><b>Note: </b> In case you need a reminder, the reason types are considered useful, is that Javascript variables are instantiated at run-time, Typescript is Static, so there are no surprises and less bugs since you can check them with your compiler before running the script</div>

<div class="step"> <b>Step 2: </b>Figure out function parameters</div>

Speaking of functions, so what would happen if you gave a function more parameters than it's function definition had ? well, you would get an error in Typescript like this one:



![Atom-TypeScript function parameter error](https://kenoleon.github.io/Front-End-Web-Dev-UI-UX/assets/images/postImages/Typescript/AtomFunctionParameterError.jpg)

In order to better deal with this sort of situation, Typescript provides support for both Optional Function parameters and default parameters, let's check them both:

<div class="step"> <b>Step 2a: </b>Figure out Optional function parameters...</div>

<p data-height="760" data-theme-id="27284" data-slug-hash="PWLPvg" data-default-tab="result" data-user="k3no" data-embed-version="2" data-pen-title="TypeScript - Optional Function Parameters" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/PWLPvg/">TypeScript - Optional Function Parameters</a> by Eugenio  Keno   Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

<div class="note"><b>Note: </b> I've included a common way of doing the same thing in plain (vanilla) javascript for comparison</div>

<div class="step"> <b>Step 2b: </b>Figure out Default function parameters...</div>

<p data-height="960" data-theme-id="27284" data-slug-hash="jyJgXy" data-default-tab="result" data-user="k3no" data-embed-version="2" data-pen-title="TypeScript - Default Function Parameters" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/jyJgXy/">TypeScript - Default Function Parameters</a> by Eugenio  Keno   Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

<div class="note"><b>Note: </b> ES5 (plain javascript) and new ES6 syntax also added for comparison</div>

<b>More on functions...</b> There are a few other things involving functions and Typescript (This, overloading for instance), check out the official docs for more... <a href="http://www.typescriptlang.org/docs/handbook/functions.html" target="_blank"><b>Typescript- HandBook: Functions</b></a>


<h3 class="fancy">Data Constructs in Typescript</h3>

Typescript also supports many newer Javascript data functions and also has some of it's own, let's check them out:


<div class="step"> <b>Step 3a: </b>Figure out what enums are and how to use them</div>


<p data-height="680" data-theme-id="27284" data-slug-hash="GrLXpX" data-default-tab="result" data-user="k3no" data-embed-version="2" data-pen-title="TypeScript - Enums" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/GrLXpX/">TypeScript - Enums</a> by Eugenio  Keno   Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>


An enum is a way to organize a collection of related values (like an array with internal operations), check out:<a href="https://basarat.gitbooks.io/typescript/content/docs/enums.html#enums" target="_blank"><b>Typescript Deep Dive - Enums</b></a> for more.

<div class="note"><b>The more you know: </b> So why would you use enums? , well, if you have a number of variables that are not going to change much (flags,constants etc),  you can use enums and your code (your method calls) reads better, instead of <pre><code>chose(option[2])</code></pre>you can write <code><pre>chose(option.optionA)</pre></code></div>

<div class="step"> <b>Step 3b: </b>Figure out what for..of is for and how to use it.</div>

<p data-height="720" data-theme-id="27284" data-slug-hash="MJRxeL" data-default-tab="result" data-user="k3no" data-embed-version="2" data-pen-title="TypeScript - For..Of" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/MJRxeL/">TypeScript - For..Of</a> by Eugenio  Keno   Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>




For..of is a convenient way of Iterating over an iterable and returning values instead of keys as in the first Javascript example (which returns keys instead of values)  note that it is not exclusive to Typescript, and the syntax is the same as in ES6, you can read more about iterables in Javascript here:<a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Iteration_protocols" target="_blank"><b>Iteration protocols</b></a>

And that's it for now, I'll come back for a final overview on Typescript and how to organize your files, I hope this code samples help you getting started with Typescript...

Best,

Keno
