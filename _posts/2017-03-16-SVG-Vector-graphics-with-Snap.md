---
layout: post
title: SVG Vector graphics with Snap.svg
excerpt: Snap is a great little library for working with svg graphics, come along and check it out !
permalink: /svgGraphicsSnap
smlogo: snapsvg.png
---

![Snap.svg](https://kenoleon.github.io/Front-End-Web-Dev-UI-UX/assets/images/snapSVG.jpg)

<h3 class="fancy">Preface</h3>

<b><a href="http://snapsvg.io" target="_blank">Snap.svg</a></b> <b>"The JavaScript SVG library for the modern web" </b> is an all in one javascript library for working with vector based graphics, the documentation is a bit sparse, and even though I've worked with Snap.svg in the past, I would like to make a getting started post for future reference and to help those just getting started, at the end of these code samples both you and I will be able to present and animate with vector graphics, so lets get started.

<div class="speechBubble"><i>Hey,( totally optional) if you are new to SVG Graphics, you might like this other post:</i></div>

- [Getting started with SVG Graphics.]({{ site.baseurl }}/Getting-Started-With-SVG){:target="_blank"}


<h3 class="fancy">Let's start by setting up - Basics</h3>

<div class="step"> <b>Step 1: </b>Import Snap.svg and create a simple vector Graphic</div>

<p data-height="600" data-theme-id="27284" data-slug-hash="QpjWyo" data-default-tab="result" data-user="k3no" data-embed-version="2" data-pen-title="Snap.svg Setup" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/QpjWyo/">Snap.svg Setup</a> by Eugenio  Keno   Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

<div class="explain"><b>Explanation: </b>
<ul>
  <li>After importing Snap.svg (check the JS tab)  you will then need an SVG element in your HTML, you will also need to position it  and size it, I am using Bootstrap to simplify things, but you can use something else (plain CSS,other frameworks, JS).</li>

<li>Once you have your SVG element, reference it in Javascript and that's it, you can start adding elements,(circles in this case and changing their appearance).</li>
</ul>

</div>

<div class="challenge"> <b>You try it. </b> <i> Recreate the previous code sample with Rectangles and different colors </i></div>


<div class="step"> <b>Step 2: </b>Animate a simple shape with Snap.svg</div>

<p data-height="600" data-theme-id="27284" data-slug-hash="367f4c9979f6a5c2514ac8704de7849d" data-default-tab="result,js" data-user="k3no" data-embed-version="2" data-pen-title="Snap.svg Animation" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/367f4c9979f6a5c2514ac8704de7849d/">Snap.svg Animation</a> by Eugenio  Keno   Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

<div class="explain"><b>Explanation: </b> Snap provides a handy <b>animate()</b> function for your basic animation needs, it is a simple affair where you provide the attributes to change ( from their current value), time to make those changes, easing function (rate of change function) and a callback function to tie animations or call other functions.
</div>

<div class="challenge"> <b>You try it. </b> <i> Recreate the previous code sample with  multiple elements and vertical animations </i></div>

<div class="step"> <b>Step 3: </b>Add mouse events & Touch Events</div>

<p data-height="600" data-theme-id="27284" data-slug-hash="ZeWXKv" data-default-tab="result" data-user="k3no" data-embed-version="2" data-pen-title="Snap.svg Interaction" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/ZeWXKv/">Snap.svg Interaction</a> by Eugenio  Keno   Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

<div class="explain"><b>Explanation: </b> Like with animations, Snap tries to make it super simple to add interactions like mouse and touch events by simply calling the relevant method on your snap element, something like:<br/>

<code><b>YOUR-SNAP-ELEMENT.mouseup(FUNCTION TO HANDLE MOUSEUP)</b></code> <br/>

And you are done : )
</div>

<div class="note"><b>Note: </b> I had some issues with the stock drag function, since it doesn't play nice with responsive displays, so some extra calculations need to be made for it to work, check the code.</div>

<div class="challenge"> <b>You try it. </b> <i> Add interaction to multiple snap elements</i></div>

<h3 class="fancy">Intermediate Snap.svg</h3>

<b>Importing vector graphics</b>

Beyond simple primitives made with Snap, you can also import vector art made on other programs:<i>Inkscape (Free) and Illustrator (Paid) are popular options </i>, let's figure out how to import some art...

<div class="step"> <b>Step 4: </b>Import some vector art !</div>

