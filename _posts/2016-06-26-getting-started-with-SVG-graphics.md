---
layout: post
title: Getting started with SVG graphics
excerpt: Learn SVG (Scalable Vector Graphics) with a few live code samples.
permalink: /Getting-Started-With-SVG
---

<h2><b>Preface</b></h2>

Another post on getting started, this time with SVG ( scalable vector graphics)


*Note: These SVG pens resize and look better while reading this if you open the CSS,JS or HTML along the Result*


<h2><b>Simple SVG Elements</b></h2>

The first thing you might want to do is add some basic shapes, most of the know-how is in the comments in the pens:

<p data-height="440" data-theme-id="0" data-slug-hash="WxGBaK" data-default-tab="html,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/WxGBaK/">Simple SVG Elements</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

<h2><b>Responsive SVG</b></h2>

There are a few ways of making SVG responsive, here are a few detailed in the comments, also check out the further reading bits inside the pens for more:

<p data-height="440" data-theme-id="0" data-slug-hash="MebJvW" data-default-tab="html,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/MebJvW/">Responsive SVG</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>


<h2><b>Animating SVG</b></h2>

Currently (Mid 2016) there are quite a few ways of animating SVG, some are on the way out, some are popular, easy or a combination, let's start with a few of the more obvious:

<h2><b>1. Animating SVG with Vanilla JS</b></h2>

Vanilla (or plain) javascript is perhaps the most robust option, but it does need you to code eveything, so more complex animations might be hard to make.

<p data-height="440" data-theme-id="0" data-slug-hash="beBmeq" data-default-tab="js,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/beBmeq/">Animating SVG with Vanilla JS</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>


<h2><b>2. Animating SVG with &lt; animate &gt; </b></h2>

&lt; animate &gt; is a cool way of animating SVG, right inside the SVG element : ), unfortunately, there is no support on ie :(

  <p data-height="440" data-theme-id="0" data-slug-hash="vKyVby" data-default-tab="html,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/vKyVby/">Animating SVG with < animate ></a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
  <script async src="//assets.codepen.io/assets/embed/ei.js"></script>

<h2><b>3.Animating SVG with &lt; animate &gt; & Js </b></h2>

Still no ie support for this one, but you could do slightly more complex things involving javascript, try clicking on the pen...

<p data-height="440" data-theme-id="0" data-slug-hash="dXNYMp" data-default-tab="html,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/dXNYMp/">Animating SVG with < animate > & JS</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

<h2><b>4. Animating SVG with CSS</b></h2>

CSS is another way of animating svg,you are mostly animating the element through transforms and translations on a style sheet, so this approach might not be the best for more complex animations, still it has wide browser support, and keyframe support, we are also adding an svg filter to sass it up.

<p data-height="440" data-theme-id="0" data-slug-hash="oLBGwr" data-default-tab="html,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/oLBGwr/">Animating  SVG  with CSS</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

<h2><b>Selecting & Interacting with SVG via CSS</b></h2>

And since SVG is another DOM element you can interact with it via CSS:

<p data-height="440" data-theme-id="0" data-slug-hash="JKEYOR" data-default-tab="html,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/JKEYOR/">Selecting SVG elements with CSS</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

<h2><b>Selecting & Interacting with SVG via Javascript</b></h2>

But more likely than not, you wwill be interacting with SVG through Javascript, here's a very basic example with Vanilla Javascript.

<p data-height="440" data-theme-id="0" data-slug-hash="LZxrXP" data-default-tab="html,result" data-user="k3no" data-embed-version="2" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/LZxrXP/">Selecting SVG elements with Javascript</a> by Eugenio - Keno -  Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

And That's it for now, I hope these pens help you get started with SVG graphics.

Best,

Keno
