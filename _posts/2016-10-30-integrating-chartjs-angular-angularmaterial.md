---
layout: post
title: 'Integrating Angular ChartJs and Angular Material'
excerpt: A post documenting how to build a small warehouse chart app with Angular, chart.js and Angular Material, code samples from the ground up.
permalink: /integrating-angularjs-chartjs
smlogo: AngularChartJS.png
---

<div class="text-center"><img src="assets/images/AngularChartjs.png" alt="Angular Chart JS"></div>

<h3 class="fancy">Preface</h3>

One of the cool things about Front End Development  is that you get to choose from a multitude of libraries and play mad scientist, come along and see if we can mix some libraries right here in codepen.

<div class="challenge"> <b>Note - Challenges: </b> I gave myself little challenges you are welcome to try if you want to recreate my own experimentation.</div>

<h3 class="fancy">What's the plan ?</h3>

The plan is to use 3 libraries and a plugin:

<ul>
<li>
<b><a href="https://www.angularjs.org" target="_blank">Angular.js</a></b> For the logic and as a framework.</li>
<li><b><a href="http://chartjs.org/" target="_blank">Chart.js</a></b> For making Charts.</li>
<li><b><a href="https://material.angularjs.org/latest/" target="_blank">Angular Material</a></b>  For styling the UI/UX.</li>
<li><b><a href="https://jtblin.github.io/angular-chart.js/" target="_blank">Angular-chart</a></b> A Chart.js plugin for easier Angular Integration.</li>
</ul>

<div class="speechBubble"><b>Pssst...</b> If you are a little lost with the libraries, here are some handy posts you might like:
</div>


- [Getting Started with Angular.js]({{ site.baseurl }}/getting-started-with-AngularJs){:target="_blank"}
- [Let's Try Angular Material]({{ site.baseurl }}/lets-try-Angular-Material){:target="_blank"}
- [Getting Started with Chart.js]({{ site.baseurl }}/getting-started-with-chartjs){:target="_blank"}


The first thing I would like to do, is try a minimal example without Angular Material and then move up from there,styling will be next.

<div class="challenge"> <b>Experiment: </b>Import Angular.js, Chart.js and Angular-chart</div>

<div class="note"> <b>Note - </b> I'll be using Angular 1.5 for now, I'll update to Angular 2 at some point in the future.</div>

<p data-height="500" data-theme-id="0" data-slug-hash="zKZRxG" data-default-tab="js,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/zKZRxG/">Angular-Chart.js</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

And there you have it, not much to it, just add the libraries and define your directives (data, options etc).

<h3 class="fancy">What's next ?</h3>

The next thing I would like to investigate, is how to modify the chart via Angular's two way data binding.

<div class="challenge"> <b>Experiment: </b>Bind Chart Data 2 ways with Angular</div>

<p data-height="500" data-theme-id="0" data-slug-hash="rrRLvm" data-default-tab="js,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/rrRLvm/">Angular-Chart.js Data Binding</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

So far so good, let's now try adding a basic Angular Material container before going further...

<div class="challenge"> <b>Experiment: </b>Add a basic Angular Material container to a chart.</div>

<p data-height="500" data-theme-id="0" data-slug-hash="qavZEQ" data-default-tab="js,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/qavZEQ/">Angular Material + Chart.js</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

Almost there !, besides the sheer number of dependencies needed, 7 Javascript Imports and a couple of Stylesheets, nothing to be scared off, so Now I think we are ready to start adding some more complex Angular Material Directives.

<div class="challenge"> <b>Experiment: </b>Add 2 way binding Angular Material Directives</div>

<p data-height="500" data-theme-id="0" data-slug-hash="QKPBBb" data-default-tab="js,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/QKPBBb/">Angular Material + Chart.js + DataBinding</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

 Surprisingly, most of the hard work was figuring out the right Material design components to use, the data binding was basically dealt with ng-repeat and ng-model. So now that we have a good understanding of how the libraries work together, let's trow the Material Kitchen sink at it...

<div class="challenge"> <b>Final Experiment: </b>Add more and more Material design elements ( The kitchen sink ) to a chart.js Angular App</div>

 <p data-height="800" data-theme-id="0" data-slug-hash="KgLvrg" data-default-tab="result" data-user="k3no" data-embed-version="2" data-pen-title=" Chart.js with Angular Material KitchenSink  WIP" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/KgLvrg/"> Chart.js with Angular Material KitchenSink  WIP</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

And there you have it, a responsive web App made with Angular, Angular Material and Chart.js, the only thing missing would be a backend to store information,manage users and add stuff, you will definitely need stuff :).

<h3 class="fancy">Conclusion</h3>

Integrating various Javascript libraries is fun, especially if you do it with a cautious step by step approach


Best,

Keno.