<p data-height="600" data-theme-id="27284" data-slug-hash="KWMZXO" data-default-tab="result" data-user="k3no" data-embed-version="2" data-pen-title="Snap.svg Loading external svgs" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/KWMZXO/">Snap.svg Loading external svgs</a> by Eugenio  Keno   Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

<div class="explain"><b>Explanation: </b>
Importing external SVG Artwork is done by using snaps <a href="http://snapsvg.io/docs/#Snap.load" target="_blank"><b>load function </b></a>and a callback function to deal with the result. Note that while you can display complex art relatively easy, if you want to deal with parts of your svg programatically you need to format your svgs into something snap can work with, in this case my original svg artwork was an Illustrator file that got converted into a compound path <i>(Object->CompoundPath->make)</i> and named as "mrCube" in the layer option, and then saved as an svg. This way you can select and modify it once the svg is loaded with <b>geom = data.select("#mrCube")</b>
</div>

<div class="challenge"> <b>You try it. </b> <i> Make and import an external vector graphic.</i></div>

In order to make more complex and interactive graphics, we need to deal with multiple elements and complex paths, so let's try that.


<div class="step"> <b>Step 5: </b>Import a complex svg with multiple elements and interact with it via snap.</div>

<p data-height="660" data-theme-id="27284" data-slug-hash="WpGbbK" data-default-tab="result" data-user="k3no" data-embed-version="2" data-pen-title="Snap.svg Loading Complex Svgs" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/WpGbbK/">Snap.svg Loading Complex Svgs</a> by Eugenio  Keno   Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>

<div class="explain"><b>Explanation: </b>A lot is happening here, so let's go step by step:

<ul>
<li>we are loading an external svg like before, but in this case the svg has 2 named paths <i>truckY</i> and <i>textY</i>, we then select each one by id with <i>data.select("#id")</i>, like a css selector.</li>
<li>We now can move and resize them with by defining a Matrix (A coordinate system, you can read more about it here: <a href="https://sarasoueidan.com/blog/svg-transformations/#matrix" target="_blank"><b>Matrix transformations</b></a> )</li>
<li>Next we are attaching a hover to the truck and animating the text inside the Hover Handler</li>
</ul>
</div>

<div class="challenge"> <b>You try it. </b> <i> Make and import an external vector graphic with multiple elements and reference & modify them in snap</i></div>

<div class="note"><b>Note: </b>Our animations now use <a href="http://snapsvg.io/docs/#mina" target="_blank"><b>mina easing</b></a>, to give the text that bounce, there is also an abbreviated transform animation that confusingly is not explained in Snaps documentation, but it is in Raphaël, a very similar svg library from the same author =>  <a href="http://dmitrybaranovskiy.github.io/raphael/reference.html#Element.transform" target="_blank"><b>Raphaël Library element transform.</b></a> </div>

<h3 class="fancy">All together now<</h3>
So now that we have a basic understanding of Snap.svg let's try making an interactive animated vector graphic with Snap !


<p data-height="600" data-theme-id="27284" data-slug-hash="peRrYq" data-default-tab="result" data-user="k3no" data-embed-version="2" data-pen-title="Snap.svg Demo wip" class="codepen">See the Pen <a href="http://codepen.io/k3no/pen/peRrYq/">Snap.svg Demo wip</a> by Eugenio  Keno   Leon (<a href="http://codepen.io/k3no">@k3no</a>) on <a href="http://codepen.io">CodePen</a>.</p>
<script async src="https://production-assets.codepen.io/assets/embed/ei.js"></script>


<div class="explain"><b>Explanation: </b>If you look under the hood( pun intended ), you might find there is a lot of code, but there is also a lot of repetition and there is nothing new from the previous examples, so nothing too scary; in general it goes like this:

<ul>
<li>Load and create all the separate elements and their initial attributes like position and visibility</li>
<li>Attach interaction events and call animations</li>
<li>The remaining  code is just animation functions and event handlers</li>
</ul>

</div>


<div class="challenge"> <b>You try it. </b> <i>Create and animate multiple Svg elements and add interaction to a couple of them.</i></div>


<h3 class="fancy">Conclusion</h3>

I personally love working with SVGs, they scale and display nicely and there are great tools for creating them, the problem usually is that they are not as performant as say HTML5 Canvas or CSS or easy to work with, Snap.svg is a super cool library that tries to bridge this gap and provide a basic yet complete set of tools for working with svg on the web, while not a complete replacement or solution,you can add very cool interactions in no time ( once you follow this or other guides ).

I hope this code samples spark your interest in making some cool interactive svg graphics for the web.

Best,

Keno
